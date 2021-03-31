# Membuat Cuti/Izin

#### Endpoint
```bash
/api/hr.holidays/create
```

#### Parameters


| Parameter   | Mandatory | Description                          | Type         |
| :--------   | :-------- | :----------                          | :----------- |
| token       | yes       | Token user                           | string       |
| create_vals | yes       | Value yang akan di-<i>create</i>     | dictionary   |


#### create_vals


| Key               | Type                     | Description                                                                            |
| :---              | :---                     | :---                                                                                   |
| name              | string                   | Penjelasan lanjutan terkait tujuan cuti/izin                                           |
| employee_id       | integer                  | ID Database karyawan yang akan mengajukan cuti/izin                                    |
| type              | string                   | Isi dengan <b>remove</b>                                                               |
| holiday_status_id | integer                  | ID Database dari jenis izin/cuti                                                       |
| date_from         | datetime                 | Tanggal dan waktu mulai cuti/izin. Format YYYY-MM-DD HH:MM:SS. Dituliskan dalam UTC    |
| date_to           | datetime                 | Tanggal dan waktu selesai cuti/izin. Format YYYY-MM-DD HH:MM:SS. Dituliskan dalam UTC  |

### Return

| Key               | Type                     | Description                                                                            |
| :---              | :---                     | :---                                                                                   |
| id                | intereger                | ID data izin yang akan terbuat                                                         |


### ID Database Jenis Cuti/Izin

* Cuti Tahunan (ID: 1)
* Sakit (ID: 2)
* Ijin - Pernikahan Dalam Kota (ID: 3)
* Cuti Diluar Tanggungan (Tidak Dibayar) (ID: 4)
* Cuti Besar (ID: 5)
* Cuti Haid (ID: 6)
* Cuti Keguguran (ID: 7)
* Cuti Melahirkan (ID: 8)
* Ijin - Pernikahan Anak (ID: 9)
* Ijin - Kelahiran Anak/Istri Keguguran (ID: 10)
* Ijin - Baptis Anak (ID: 11)
* Ijin - Khitanan Anak (ID: 12)
* Ijin - Upacara Potong Gigi (Hindu) (ID: 13)
* Ijin - Perayaan Wisudi (ID: 14)
* Ijin - Hari Raya Galungan (ID: 15)
* Ijin - Merawat Suami/Istri/Anak di RS (ID: 16)
* Ijin - Merawat Orang tua/Mertua di RS (ID: 17)
* Ijin - Meninggal (Suami/Anak/Istri  Dalam Kota) (ID: 18)
* Ijin - Meninggal (Keluarga Langsung Lainnya Dalam Kota) (ID: 19)
* Ijin - Meninggal (Keluarga Luar Kota) (ID: 20)
* Ijin - Meninggal (Kerabat serumah) (ID: 21)
* Ijin - Ibadah Haji (ID: 22)
* Ijin - Musibah Kebakaran/Banjir/Bencana Alam (ID: 23)
* Ijin - Pernikahan Luar Kota (ID: 24)
* Cuti Bersama (ID: 25)
* Ijin Telat (ID: 26)
