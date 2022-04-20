# Membuat Bank Account
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/create_data.md)

#### Parameter
- <b>model:</b>res.partner.bank</br>
- <b>create_vals:</b> </br>

| Key                                          | Type                     | Description                                                                                                   |
| :---                                         | :---                     | :---                                                                                                          |
| state                                        | string                   | Bank Account Type, isi dengan "<b>bank</b>"                                                                   |
| acc_number                                   | string                   | Account Number                                                                                                |
| bank                                         | integer                  | ID Bank yang didapat dari [Mencari Bank](../search_master/bank.md)                                            |
| bank_name                                    | string                   | Bank Name                                                                                                     |
| partner_id                                   | integer                  | Account Owner, isi dengan "<b>1</b>"                                                                          |
| journal_id                                   | integer                  | ID Journal yang didapat dari [Mencari Journal](../search_master/journal.md)                                   |

#### Contoh
```bash
create_vals="{
    'state': 'bank',
    'acc_number': '0293282931829',
    'bank': 13,
    'bank_name': 'BCA KCP Serpong',
    'partner_id': 1,
    'journal_id': 1,
}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&create_vals=${create_vals}" \
    https://demo8.simetri-sinergi.id/api/res.partner.bank/create
```
