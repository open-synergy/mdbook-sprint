# Membuat Reimbursement
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/create_data.md)

#### Parameter
- <b>model:</b>hr.reimbursement</br>
- <b>create_vals:</b> </br>

| Key                                          | Type                     | Description                                                                                                   |
| :---                                         | :---                     | :---                                                                                                          |
| employee_id                                  | string                   | ID Employee yang didapat dari [Mencari ID Employee](../search_master/employee.md)                             |
| type_id                                      | integer                  | ID Reimbursement Type yang didapat dari [Mencari Reimbursement Type](../search_master/reimbursement_type.md)  |
| journal_id                                   | integer                  | ID Journal yang didapat dari [Mencari Journal](../search_master/journal.md)                                   |
| employee_reimbursement_payable_account_id    | integer                  | ID Reimbursement Payable Account yang didapat dari [Mencari ID Account](../search_master/account.md)          |
| date_expense                                 | integer                  | Tanggal Reimbursement                                                                                         |
| date_due                                     | integer                  | Tanggal Jatuh Tempo                                                                                           |

- Penjelasan isi dictionary dari <b>line_ids:</b> </br>

| Key                 | Type                           | Description                                                                    |
| :---                | :---                           | :---                                                                           |
| product_id          | integer                        | ID Account yang didapat dari [Mencari ID Account](../search_master/product.md) |
| note                | string                         | Catatan (Opsional)                                                             |
| ref                 | string                         | Referensi (Opsional)                                                           |
| account_id          | integer                        | ID Account yang didapat dari [Mencari ID Account](../search_master/account.md) |
| price_unit          | float                          | Harga satuan                                                                   |
| approve_price_unit  | float                          | Samakan dengan nilai price_unit                                                |
| quantity            | float                          | Kuantitas                                                                      |
| approve_quantity    | float                          | Samakan dengan nilai quantity                                                  |
| uom_id              | integer                        | ID Account yang didapat dari [Mencari ID UOM](../search_master/uom.md)         |

#### Contoh
```bash
create_vals="{
    'employee_id': 1,
    'type_id': 2,
    'journal_id': 49,
    'employee_reimbursement_payable_account_id': 689,
    'date_expense': '2021-01-01',
    'date_due': '2021-01-10',
    'line_ids': [
        (0, 0, {
            'product_id': 10,
            'account_id': 34,
            'price_unit': 1500000.00,
            'approve_price_unit': 1500000.00,
            'quantity': 3,
            'approve_quantity': 3,
            'uom_id': 1,
        }),
        (0, 0, {
            'product_id': 10,
            'note': 'Note #1',
            'ref': 'Ref #1',
            'account_id': 44,
            'price_unit': 32500000.00,
            'approve_price_unit': 32500000.00,
            'quantity': 1,
            'approve_quantity': 1,
            'uom_id': 1,
        }),
    ]
}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&create_vals=${create_vals}" \
    https://demo8.simetri-sinergi.id/api/hr.reimbursement/create
```
