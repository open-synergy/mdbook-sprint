# Menambahkan Attachment Pada Customer Invoice
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
| res_model         | string                   | diisi dengan **account.invoice**                                               |
| res_id            | integer                  | ID customer invoice                                                            |

#### Contoh
```bash
import requests
import base64

params = {
    "login": "admin",
    "password": "admin"
}

response = requests.get("https://localhost:8069/api/user/get_token?", params=params)
json_data = response.json()
token = json_data["token"]

vals = {
    "name": "invoice.pdf",
    "type": "binary",
    "datas_fname": "create_data_invoice.pdf",
    "res_model": "res.partner",
    "res_id": 6,
}

params = {
    "token": token,
    "create_vals": str(vals),
}

f = open("/home/ubuntu/Documents/create_data_invoice.pdf", 'rb')
files = {"file": f}

response = requests.get("https://localhost:8069/api/attachment/create?", files=files, params=params)
print (response.content)
```
