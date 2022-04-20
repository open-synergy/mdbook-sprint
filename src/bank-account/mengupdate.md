# Mengupdate Bank Account
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/update_data.md)

#### Parameter
- <b>model:</b>res.partner.bank</br>
- <b>update_vals:</b> </br>

| Key                                          | Type                     | Description                                                                                                   |
| :---                                         | :---                     | :---                                                                                                          |
| acc_number                                   | string                   | Account Number                                                                                                |
| bank                                         | integer                  | ID Bank yang didapat dari [Mencari Bank](../search_master/bank.md)                                            |
| bank_name                                    | string                   | Bank Name                                                                                                     |
| journal_id                                   | integer                  | ID Journal yang didapat dari [Mencari Journal](../search_master/journal.md)                                   |

#### Contoh
```bash
update_vals="{
    'acc_number': '12392883883',
}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&create_vals=${update_vals}" \
    https://demo8.simetri-sinergi.id/api/res.partner.bank/update/{id_bank_account}
```
