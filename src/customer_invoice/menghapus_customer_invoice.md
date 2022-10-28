# Menghapus Customer Invoice
#### Endpoint
```bash
 /api/<string:model>/unlink/<int:id>
```

#### Parameter
- **model:** Diisi dengan *account.invoice*
- **id:** ID customer invoice yang akan dihapus

#### Contoh

curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76" \
    https://demo8.simetri-sinergi.id/api/account.invoice/unlink/3
