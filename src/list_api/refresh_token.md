# Refresh Token
#### Endpoint
```bash
/api/user/refresh_token
```

#### Parameters
| Parameter | Mandatory     | Description                          | Type               |
| :---      | :---          | :---                                 | :---               |
| token     | yes           | Token user                           | string             |

#### Output
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76" \
    https://demo8.simetri-sinergi.id/api/user/refresh_token
`````
````bash
{"token": "d69376c3145041998d1b95650751fe32"}
````
