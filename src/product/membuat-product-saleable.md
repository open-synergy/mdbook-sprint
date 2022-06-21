# Membuat Product Saleable
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/create_data.md)

#### Parameter
- <b>model:</b>product.product</br>
- <b>create_vals:</b> </br>

| Key                                          | Type                     | Description                                                                                                   |
| :---                                         | :---                     | :---                                                                                                          |
| name                                         | string                   | Nama layanan
| type                                         | string                   | Diisi dengan **service**
| default_code                                 | string                   | Diisi dengan kode layanan
| sale_ok                                      | boolean                  | Diisi dengan **True**
| purchase_ok                                  | boolean                  | Diisi dengan **False**
| uom_id                                       | integer                  | Diisi dengan **1**
| uom_po_id                                    | integer                  | Diisi dengan **1**
| categ_id                                     | integer                  | Diisi dengan **2**
| property_account_income                      | integer                  | Diisi dengan ID Database dari data akun


#### Contoh
```bash
create_vals="{
    'name': 'APM',
    'type': 'service',
    'default_code': 'A101',
    'sale_ok': true,
    'purchase_ok': true,
    'uom_id': 1,
    'uom_po_id': 1,
    'categ_id': 2,
    'property_account_income': 1072,

}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&create_vals=${create_vals}" \
    https://demo8.simetri-sinergi.id/api/product.product/create
```

