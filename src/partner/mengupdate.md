# Mengupdate Partner

#### Endpoint
```bash
/api/res.partner/updata/<<id-partner>>
```


#### Parameter
- **token:** API token</br>
- **update_vals:**

| Key           | Type          | Description                                                                       |
| :---          | :---          | :---                                                                              |
| name          | varchar       | Nama klien. Wajib diisi                                                           |
| customer      | boolean       | Diisi dengan **True**. Wajib diisi.                                               |
| is_customer   | boolean       | Diisi dengan **True**. Wajib diisi.                                               |
| vat           | varchar       | NPWP Klien. Diisi dengan format ***ID*** + NPWP Klien                             |
| street        | varchar       | Jalan                                                                             |
| street2       | varchar       | Jalan (baris ke-2)                                                                |
| zip           | varchar       | Kode pos                                                                          |
| city          | varchar       | Kota/Kabupaten/Kota Madya                                                         |
| state_id      | integer       | ID database dari propinsi                                                         |
| country_id    | integer       | ID database dari negara                                                           |
| country_id    | integer       | ID database dari negara                                                           |
| email         | varchar       | Email
| ref           | varchar       | CustomerID


#### Contoh
```bash
update_vals="{
    'name': 'PT. Simetri Sinergi Indonesia',
    'customer': True,
    'is_company': True,
    'vat': 'ID94.695.791.7-002.000'
    'street': 'vOffice East. Jl. Raya Perserikatan No. 1 Blok A Kav 261',
    'steer2': 'RT 002 RW 008 Kec. Rawamangun Kel. Pulogadung',
    'city': 'Jakarta Timur',
    'zip': '13220',
    'state_id': 60,
    'country_id': 101,
    'email': 'you@example.com',

}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&update_vals=${update_vals}" \
    https://demo8.simetri-sinergi.id/api/res.partner/update/3
```

