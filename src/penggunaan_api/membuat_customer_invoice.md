# Membuat Customer Invoice
#### Langkah 1: Generate Token User yang digunakan untuk API
Menjalankan API untuk Generate Token, sehingga token akan di-<i>generate</i> ulang </br></br>
Contoh:
```
https://demo8.simetri-sinergi.id/api/user/get_token/api/user/get_token?login=admin&password=test123
```
#### Langkah 2: Mencari ID Partner
Mencari ID Partner yang sesuai di Odoo.</br>
Kriteria pencarian data yang akan digunakan adalah: <b>[('ref', '=', <kode_klien>)]</b>, dimana <b>kode_klien</b> adalah kode Partner yang terdaftar pada aplikasi yang akan menjalankan API Odoo.</br></br>
Contoh:
```
https://demo8.simetri-sinergi.id/api/res.partner/search?token=5e15c55228834261944ad24c6ce15e7a&domain=[('ref', '=', 'ADM')]
```
#### Langkah 3: Mencari ID Account
Mencari ID Account yang sesuai di Odoo.</br>
Kriteria pencarian data yang akan digunakan adalah: <b>[('code', '=', <kode_akun>)]</b>, dimana <b>kode_akun</b> adalah kode Account yang terdaftar pada aplikasi yang akan menjalankan API Odoo.</br></br>
Contoh:
```
https://demo8.simetri-sinergi.id/api/account.account/search?token=5e15c55228834261944ad24c6ce15e7a&domain=[('code', '=', '01.01.01')]
```
#### Langkah 4: Membuat Customer Invoice
Format <b>create_vals</b> yang digunakan untuk pembuatan Customer Invoice, adalah:
```
{
    'internal_number': <str:no_invoice>,
    'partner_id': <int:partner_id>, # Output ID Partner dari hasil Langkah 2
    'account_id': 948, # Fixed
    'journal_id': 46, # Fixed
    'type': 'out_invoice', #Fixed
    'date_invoice': <date:date_invoice>,
    'date_due': <date:date_due>
    'invoice_lines': [
        (0, 0, {
            'name': <str:item>,
            'account_id': <int:account_id>, # Output ID Account dari hasil Langkah 3
            'price_unit': <numeric:price_unit>,
            'qty': <numeric:qty>,
            'tax_ids': [(6, 0, [<int:tax_id>])] #Hilang jika tidak ada PPN. Gunakan 3 jika exclude. 4 untuk include
        })
    ]}"
}
```

Contoh:
```
create_vals="{
    'internal_number': 'TEST/INV/2020/10/10/0001',
    'partner_id': 12,
    'journal_id': 3,
    'account_id': 138,
    'type': 'out_invoice',
    'date_invoice': '2020-10-10',
    'date_due': '2020-10-10',
    'invoice_lines': [
        (0, 0, {
            'name': 'Item #1',
            'account_id': 198,
            'price_unit': 40000.00,
            'qty': 3,
            'tax_ids': [(6, 0, [3])]
        }),
        (0, 0, {
            'name': 'Item #2',
            'account_id': 198,
            'price_unit': 100000.00,
            'qty': 1,
        }),
    ]
}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&create_vals=${create_vals}" \
    https://demo8.simetri-sinergi.id/api/account.invoice/create
```
