# Mencari ID Bank
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/search_data.md)

#### Mencari ID Bank Berdasarkan Nama
#### Parameter
- <b>model:</b> res.bank</br>
- <b>domain:</b> [('acc_number', '=', <nomor_rekening>)]</br>
<b>nama_bank</b> = Nama Bank.

#### Contoh
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&domain=[('acc_number', '=', '9384658743658745')]" \
    https://demo8.simetri-sinergi.id/api/res.bank/search
````

#### Mencari Semua ID Bank
#### Contoh
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76" \
    https://demo8.simetri-sinergi.id/api/res.bank/search
````
