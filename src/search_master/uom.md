# Mencari ID UOM
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/search_data.md)

#### Parameter
- <b>model:</b> product.uom</br>
- <b>domain:</b> [('name', '=', <nama_satuan>)]</br>
<b>kode_akun</b> = Nama Satuan

#### Contoh
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&domain=[('name', '=', 'Unit(s)')]" \
    https://demo8.simetri-sinergi.id/api/product.uom/search
````
