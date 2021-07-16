# Mencari ID Product
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/search_data.md)

#### Parameter
- <b>model:</b> product.product</br>
- <b>domain:</b> [('default_code', '=', <kode_product>)]</br>
<b>kode_akun</b> = Kode Produk

#### Contoh
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&domain=[('default_code', '=', 'R902382')]" \
    https://demo8.simetri-sinergi.id/api/product.product/search
````
