# Mencari ID Employee
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/search_data.md)

#### Parameter
- <b>model:</b> hr.employee</br>
- <b>domain:</b> [('code', '=', <kode_karyawan>)]</br>
<b>kode_karyawan</b> = kode karyawan yang terdaftar pada aplikasi yang akan menjalankan API Odoo.

#### Contoh
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&domain=[('code', '=', 'EMP0001')]" \
    https://demo8.simetri-sinergi.id/api/hr.employee/search
````
