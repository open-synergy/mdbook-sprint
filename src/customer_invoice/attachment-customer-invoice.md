# Menambahkan Attachment Pada Customer Invoice
#### Endpoint
```bash
/api/ir.attachment/create
```

#### Parameter
- **token:** API token</br>
- **create_vals:**

| Key               | Type                     | Description                                                                    |
| :---              | :---                     | :---                                                                           |
| datas             | base64                   | base64 file yang akan diattach                                                 |
| datas_fname       | string                   | nama file yang akan diattach                                                   |
| name              | base64                   | nama attachment. Boleh sama dengan datas_fname                                 |
| res_model         | string                   | diisi **account.invoice**                                                      |
| res_id            | integer                  | ID customer invoice                                                            |
                                      |


#### Contoh
```bash
create_vals="{
    'datas_fname': 'rekap-penagihan.pdf',
    'name': 'rekap-penagihan.pdf',
    'res_model': 'account.invoice',
    'res_id': 34,
    'datas': base64,
}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&create_vals=${create_vals}" \
    https://demo8.simetri-sinergi.id/api/ir.attachment/create
```
