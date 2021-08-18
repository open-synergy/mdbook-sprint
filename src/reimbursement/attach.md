# Attach Dokumen Pada Reimbursement
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/create_data.md)

#### Parameter
- <b>model:</b>hr.reimbursement</br>
- <b>create_vals:</b> </br>

| Key            | Type    | Description                                                                                            |
| :---           | :---    | :---                                                                                                   |
| name           | string  | Isi dengan nama file attachment disertakan dengan extension filenya, cth: png,txt,jpeg                 |
| type           | string  | Isi dengan "<b>binary</b>"                                                                             |
| datas          | base64  | File attachment yang sudah dikonversi menjadi format base64                                            |
| datas_fname    | string  | Nama harus sesuai dengan file yang hendak diupload                                                     |
| res_model      | string  | Isikan dengan "<b>hr.reimbursement</b>"                                                                |
| res_id         | integer | ID Reimbursement yang ingin dilampirkan attachment                                                     |

> <b><i>Note:</i></b> File Extension antara <b>name</b> dan <b>datas_fname</b> harus sama

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

datas = open("/home/ubuntu/Documents/data1.png", 'rb').read().encode('base64')


vals = {
    "name": "attachment.png",
    "type": "binary",
    "datas": datas,
    "datas_fname": "data1.png",
    "res_model": "hr.reimbursement",
    "res_id": 8,
}

params = {
    "token": token,
    "create_vals": str(vals),
}

response = requests.get("http://localhost:8069/api/ir.attachment/create?", params=params)
print (response.content)
```
