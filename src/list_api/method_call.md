# Method Call
- #### API
<b>Without Arg:</b>

```bash
<host>/api/<str:model_name>/<int:id>/method/<str:method_name>/?token=<str:token>
```

<b>With Arg:</b>

```bash
<host>/api/<str:model_name>/<int:id>/method/<str:method_name>/?token=<str:token>&args=<list:id>
```

<b>With Key Arg:</b>

```bash
<host>/api/<str:model_name>/<int:id>/method/<str:method_name>/?token=<str:token>&kwargs=<dict:value>
```
