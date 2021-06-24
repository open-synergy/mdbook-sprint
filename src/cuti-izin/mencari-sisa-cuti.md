# Mencari Sisa Cuti

#### Endpoint
```bash
/api/hr.holidays.status/{id}/method/get_days/
```

#### Parameters


| Parameter   | Mandatory | Description                          | Type         |
| :--------   | :-------- | :----------                          | :----------- |
| token       | yes       | Token user                           | string       |
| args | yes       | keyword argument     | dictionary   |



#### args


| Key               | Type                     | Description                                                                            |
| :---              | :---                     | :---                                                                                   |
| employee_id              | integer                   | Database ID karyawan

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

### Contoh

Mencari jatah **cuti tahunan** untuk karyawan dengan database ID **2**

```bash
/api/hr.holidays.status/1/method/get_days/?
	token=1ec448c54a004165b4c0da976b227260&args={'employee_id':2}
```
