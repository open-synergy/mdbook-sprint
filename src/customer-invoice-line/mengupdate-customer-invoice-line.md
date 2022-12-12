# Mengupdate Customer Invoice Line
#### Endpoint
```bash
/api/account.invoice.line/update/<<id-invoice-line>>
```


#### Parameter
- **token:** API token</br>
- **update_vals:**

| Key                 | Type                           | Description                                                                                                                     |
| :---                | :---                           | :---                                                                                                                            |
| sequence            | integer                        | Urutan
| product_id          | integer                        | ID Produk layanan.                                                            |
| name                | string                         | Deskripsi Invoice                                                      |
| account_id          | integer                        | ID Account yang didapat dari [Mencari ID Account](../search_master/account.md)                                                  |
| price_unit          | float                          | Harga satuan                                                                                                                    |
| quantity            | float                          | Kuantitas                                                                                                                       |
| invoice_line_tax_id | [(6, 0, &lt;list_of_id&gt;)]   | Apabila ada PPN, (1) isi <b>list_of_id</b> dengan <b>[14]</b> jika exclude PPN, atau (2)<b>[16]</b> jika include PPN, atau (3) **[14,13]** jika exclude PPN dan klien adalah WAPU, atau (4) **[16,15]** jika include PPN dan klien adalah WAPU. Apabila tidak ada hilangkan.|

#### Contoh
```bash
update_vals="{
    'name': 'Item #1',
    'account_id': 198,
    'price_unit': 40000.00,
    'quantity': 3,
    'invoice_line_tax_id': [(6, 0, [3])]
}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&update_vals=${update_vals}" \
    https://demo8.simetri-sinergi.id/api/account.invoice.line/update/1234
```


