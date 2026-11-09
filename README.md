# SpamScam

Tool buat ngebombing OTP ke beberapa provider pinjol sekaligus. Tiap siklus ngirim request ke semua provider, terus nunggu cooldown 62 detik sebelum lanjut ke siklus berikutnya.

## Provider yang tersedia

- AdaKami
- Indosaku
- KrediOne
- RupiahCepat
- KreditNavigator

## Cara pakai

Install dulu dependensinya:

```
pip install -r requirements.txt
```

Jalankan:

```
python main.py
```

Nanti bakal diminta input nomor HP target dan berapa kali mau diresend. Masukkan nomor dengan format `08xxxxxxxxxx`.

## Struktur proyek

```
smsOtp/
├── main.py
├── requirements.txt
└── provider/
    ├── __init__.py
    ├── adakami_provider.py
    ├── indosaku_provider.py
    ├── kredione_provider.py
    ├── rc_provider.py
    └── kreditnavigator_provider.py
```

Kalau mau nambahin provider baru, tinggal buat file baru di folder `provider/` dengan fungsi `send_otp(mobile: str) -> bool`, terus daftarin di `provider/__init__.py` dan `main.py`.
