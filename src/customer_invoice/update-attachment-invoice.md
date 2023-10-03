# Mengupdate Data Attachment Berdasarkan ID Invoice
#### Endpoint
```bash
/api/attachment/update
```

#### Parameter
| Key            | Type    | Description                               |
| :---           | :---    | :---                                      |
| token          | string  | Isi dengan token                          |
| file           | string  | File Attachment                           |
| update_vals    | string  | Update Value. Penjelasan ada dibawah      |

- Penjelasan isi dictionary dari <b>update_vals:</b> </br>

| Key            | Type    | Description                               |
| :---           | :---    | :---                                      |
| name           | string  | Nama Attachment                           |
| type           | string  | Isi dengan "binary"                       |
| datas_fname    | string  | Nama Original File                        |

#### Contoh
```bash
import requests
import base64

params = {
    "login": "admin",
    "password": "admin"
}
response = requests.get("http://localhost:8069/api/user/get_token?", params=params)
json_data = response.json()
token = json_data["token"]

f = open("/home/ubuntu/Documents/test.csv", 'rb')
files = {"file": f}

vals = {
    "name": "update_data_invoice.csv",
    "type": "binary",
    "datas_fname": "test.csv",
}

params = {
    "token": token,
    "update_vals": str(vals),
}

response = requests.get("http://localhost:8069/api/attachment/update/441",files=files, params=params)
print (response.content)
```
> <b><i>Note:</i></b>
>> <b>id_attachment</b> diatas didapat dari proses [Mengupdate Data Attachment Berdasarkan ID Invoice](mencari-attachment-invoice.md)
