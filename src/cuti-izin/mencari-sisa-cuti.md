# Mencari Sisa Cuti

#### Endpoint
```bash
/api/hr.employee/{id}/method/_get_available_leave_allocation/
```

#### Parameters


| Parameter   | Mandatory | Description                          | Type         |
| :--------   | :-------- | :----------                          | :----------- |
| token       | yes       | Token user                           | string       |
| kwargs      | yes       | keyword argument                     | dictionary   |



#### args


| Key               | Type                     | Description                                                                            |
| :---              | :---                     | :---                                                                                   |
| leave_type_id     | integer                  | Database ID Jenis Cuti/Izin

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

### Contoh

Mencari jatah **cuti tahunan** untuk karyawan dengan database ID **2**

```bash
/api/hr.employee/2/method/_get_available_leave_allocation/?
	token=1ec448c54a004165b4c0da976b227260&kwargs={'leave_type_id':27}
```
