# Command Eksekusi (PowerShell)

Berikut adalah perintah `curl.exe` yang dieksekusi melalui Windows PowerShell untuk berinteraksi dengan API lokal di `http://localhost:8088`.

### 1. GET Daftar Produk
```
curl.exe -i -X GET "http://localhost:8088/api/products"
```

### 2. GET Detail Produk (ID: 1)

```
curl.exe -i -X GET "http://localhost:8088/api/products/1"
```

### 3. POST Tambah Produk Pertama
Catatan: Menggunakan escape string (\") agar payload JSON tidak terpotong oleh PowerShell.
```
curl.exe -i -X POST "http://localhost:8088/api/products" -H "Content-Type: application/json" -d '{\"name\": \"Smart Sensor\", \"category\": \"iot\", \"price\": 175000, \"stock\": 12}'
```

### 4. POST Tambah Produk Kedua
```
curl.exe -i -X POST "http://localhost:8088/api/products" -H "Content-Type: application/json" -d '{\"name\": \"Microcontroller NodeMCU\", \"category\": \"iot\", \"price\": 65000, \"stock\": 25}'
```
