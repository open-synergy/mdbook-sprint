# Membuat Absen Masuk
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/create_data.md)

#### Parameter
- <b>model:</b> hr.employee</br>
- <b>create_vals:</b> </br>

| Key           | Type          | Description                                                                       |
| :---          | :---          | :---                                                                              |
| employee_id   | integer       | ID Employee yang didapat dari [Mencari ID Employee](../search_master/employee.md) |
| action        | string        | Isi dengan <b>sign_in</b>                                                         |
| name          | datetime      | Tanggal Absen Masuk                                                               |

#### Contoh
```bash
create_vals="{
    'employee_id': 1,
    'action': 'sign_in',
    'name': '2020-09-09 08:00:00',
}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&create_vals=${create_vals}" \
    https://demo8.simetri-sinergi.id/api/hr.employee/create
```
