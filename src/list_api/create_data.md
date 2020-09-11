# Create Data
#### Endpoint
```bash
/api/<string:model>/create
```
#### Parameters
| Parameter   | Mandatory     | Description                          | Type         |
| :---        | :---          | :---                                 | :---         |
| token       | yes           | Token user                           | string       |
| create_vals | yes           | Value yang akan di-<i>create</i>     | dictionary   |

#### Output
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&create_vals={'name': 'Data Partner Demo #1'}" \
    https://demo8.simetri-sinergi.id/api/res.partner/create
`````
````json
{"id": 28}
````
