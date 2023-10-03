# Attach Dokumen Pada Reimbursement
#### Endpoint
```bash
/api/attachment/create
```

#### Parameter
- **token:** API token</br>
- **file:** File Attachment
- **create_vals:**

| Key               | Type                     | Description                                                                    |
| :---              | :---                     | :---                                                                           |
| datas_fname       | string                   | nama file yang akan diattach                                                   |
| name              | base64                   | nama attachment. Boleh sama dengan datas_fname                                 |
| type              | string                   | diisi dengan **binary**                                                        |
| res_model         | string                   | diisi dengan **hr.reimbursement**                                              |
| res_id            | integer                  | ID Reimbursement                                                               |

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

vals = {
    "name": "attachment.png",
    "type": "binary",
    "datas_fname": "data1.png",
    "res_model": "hr.reimbursement",
    "res_id": 8,
}

params = {
    "token": token,
    "create_vals": str(vals),
}

f = open("/home/ubuntu/Documents/data1.png", 'rb')
files = {"file": f}

response = requests.get("http://localhost:8069/api/attachment/create?", files=files, params=params)
print (response.content)
```
