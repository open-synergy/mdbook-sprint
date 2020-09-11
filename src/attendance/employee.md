# Mencari ID Employee
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/search_data.md)

#### Parameter
- <b>model:</b> hr.employee</br>
- <b>domain:</b> [('ref', '=', <kode_klien>)]</br>
<b>kode_klien</b> = kode partner yang terdaftar pada aplikasi yang akan menjalankan API Odoo.

#### Contoh
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&domain=[('ref', '=', 'ADM')]" \
    https://demo8.simetri-sinergi.id/api/hr.employee/search
````
