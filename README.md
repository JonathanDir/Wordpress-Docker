# WordPress Docker Project



## Cara Menjalankan
docker compose up -d

## Akses
http://localhost:8000

## Container
- wordpress
- mysql
- redis

## Test Redis
docker exec -it redis_cache redis-cli
ping

## Dokumentasi
Gambar 1. Halaman Dashboard WordPress
Gambar 2. Instalasi WordPress
Gambar 3. Docker Container Running & Redis CLI Ping Test

## Pertanyaan
1. Kenapa perlu volume untuk MySQL?
=> Agar data database tidak hilang saat container dihapus/restart.

2. Apa fungsi depends_on?
Mengatur urutan startup container dan WordPress menunggu MySQL aktif dulu.

3. Bagaimana WordPress connect ke MySQL?
Lewat network Docker internal menggunakan hostname : mysql (karena nama service mysql).

4. Keuntungan Redis untuk WordPress?
- Website lebih cepat
- Mengurangi query database
- Cache object/data sementara
