
## Importer Data Prakiraan Cuaca BMKG

![Cuaca](https://data.bmkg.go.id/include/assets/img/cuaca.svg)

Script PHP untuk import data prakiraan cuaca dari BMKG, dan ditambahkan ke database MYSQL, sehingga untuk kebutuhan ambil data cuaca bisa langsung query tanpa harus rekues lagi ke server BMKG

Apa yang saya lakukan dengan data ini?

Aplikasi saya bisa mencari wilayah terdekat dari table **t_wilayah**, sehingga cuaca yang ditampilkan sesuai wilayahnya terdekat, di Android saya buat versi SQLITE dan saya query wilayah terdekat dari situ, lalu ambil data cuacanya ke server.

Script ini bisa dijalankan di Browser ataupun di command line, tapi bagusnya di commandline dan gunakan [crontab](https://crontab.guru/#0_3_*_*_*) agar dieksekusi tiap waktu yang ditentukan

Dan ingat, bahwa anda harus memberitahukan jika datanya dari BMKG.

## Instalasi

Copy **config.example.php** menjadi **config.php**
ganti isinya dengan konfigurasi database anda
impor **bmkg.sql** ke database anda
pada file **bmkg.php** di paling bawah, **hapus** bagian **git**
kecuali anda mau host datanya di Github juga

# Pakai langsung?

siapkan url endpoint
```https://bagussatoto.github.io/BMKG-commit/```

dari aplikasi, unduh file wilayah.json
```https://bagussatoto.github.io/BMKG-commit/cuaca/wilayah.json```

Dari json tersebut, kalkulasi lokasi user dengan wilayah terdekat, atau user pilih sendiri.

lalu download cuaca di wilayah yang dipilih berdasarkan kodenya
```https://bagussatoto.github.io/BMKG-commit/cuaca/idWilayah.json```

contoh:
```https://bagussatoto.github.io/BMKG-commit/cuaca/501233.json```

sesuaikan kode cuaca dengan icon di folder icon
```https://bagussatoto.github.io/BMKG-commit/icon/5.png```


# Contoh
cek folder **contoh**
-  [HTML](contoh/html/)
-  [PHP](contoh/php/index.php)


#### Sumber
-  [BMKG](http://data.bmkg.go.id/prakiraan-cuaca/)
-  [ICON](http://www.iconarchive.com/tag/weather)
-  [Medoo](http://www.iconarchive.com/tag/weather)

Silahkan dimanfatkan untuk keperluan anda

Developer 💖 Bagus Budi Satoto
