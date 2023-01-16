# Mengupdate Header Customer Invoice
#### Endpoint
```bash
/api/account.invoice/update/<<id-invoice>>
```


#### Parameter
- **token:** API token</br>
- **update_vals:**

| Key               | Type                     | Description                                                                    |
| :---              | :---                     | :---                                                                           |
| partner_id        | integer                  | ID Partner yang didapat dari [Mencari ID Partner](../search_master/partner.md) |
| customer_code     | string                   | Kode klien                                                                     |
| account_id        | integer                  | Isi dengan ID: <b>948</b>                                                      |
| journal_id        | integer                  | Isi dengan ID: <b>46</b>                                                       |
| type              | string                   | Isi dengan <b>out_invoice</b>  
| partner_bank_id   | integer                  | ID rekening bank tujuan
| date_invoice      | date                     | Tanggal Invoice                                                                |
| date_due          | date                     | Tanggal Jatuh Tempo                                                            |
| urgent            | boolean                  | True apabila urgent
| urgency_note      | text                     | Catatan terkait urgency                                                        |
| period_id         | integer                  | Diisi dengan **False**
| invoice_line      | [(5)]                    | Detail Invoices. Penjelasan ada dibawah                                        |
| last_backoffice_sync      | datetime                     | Waktu terakhir invoice diupdate dari backoffice                                                       |


#### Contoh
```bash
create_vals="{
    'partner_id': 22,
    'journal_id': 46,
    'account_id': 948,
    'type': 'out_invoice',
    'date_invoice': '2020-10-10',
    'date_due': '2020-10-10',
    'period_id': False,
    'invoice_line': [
        (5)
    ]
}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&update_vals=${update_vals}" \
    https://demo8.simetri-sinergi.id/api/account.invoice/update/4
```

