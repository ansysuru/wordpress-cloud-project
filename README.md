Siap, aku **hanya betulkan typo & kesalahan kecil tanpa mengubah isi**:

---

# WordPress Cloud Project

## Deskripsi

Project ini dibuat untuk memenuhi tugas mata kuliah Cloud Computing. Sistem dibangun menggunakan Docker Compose dengan beberapa layanan yang berjalan dalam container dan saling terhubung, yaitu WordPress, MySQL, Redis, dan MinIO.

Implementasi ini bertujuan untuk mempelajari deployment aplikasi berbasis container, optimasi performa menggunakan caching, penerapan object storage, serta penerapan best practices keamanan melalui penggunaan file environment (.env).

---

## Teknologi yang Digunakan

* WordPress
* MySQL 8
* Redis Cache
* MinIO Object Storage
* Docker Compose
* Docker Network
* Environment Variables (.env)

---

## Arsitektur Sistem

Layanan yang digunakan dalam project ini:

### WordPress

Berfungsi sebagai Content Management System (CMS) utama yang digunakan untuk mengelola website.

### MySQL

Digunakan sebagai database utama untuk menyimpan data WordPress.

### Redis

Digunakan sebagai cache service untuk meningkatkan performa aplikasi WordPress.

### MinIO

Digunakan sebagai object storage untuk menyimpan file dan media.

### Docker Compose

Digunakan untuk mengelola seluruh container dalam satu konfigurasi.

---

## Struktur Project

```text id="qk3x8c"
wordpress-cloud-project/

├── docker-compose.yml

├── .env

├── README.md

├── notes-kontribusi.txt

└── screenshots/
```

---

## Keamanan Konfigurasi (Milestone 3)

Untuk menerapkan best practices keamanan:

* Seluruh credentials disimpan pada file `.env`.
* Tidak terdapat hardcode password pada file `docker-compose.yml`.
* Konfigurasi database dan object storage menggunakan environment variables.
* Pemisahan konfigurasi aplikasi dan data sensitif dilakukan untuk meningkatkan keamanan deployment.

Contoh penggunaan environment variables:

```
MYSQL_ROOT_PASSWORD=${MYSQL_ROOT_PASSWORD}

MYSQL_PASSWORD=${MYSQL_PASSWORD}

MINIO_ROOT_PASSWORD=${MINIO_ROOT_PASSWORD}
```

---

## Cara Menjalankan Project

### 1. Clone Repository

```bash
git clone https://github.com/ansysuru/wordpress-cloud-project.git
cd wordpress-cloud-project
```

### 2. Membuat File Environment

```bash
cp .env.example .env
```

### 3. Menjalankan Docker Compose

```bash
docker compose up -d
```

### 4. Memeriksa Status Container

```bash
docker ps
```

### 5. Menghentikan Container

```bash
docker compose down
```

---

## Akses Layanan

### WordPress

[http://localhost:8080](http://localhost:8080)

### MinIO Console

[http://localhost:9001](http://localhost:9001)

---

## Akun MinIO

Username: minioadmin
Password: minioadmin

---

## Milestone 1

* Setup repository GitHub.
* Membuat konfigurasi Docker Compose.
* Deployment WordPress dan MySQL menggunakan container.
* Pengujian akses WordPress melalui browser.

---

## Milestone 2

* Integrasi Redis Cache dengan WordPress.
* Integrasi MinIO sebagai Object Storage.
* Pengujian layanan Redis dan MinIO.
* Upload file media pada bucket object storage.
* Dokumentasi hasil implementasi dan commit ke GitHub.

---

## Milestone 3

* Penerapan best practices keamanan menggunakan file .env.
* Penghapusan hardcode credentials pada docker-compose.yml.
* Dokumentasi kontribusi anggota kelompok.
* Pembuatan portofolio pada platform Bisa.ai.
* Finalisasi project untuk pengumpulan.

---

## Hasil Implementasi

Hasil implementasi menunjukkan bahwa seluruh layanan berhasil berjalan menggunakan Docker Compose. Seluruh layanan diuji menggunakan `docker ps`, `docker logs`, serta pengujian akses melalui browser dan CLI (Redis PING → PONG). Hasil pengujian menunjukkan seluruh service berjalan stabil tanpa error.

Container yang berhasil dijalankan:

* WordPress
* MySQL
* Redis
* MinIO

Seluruh layanan dapat saling terhubung dan berfungsi sesuai kebutuhan project.

---

## Kontribusi Anggota

### Anastasia Suru

* Konfigurasi Docker Compose.
* Setup WordPress, MySQL, Redis, dan MinIO.
* Konfigurasi file `.env` dan pengujian sistem.

### Maria Helena Lipat

* Dokumentasi dan screenshot hasil implementasi.
* Membantu pengujian sistem.

### Mariana Mako Pawe

* Portofolio Bisa.ai.
* Membantu pengujian dan finalisasi project.

---

## Dokumentasi

Screenshot proses pengerjaan dan hasil implementasi disimpan pada folder:

```text id="w8m3qv"
screenshots/
├── milestone-1/
├── milestone-2/
└── milestone-3/
```

---

## Repository

[https://github.com/ansysuru/wordpress-cloud-project](https://github.com/ansysuru/wordpress-cloud-project)

---

## Kesimpulan

Project ini berhasil mengimplementasikan arsitektur aplikasi berbasis microservices menggunakan Docker Compose. Integrasi WordPress dengan MySQL, Redis, dan MinIO menunjukkan implementasi konsep cloud-native application, termasuk containerization, service orchestration, caching, dan object storage. Selain itu, penerapan environment variables (.env) meningkatkan aspek keamanan dengan memisahkan konfigurasi sensitif dari source code.

---

