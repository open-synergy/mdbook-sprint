# Membuat Cuti/Izin

#### Endpoint
```bash
/api/hr.leave/create
```

#### Parameters


| Parameter   | Mandatory | Description                          | Type         |
| :--------   | :-------- | :----------                          | :----------- |
| token       | yes       | Token user                           | string       |
| create_vals | yes       | Value yang akan di-<i>create</i>     | dictionary   |


#### create_vals


| Key               | Type                     | Description                                                                            |
| :---              | :---                     | :---                                                                                   |
| employee_id       | integer                  | ID Database karyawan yang akan mengajukan cuti/izin                                    |
| department_id     | integer                  | ID department karyawan yang akan mengajukan cuti (optional)                            |
| job_id            | integer                  | ID Database jabatan karyawan yang akan mengajukan cuti/izin (optional)                 |
| manager_id        | integer                  | ID Database atasan karyawan yang akan mengajukan cuti/izin (optional)                  |
| type_id           | integer                  | ID Database dari jenis izin/cuti                                                       |
| date_start        | date                     | Tanggal dan waktu mulai cuti/izin. Format YYYY-MM-DD                                   |
| date_end          | date                     | Tanggal dan waktu selesai cuti/izin. Format YYYY-MM-DD                       |


### Return

| Key               | Type                     | Description                                                                            |
| :---              | :---                     | :---                                                                                   |
| id                | intereger                | ID data izin yang akan terbuat                                                         |


### ID Database Jenis Cuti/Izin

* Cuti Tahunan (ID: 27)
* Sakit (ID: 28)
* Ijin - Pernikahan Dalam Kota (ID: 29)
* Cuti Diluar Tanggungan (Tidak Dibayar) (ID: 30)
* Cuti Besar (ID: 31)
* Cuti Haid (ID: 32)
* Cuti Keguguran (ID: 33)
* Cuti Melahirkan (ID: 34)
* Ijin - Pernikahan Anak (ID: 35)
* Ijin - Kelahiran Anak/Istri Keguguran (ID: 36)
* Ijin - Baptis Anak (ID: 37)
* Ijin - Khitanan Anak (ID: 38)
* Ijin - Upacara Potong Gigi (Hindu) (ID: 39)
* Ijin - Perayaan Wisudi (ID: 40)
* Ijin - Hari Raya Galungan (ID: 41)
* Ijin - Merawat Suami/Istri/Anak di RS (ID: 42)
* Ijin - Merawat Orang tua/Mertua di RS (ID: 43)
* Ijin - Meninggal (Suami/Anak/Istri  Dalam Kota) (ID: 44)
* Ijin - Meninggal (Keluarga Langsung Lainnya Dalam Kota) (ID: 45)
* Ijin - Meninggal (Keluarga Luar Kota) (ID: 46)
* Ijin - Meninggal (Kerabat serumah) (ID: 47)
* Ijin - Ibadah Haji (ID: 48)
* Ijin - Musibah Kebakaran/Banjir/Bencana Alam (ID: 49)
* Ijin - Pernikahan Luar Kota (ID: 50)
* Ijin Telat (ID: 52)
* Ijin Pulaang Cepat (ID: 53)
