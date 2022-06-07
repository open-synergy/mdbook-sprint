# Membuat Kontak

#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/create_data.md)

#### Parameter
- ***model:***res.partner
- ***create_vals:***

| Key           | Type          | Description                                                                       |
| :---          | :---          | :---                                                                              |
| name          | varchar       | Nama klien. Wajib diisi                                                           |
| parent_id     | integer       | ID database dari partner utama                                                    |
| customer      | boolean       | Diisi dengan **True**. Wajib diisi.                                               |
| is_company    | boolean       | Diisi dengan **False**. Wajib diisi.                                               |
| street        | varchar       | Jalan                                                                             |
| street2       | varchar       | Jalan (baris ke-2)                                                                |
| zip           | varchar       | Kode pos                                                                          |
| city          | varchar       | Kota/Kabupaten/Kota Madya                                                         |
| state_id      | integer       | ID database dari propinsi                                                         |
| country_id    | integer       | ID database dari negara                                                           |
| email         | varchar       | Email                                                                             |
| phone         | varchar       | Nomor telepon                                                                     |
| mobil         | varchar       | Nomor handphone                                                                     |
| function      | varchar       | Jabatan

#### Contoh
```bash
create_vals="{
    'name': 'Andhitia Rama',
    'parent_id': 3,
    'customer': True,
    'is_company': False,
    'street': 'vOffice East. Jl. Raya Perserikatan No. 1 Blok A Kav 261',
    'steet2': 'RT 002 RW 008 Kec. Rawamangun Kel. Pulogadung',
    'city': 'Jakarta Timur',
    'zip': '13220',
    'state_id': 60,
    'country_id': 101,
    'email': 'you@example.com',
    'phone': '+62219237483',
    'mobile': '+628882000014',
    'function': 'Konsultan',

}"
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&create_vals=${create_vals}" \
    https://demo8.simetri-sinergi.id/api/res.partner/create
```
