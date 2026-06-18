# WordPress Cloud Project

## Deskripsi

Project ini dibuat untuk memenuhi tugas mata kuliah Cloud Computing. Sistem dibangun menggunakan Docker Compose dengan beberapa container yang saling terhubung, yaitu WordPress, MySQL, Redis, dan MinIO.

Implementasi ini bertujuan untuk memahami konsep deployment aplikasi berbasis container, optimasi performa menggunakan caching, serta pemanfaatan object storage dalam lingkungan cloud.

## Teknologi yang Digunakan

* WordPress
* MySQL 8
* Redis Cache
* MinIO Object Storage
* Docker Compose

## Struktur Layanan

* **WordPress** sebagai CMS utama.
* **MySQL** sebagai database penyimpanan data.
* **Redis** sebagai cache untuk meningkatkan performa aplikasi.
* **MinIO** sebagai object storage untuk penyimpanan file dan media.
* **Docker Compose** untuk mengelola seluruh layanan dalam satu lingkungan.

## Menjalankan Project

### Clone Repository

```bash
git clone https://github.com/ansysuru/wordpress-cloud-project.git
cd wordpress-cloud-project
```

### Membuat File Environment

```bash
cp .env.example .env
```

### Menjalankan Container

```bash
docker compose up -d
```

### Memeriksa Status Container

```bash
docker ps
```

## Akses Layanan

### WordPress

```text
http://localhost:8080
```

### MinIO Console

```text
http://localhost:9001
```

## Akun MinIO

```text
Username : minioadmin
Password : minioadmin
```

## Milestone 1

* Setup repository GitHub.
* Membuat konfigurasi Docker Compose.
* Deployment WordPress dan MySQL menggunakan container.
* Pengujian akses WordPress melalui browser.

## Milestone 2

* Integrasi Redis Cache dengan WordPress.
* Integrasi MinIO sebagai Object Storage.
* Pengujian layanan Redis dan MinIO.
* Upload file media pada bucket object storage.
* Dokumentasi hasil implementasi dan commit ke GitHub.

## Hasil Implementasi

Pada Milestone 2, Redis berhasil diintegrasikan dengan WordPress menggunakan Redis Object Cache. Selain itu, MinIO berhasil dijalankan sebagai object storage dan digunakan untuk menyimpan file hasil pengujian. Seluruh container dapat berjalan dengan baik menggunakan Docker Compose.

## Dokumentasi

Screenshot proses pengerjaan dan hasil implementasi disimpan pada folder:

```text
screenshots/
```

## Repository

https://github.com/ansysuru/wordpress-cloud-project
