# WordPress Cloud Project

## Deskripsi

Project ini dibuat untuk memenuhi tugas mata kuliah Cloud Computing. Sistem dibangun menggunakan Docker Compose dengan beberapa container yang saling terhubung, yaitu WordPress, MySQL, Redis, dan MinIO.

## Teknologi yang Digunakan

* WordPress
* MySQL 8
* Redis Cache
* MinIO Object Storage
* Docker Compose

## Struktur Layanan

* WordPress sebagai CMS utama.
* MySQL sebagai database.
* Redis sebagai cache untuk meningkatkan performa.
* MinIO sebagai object storage untuk penyimpanan file.

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

WordPress

```text
http://localhost:8080
```

MinIO Console

```text
http://localhost:9001
```

## Akun MinIO

```text
Username : minioadmin
Password : minioadmin
```

## Milestone 1

* Setup repository GitHub
* Setup Docker Compose
* Deployment WordPress dan MySQL

## Milestone 2

* Integrasi Redis Cache
* Integrasi MinIO Object Storage
* Pengujian performa dan penyimpanan media

## Dokumentasi

Screenshot progress disimpan pada folder:

```text
screenshots/
```

## Repository

https://github.com/ansysuru/wordpress-cloud-project
