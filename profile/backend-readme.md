## **Backend Environment Setup Guide**

Dokumentasi ini menjelaskan langkah-langkah konfigurasi dan menjalankan **Backend Service** yang terintegrasi dengan **PostgreSQL, Redis, dan Machine Learning API**.

---

## **1\. Prerequisites**

Pastikan sistem telah terpasang:

* **Node.js** (versi LTS direkomendasikan)  
* **npm**  
* **Docker**  
* **PostgreSQL**  
* Koneksi internet (jika menggunakan ML API hosted)

---

## **2\. Environment Configuration**

Sebelum menjalankan aplikasi, pengguna **wajib mengisi environment variable** yang digunakan oleh backend.

Buat file `.env` pada root folder backend, kemudian isi dengan konfigurasi berikut:

`# Application Configuration`  
`PORT=5000`  
`NODE_ENV=development`  
`# Database Configuration (PostgreSQL)`  
`DATABASE_URL="postgresql://username:password@host:port/database_name"`
`# Authentication (JWT)`  
`JWT_SECRET="your_jwt_secret_key"`  
`JWT_EXPIRES_IN=24h`  
`# JWT_EXPIRES_IN=3`  
`# Password Hashing`  
`BCRYPT_ROUNDS=10`  
`# Redis Configuration`  
`REDIS_HOST=localhost`  
`REDIS_PORT=6379`  
`REDIS_PASSWORD=""`

`# Health Check (Node Cron)`  
`URL_WEB="http://localhost:5000/api/v1/health"`  
`# Machine Learning API Configuration`  
`# Gunakan konfigurasi berikut jika model ML dijalankan secara lokal`  
`# ML_API_BATCH="http://127.0.0.1:8000/predict/batch"`  
`# ML_API_SINGLE="http://127.0.0.1:8000/predict"`

`# Gunakan konfigurasi berikut jika model ML sudah di-hosting`  
`ML_API_BATCH="https://ml-bank-portal.onrender.com/predict/batch"`  
`ML_API_SINGLE="https://ml-bank-portal.onrender.com/predict"`

**Catatan penting:**

* Pastikan `DATABASE_URL` sesuai dengan konfigurasi PostgreSQL yang digunakan.  
* `JWT_SECRET` harus diisi dengan string yang aman dan tidak dibagikan.  
* Pilih **satu jenis ML API** (local atau hosted), jangan aktifkan keduanya sekaligus.

---

## **3\. Install Dependencies**

Setelah environment berhasil dikonfigurasi, jalankan perintah berikut:

`npm install`

Perintah ini akan menginstal seluruh dependency yang dibutuhkan oleh backend.

---

## **4\. Menjalankan Redis dengan Docker**

Backend menggunakan **Redis** untuk caching dan queue. Jalankan Redis menggunakan Docker dengan perintah berikut:

`docker run -d \`  
  `--name redis-stack \`  
  `-p 6379:6379 \`  
  `-p 8001:8001 \`  
  `redis/redis-stack:latest`

Pastikan container Redis berjalan dengan baik:

`docker ps`

---

## **5\. Menjalankan Backend Server**

Setelah Redis aktif dan dependency terinstal, jalankan backend dengan perintah:

`npm run dev`

atau jika menggunakan mode production:

`npm start`

Backend akan berjalan pada:

`http://localhost:5000`

---

## **6\. Health Check**

Untuk memastikan backend berjalan dengan 정상, akses endpoint berikut:

`GET /api/v1/health`

Jika berhasil, server akan mengembalikan status aplikasi dalam kondisi aktif.

---

## **7\. Integration Notes**

* Backend akan mengirim request ke **Machine Learning API** sesuai konfigurasi `ML_API_SINGLE` dan `ML_API_BATCH`.  
* Redis digunakan untuk meningkatkan performa dan mengurangi beban request berulang.  
* Sistem dirancang modular sehingga ML service dapat diganti tanpa mengubah logic utama backend.
