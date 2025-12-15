# Deposify-A25-CS059 
# **Predictive Lead Scoring Portal for Banking Sales**

Selamat datang di repository proyek **Predictive Lead Scoring Portal for Banking Sales**, sebuah solusi end-to-end yang dikembangkan untuk meningkatkan efektivitas proses akuisisi nasabah dalam industri perbankan. Proyek ini merupakan hasil kolaborasi antara tim Machine Learning dan tim REBE (React & Backend), dengan tujuan menyediakan sistem prediksi, pengelolaan leads, serta dashboard performa yang komprehensif bagi Sales dan Admin.

---

## **✨ Overview Proyek**
![Logo](https://raw.githubusercontent.com/Deposify-A25/.github/refs/heads/main/assets/Phone%20Capture-1.jpeg)

Proyek ini menghadirkan sebuah portal terpadu yang mampu membantu bank dalam menentukan prioritas nasabah (leads) melalui pendekatan *predictive analytics*. Sistem dilengkapi dengan fitur manajemen Sales, manajemen nasabah, serta pemantauan performa berbasis dashboard interaktif.

Aplikasi ini dibangun dengan dua peran utama:

* **Admin**  
* **Sales**

Masing-masing memiliki fungsionalitas yang dirancang secara spesifik untuk mendukung alur kerja harian mereka dengan lebih efisien, terarah, dan berbasis data.

---

## **👥 Tim Kami**

Tim kami terdiri dari enam anggota yang berasal dari dua learning path. Divisi Machine Learning bertanggung jawab mengembangkan model prediksi nasabah yang berpotensi membuka rekening deposito, menggunakan algoritma XGBoost yang telah melalui proses hyperparameter tuning. Sementara itu, divisi React Back End bertugas membangun portal dashboard untuk tim sales, yang menyajikan daftar prioritas nasabah secara informatif dan mudah diakses.

| **Nama** | **Cohort ID** | **Path** | **Social Media** |
| --- | --- | --- | --- |
| Mohammad Fajar Ma'shum | M891D5Y1140 | Machine Learning, Project Manager | [LinkedIn](https://www.linkedin.com/in/mohammadfajarmashum/) |
| Amellia Dwi Maharani |  M891D5X0188 | Machine Learning | [LinkedIn](https://www.linkedin.com/in/amelliadwimaharani/) |
| Arfizan Rabbani |  M007D5Y0263  | Machine Learning | [LinkedIn](https://www.linkedin.com/in/arfizan-rabbani/) |
| Renaldi Saputra | R891D5Y1679 | React & Back-End with AI | [LinkedIn](https://www.linkedin.com/in/renaldiisptr/) |
| As Ari Firmansyah | R891D5Y0296 |  React & Back-End with AI | [LinkedIn](https://www.linkedin.com/in/asari-firmansyah-548832319/) |
| Nabil Amar Abiyyi | R518D5Y1419  |  React & Back-End with AI | [LinkedIn](https://www.linkedin.com/in/nabil-amar-abiyyi-101125304/) |

---

## **💡 Fitur Utama**

### **🔹 Fitur untuk Sales**

* Menampilkan daftar nasabah yang telah di-assign beserta prioritasnya.  
* Melakukan **follow-up** langsung melalui dashboard.  
* Melihat **detail profil nasabah** dan **riwayat follow-up** sebelumnya.  
* Menjadwalkan **follow-up lanjutan** untuk memastikan interaksi yang konsisten.  
* Melakukan **konversi nasabah** apabila terjadi deposit.  
* Mengakses **statistik performa pribadi**, seperti jumlah follow-up dan tingkat konversi.

---

### **🔹 Fitur untuk Admin**

* Mengakses log aktivitas Sales secara menyeluruh.  
* Melihat total nasabah, Sales aktif, conversion rate, serta total konversi sistem.  
* Melihat **Top 5 Sales with Most Successful Conversions** yang dapat difilter per bulan dan tahun.  
* Menambah, mengedit, dan menonaktifkan akun Sales.  
* Mengimpor data nasabah melalui **CSV/Excel** untuk efisiensi input.  
* Melakukan assignment atau reassignment nasabah ke Sales dalam jumlah banyak.  
* Mengakses halaman **analytics** berisi:  
  * Total revenue  
  * Rata-rata deposit  
  * Total nasabah yang melakukan deposit  
  * Rata-rata durasi

---

## **🤖 Machine Learning Model**

Tim Machine Learning mengoptimalkan performa prediksi menggunakan tiga model utama:

* **XGBoost**  
* **Random Forest**  
* **Decision Tree**

Model-model tersebut dipilih karena performanya yang unggul pada data tabular perbankan serta kemampuannya menangani kompleksitas fitur. Model kemudian dideploy menggunakan **FastAPI**, menyediakan REST API yang cepat, ringan, dan scalable.

---

## **🛠️ Teknologi yang Digunakan**

### **Frontend**

* React / Next js  
* Typescript  
* TailwindCSS / Shadcn UI  
* React Router / Tanstack Router  
* ZOD / React Hook Form  
* Axios  
* Zustand  
* Eslint

### **Backend**

* Node.js / Express  
* FastAPI (untuk ML deployment)  
* PostgreSQL  
* Prisma ORM  
* ioRedis  
* Winston  
* Helmet  
* Axios  
* Bcrypt  
* Morgan  
* Xlsx  
* Node-cron  
* Multer  
* Jsonwebtoken  
* Joi  
* Eslint

### **Machine Learning**

* Python  
* Scikit-Learn  
* XGBoost  
* Pandas / NumPy

## **💾 Repository**

### **Machine Learning**

- [Model & API](https://drive.google.com/file/d/17RohNZ1soFrFmvUBO5MyLf2hK6xyAWfC/view?usp=sharing) Notebook of our model

## **Documentation**
### **Machine Learing**
**Link: (https://github.com/Deposify-A25/.github/blob/main/profile/ml-readme.md)**
### **Backend Developer**
**Link: (https://github.com/Deposify-A25/.github/blob/main/profile/backend-readme.md)**
### **Frontend Developer**
**Link: (https://github.com/Deposify-A25/.github/blob/main/profile/frontend-readme.md)**
