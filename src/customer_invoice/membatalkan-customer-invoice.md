# Membatalkan Customer Invoice

#### Endpoint
```bash
/api/account.invoice/id/method/signal_workflow
```

#### Parameter
- **token:** API token</br>
- **args:** diisi dengan ['invoice_cancel']</br>

#### Contoh

```bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&args=['invoice_cancel']" \
    https://demo8.simetri-sinergi.id/api/account.invoice/3/method/signal_workflow
```

