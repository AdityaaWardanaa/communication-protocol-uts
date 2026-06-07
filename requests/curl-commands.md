# Command Eksekusi (PowerShell)

Berikut adalah perintah `curl.exe` yang dieksekusi melalui Windows PowerShell untuk berinteraksi dengan API lokal di `http://localhost:8088`.

### 1. GET Daftar Produk
```powershell
curl.exe -i -X GET "http://localhost:8088/api/products"
