\========================================================  
Cara Menjalankan Deposit Prediction API (FastAPI Backend)  
\========================================================

1️⃣ Buka Command Prompt / Terminal

2️⃣ Masuk ke folder project yang berisi file berikut:  
    \- main.py  
    \- deposit\_xgb\_model.pkl  
    \- requirements.txt

   Contoh perintah (sesuaikan dengan lokasi folder Anda):  
   cd C:\\Users\\...\\Documents\\final\_api

3️⃣ (Opsional tapi direkomendasikan)  
   Cek Python sudah terinstall:  
   python \--version

4️⃣ Install semua dependencies:  
   pip install \-r requirements.txt

   Jika tidak ada requirements.txt:  
   pip install fastapi uvicorn xgboost scikit-learn numpy pandas joblib

5️⃣ Jalankan API dengan:  
   python main.py

   ATAU dengan uvicorn secara manual:  
   uvicorn main:app \--host 0.0.0.0 \--port 8000 \--reload

6️⃣ Jika berhasil, akan muncul log seperti:  
   Uvicorn running on http://127.0.0.1:8000

7️⃣ Buka browser untuk melihat dokumentasi API:  
   http://127.0.0.1:8000/docs

8️⃣ Tes API melalui Swagger UI  
   \- Pilih POST /predict  
   \- Klik "Try it out"  
   \- Isi JSON sesuai field yang tersedia  
   \- Klik Execute

\-----------------------------------  
Contoh Request JSON ke /predict:  
\-----------------------------------  
{  
  "age": 35,  
  "job": "admin.",  
  "marital": "married",  
  "education": "tertiary",  
  "default": "no",  
  "balance": 1200,  
  "housing": "yes",  
  "loan": "no",  
  "contact": "cellular",  
  "day": 15,  
  "month": "may",  
  "duration": 200,  
  "campaign": 1,  
  "previous": 0,  
  "poutcome": "unknown"  
}

\-----------------------------------  
Respons API akan berbentuk seperti:  
\-----------------------------------  
{  
  "prediction": "yes",  
  "probability\_yes": 0.79  
}

\========================================================  
Jika API ingin dihentikan:  
Tekan CTRL \+ C di terminal  
\========================================================
