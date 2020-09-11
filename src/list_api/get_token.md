# Get Token
#### Endpoint
```bash
/api/user/get_token
```

#### Parameters
| Parameter | Mandatory     | Description                          | Type               |
| :---      | :---          | :---                                 | :---               |
| login     | yes           | Login User                           | string             |
| password  | yes           | Password user                        | string             |

#### Output
````bash
curl -i -d "login=test_user&password=test_password" \
    https://demo8.simetri-sinergi.id/api/user/get_token
`````
````bash
{"token": "858a5f372ea04cb7aad222fb6ba95f76"}
````
