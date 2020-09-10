# Update Data
#### Endpoint
```
/api/<string:model>/update/<int:id>
```
#### Parameters
| Parameter   | Mandatory     | Description                                             | Type         |
| :---        | :---          | :---                                                    | :---         |
| token       | yes           | Token user                                              | string       |
| update_vals | yes           | Value yang akan di-<i>update</i>                        | dictionary   |

#### Output
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&update_vals={'name': 'Update Data Partner Demo #1'}" \
    https://demo8.simetri-sinergi.id/api/res.partner/update/28
`````
````json
{"success": "Record Updated Successfully"}
````
