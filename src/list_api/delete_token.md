# Delete Token
#### Endpoint
```bash
/api/user/delete_token
```

#### Parameters
| Parameter | Mandatory     | Description                          | Type               |
| :---      | :---          | :---                                 | :---               |
| token     | yes           | Token user                           | string             |

#### Output
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76" \
    https://demo8.simetri-sinergi.id/api/user/delete_token
`````
````bash
{"success": "Token 858a5f372ea04cb7aad222fb6ba95f76 Deleted Successfully"}
````
