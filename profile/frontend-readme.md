## **Frontend Environment Setup Guide**

Dokumentasi ini menjelaskan langkah-langkah konfigurasi dan menjalankan **Frontend Application** yang berfungsi sebagai antarmuka pengguna dan terintegrasi langsung dengan **Backend API**.

---

## **1\. Prerequisites**

Pastikan sistem telah terpasang:

* **Node.js** (versi LTS direkomendasikan)  
* **npm**  
* Web browser modern (Chrome, Firefox, Edge)

---

## **2\. Environment Configuration**

Frontend menggunakan environment variable untuk menentukan endpoint **Backend API** yang akan diakses oleh aplikasi.

Buat file `.env.local` pada root folder frontend, kemudian isi dengan konfigurasi berikut:

`NEXT_PUBLIC_API_URL="http://localhost:5000/api/v1"`
atau bisa menggunakan backend yang sudah di deploy
`NEXT_PUBLIC_API_URL=https://backend-bank-portal-fork-1m08.onrender.com/api/v1`
**Penjelasan:**

* `NEXT_PUBLIC_API_URL` merupakan base URL backend yang digunakan untuk seluruh request API dari frontend.  
* Prefix `NEXT_PUBLIC_` wajib digunakan agar variabel dapat diakses di sisi client (browser).

**Catatan:**

* Untuk environment production, ganti nilai URL sesuai dengan domain backend yang telah di-deploy.  
* Pastikan endpoint backend aktif sebelum menjalankan frontend.

---

## **3\. Install Dependencies**

Setelah environment variable dikonfigurasi, jalankan perintah berikut:

`npm install`

Perintah ini akan menginstal seluruh dependency yang dibutuhkan oleh frontend application.

---

## **4\. Menjalankan Frontend Application**

Untuk menjalankan aplikasi dalam mode development, gunakan perintah:

`npm run dev`

Aplikasi frontend akan berjalan secara default pada:

`http://localhost:3000`

---

## **5\. Build untuk Production**

Untuk membuat versi production-ready dari frontend, jalankan:

`npm run build`  
`npm start`

Build ini telah dioptimalkan untuk performa dan siap di-deploy ke server atau platform hosting.

---

## **6\. Frontend–Backend Integration Flow**

* Frontend mengirim HTTP request ke backend melalui `NEXT_PUBLIC_API_URL`  
* Backend memproses request, termasuk autentikasi dan integrasi ML  
* Response dikembalikan ke frontend dalam format JSON  
* Frontend menampilkan data secara dinamis kepada pengguna

---

## **7\. Common Issues & Notes**

* Pastikan backend berjalan sebelum frontend diakses.  
* Jika terjadi error CORS, periksa konfigurasi backend.  
* Perubahan pada file `.env.local` mengharuskan restart frontend server.
