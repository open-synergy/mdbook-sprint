# Mencari ID Reimbursment Type
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/search_data.md)

#### Parameter
- <b>model:</b>hr.reimbursement_type</br>
- <b>domain:</b> [('code', '=', <kode_reimbursement_type>)]</br>
<b>code</b> = Kode Reimbursement Type

#### Contoh
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&domain=[('code', '=', 'REI01')]" \
    https://demo8.simetri-sinergi.id/api/hr.reimbursement_type/search
````
