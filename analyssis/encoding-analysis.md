# Analisis Encoding Data

Pengujian ini menggunakan format encoding murni **JSON (JavaScript Object Notation)** dengan standar karakter **UTF-8**, dibuktikan oleh parameter header `Content-Type: application/json; charset=utf-8`.

### Rincian Analisis:
1. **Struktur Sintaksis:** Data dikonstruksi menggunakan metode *key-value pairs*. Koleksi data inventaris ditransmisikan dalam bentuk *array of objects* `[]`, sedangkan data entitas tunggal atau payload transmisi dibatasi oleh *curly braces* `{}`. Tipe data diisolasi secara presisi, di mana atribut nama dan kategori menggunakan *String*, sedangkan atribut harga, stok, dan ID menggunakan *Integer*.
2. **Mekanisme Transmisi:** Client melakukan *serialization* terhadap payload JSON menjadi format *string* utuh melalui command line (menggunakan escape karakter `\"` pada Windows PowerShell agar tidak terpotong oleh spasi). Server melakukan *deserialization* untuk membaca string tersebut dan mengonversinya kembali menjadi struktur data valid sebelum menyimpannya ke database.
