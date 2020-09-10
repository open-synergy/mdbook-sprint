# Mencari ID Account
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/search_data.md)

#### Parameter
- <b>model:</b> account.account</br>
- <b>domain:</b> [('code', '=', <kode_akun>)]</br>
<b>kode_akun</b> = kode akun yang terdaftar pada aplikasi yang akan menjalankan API Odoo.

#### Contoh
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&domain=[('code', '=', '01.01.01')]" \
    https://demo8.simetri-sinergi.id/api/account.account/search
````
