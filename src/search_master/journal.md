# Mencari ID Journal
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/search_data.md)

#### Parameter
- <b>model:</b> account.journal</br>
- <b>domain:</b> [('code', '=', <kode_jurnal>)]</br>
<b>kode_akun</b> = Kode Jurnal

#### Contoh
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&domain=[('code', '=', 'BNK01')]" \
    https://demo8.simetri-sinergi.id/api/account.journal/search
````
