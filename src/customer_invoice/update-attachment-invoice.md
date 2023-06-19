# Mengupdate Data Attachment Berdasarkan ID Invoice
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/update_data.md)

#### Parameter
| Key            | Type    | Description                               |
| :---           | :---    | :---                                      |
| token          | string  | Isi dengan token                          |
| update_vals    | string  | Update Value. Penjelasan ada dibawah      |

- Penjelasan isi dictionary dari <b>update_vals:</b> </br>

| Key            | Type    | Description                               |
| :---           | :---    | :---                                      |
| name           | string  | Nama Attachment                           |
| type           | string  | Isi dengan "binary"                       |
| datas          | string  | Binary File                               |
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

with open("/home/ubuntu/Documents/test.csv", "rb") as binary_file:
    file_data = binary_file.read()
    datas = base64.b64encode(file_data)

vals = {
    "name": "update_data_invoice.csv",
    "type": "binary",
    "datas": datas,
    "datas_fname": "test.csv",
}

params = {
    "token": token,
    "update_vals": str(vals),
}

# FORMAT API = /api/ir.attachment/update/{id_attachment}

response = requests.get("http://localhost:8069/api/ir.attachment/update/441", params=params)
json_data = response.json()
print (response.content)
```
> <b><i>Note:</i></b>
>> <b>id_attachment</b> diatas didapat dari proses [Mengupdate Data Attachment Berdasarkan ID Invoice](mencari-attachment-invoice.md)
