# Membuat Customer Invoice
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/create_data.md)

#### Parameter
- <b>model:</b> account.invoice</br>
- <b>create_vals:</b> </br>

| Key               | Type                     | Description                                                                    |
| :---              | :---                     | :---                                                                           |
| internal_number   | string                   | Nomor Invoice                                                                  |
| partner_id        | integer                  | ID Partner yang didapat dari [Mencari ID Partner](../search_master/partner.md) |
| customer_code     | string                   | Kode klien                                                                     |
| account_id        | integer                  | Isi dengan ID: <b>948</b>                                                      |
| journal_id        | integer                  | Isi dengan ID: <b>46</b>                                                       |
| type              | string                   | Isi dengan <b>out_invoice</b>  
| partner_bank_id   | integer                  | ID rekening bank tujuan
[ payment_term      | integer                  } Gunakan ID 4 untuk 14 hari. ID 3 untuk 30 hari                                 |
| user_id           | integer                  | ID user yang bertanggung jawab                                                 |
| urgent            | boolean                  | True apabila urgent
| urgency_note      | text                     | Catatan terkait urgency                                                        |
| invoice_line      | [(0, 0, &lt;dict&gt;)]   | Detail Invoices. Penjelasan ada dibawah                                        |
| urgency_note      | text                     | Catatan terkait urgency                                                        |
| last_backoffice_sync      | datetime                     | Waktu terakhir invoice diupdate dari backoffice                                                       |

- Penjelasan isi dictionary dari <b>invoice_line:</b> </br>

| Key                 | Type                           | Description                                                                                                                     |
| :---                | :---                           | :---                                                                                                                            |
| sequence            | integer                        | Urutan
| product_id          | integer                        | ID Produk layanan.
| name                | string                         | Deskripsi Invoice                                                                                                               |
| account_id          | integer                        | ID Account yang didapat dari [Mencari ID Account](../search_master/account.md)                                                  |
| price_unit          | float                          | Harga satuan                                                                                                                    |
| quantity            | float                          | Kuantitas                                                                                                                       |
| invoice_line_tax_id | [(6, 0, &lt;list_of_id&gt;)]   | Apabila ada PPN, (1) isi <b>list_of_id</b> dengan <b>[14]</b> jika exclude PPN, atau (2)<b>[16]</b> jika include PPN, atau (3) **[14,13]** jika exclude PPN dan klien adalah WAPU, atau (4) **[16,15]** jika include PPN dan klien adalah WAPU. Apabila tidak ada hilangkan.|

#### Contoh
```bash
create_vals="{
    'internal_number': 'TEST/INV/2020/10/10/0001',
    'partner_id': 22,
    'journal_id': 46,
    'account_id': 948,
    'type': 'out_invoice',
    'date_invoice': '2020-10-10',
    'date_due': '2020-10-10',
    'invoice_line': [
        (0, 0, {
            'name': 'Item #1',
            'account_id': 198,
            'price_unit': 40000.00,
            'quantity': 3,
            'invoice_line_tax_id': [(6, 0, [3])]
        }),
        (0, 0, {
            'name': 'Item #2',
            'account_id': 198,
            'price_unit': 100000.00,
            'quantity': 1,
        }),
    ]
}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&create_vals=${create_vals}" \
    https://demo8.simetri-sinergi.id/api/account.invoice/create
```
