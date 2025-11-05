# AES-256-CBC-Crypto

Aplikasi enkripsi dan dekripsi file yang aman menggunakan algoritma **AES-256 CBC** dengan key derivation PBKDF2-HMAC-SHA256. **Tidak perlu instalasi - langsung jalankan di Google Colab dengan satu klik!**

<div align="center">

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1F_ZvKED_W_Eqi-KSuLxfJp-8vJ-aH8Wq?usp=sharing)

**Klik tombol di atas untuk membuka di Google Colab**

</div>

---

## 🚀 Quick Start

### Opsi 1: Buka Link Google Colab di icon diatas

**Langkah:**
1. Klik link Colab di atas
2. Runtime → Run all (atau tekan Ctrl+F9)
3. Pilih menu 1-4 dan ikuti instruksi
4. File hasil otomatis tersimpan di collab storage

## 🎯 Fitur Utama

### ✅ Enkripsi & Dekripsi Teks
- Input teks langsung → otomatis save ke file JSON
- Upload JSON → dekripsi → otomatis simpan file TXT

### ✅ Enkripsi & Dekripsi File
- Upload file apapun (txt, csv, pdf, docx, etc)
- Metadata menyimpan nama file original
- Dekripsi → file kembali ke format asli
- Support hingga 1 MB

### ✅ Keamanan Enterprise-Grade
- AES-256 (standar militer & bank)
- CBC mode mencegah pola
- PBKDF2 100k iterasi
- Random IV & Salt setiap enkripsi

---

## 🔐 Spesifikasi Teknis

### Algoritma Enkripsi

| Komponen | Spesifikasi |
|----------|-------------|
| **Algoritma** | AES-256 (Advanced Encryption Standard) |
| **Mode** | CBC (Cipher Block Chaining) |
| **Key Size** | 256-bit (32 bytes) |
| **Block Size** | 128-bit (16 bytes) |
| **Ronde** | 14 ronde enkripsi |

### Key Derivation

| Komponen | Spesifikasi |
|----------|-------------|
| **Algoritma** | PBKDF2-HMAC-SHA256 |
| **Iterasi** | 100,000 iterasi |
| **Hash** | SHA-256 |
| **Output** | 256-bit key |
| **Salt** | 128-bit random |

---

## 📝 Cara Penggunaan

**Step 1: Buka di Colab**
- [Klik tombol "Open in Colab" di atas]
- Atau kunjungi link: [crypto_app.ipynb di Colab](https://colab.research.google.com/drive/1F_ZvKED_W_Eqi-KSuLxfJp-8vJ-aH8Wq?usp=sharing)

**Step 2: Run All Cells**
- Pilih **Runtime** → **Run all**
- Atau tekan **Ctrl+F9**
- Tunggu semua cell selesai dijalankan

**Step 3: Gunakan Aplikasi**
```

========== MENU UTAMA ==========

1. Enkripsi Teks
2. Dekripsi Teks
3. Enkripsi File
4. Dekripsi File
5. Keluar

Pilih (0-4): 1

```

**Step 4: Follow Instructions**
- Input sesuai prompts
- File hasil otomatis terdownload
- Selesai! 🎉

---

## 📚 Contoh Penggunaan

### Menu 1: Enkripsi Teks

```

Pilih (0-4): 1
Teks yang akan dienkripsi: Rahasia dari Data Science!
Password: 1234

✓ BERHASIL DIENKRIPSI!
File tersimpan: encrypted_text_20251103_134500.json

```

**File yang dihasilkan: `encrypted_text_20251103_134500.json`**
```

{
"ciphertext": "rB2kJvN5xP8mQ3pL9oW2vA+1bC4dE7fG8...",
"iv": "xY9pZ2aB5cD8eF1gH4iJ7kL0mN3oP6qR9sT2uV5wX8",
"salt": "7mK0pL3qR6sT9uV2wX5yZ8aC1bD4eF7gH0iJ3kL6mN9"
}

```

---

### Menu 2: Dekripsi Teks

```

Pilih (0-4): 2

📤 Upload file JSON hasil enkripsi...
[Pilih file encrypted_text_20251103_134500.json]

Password: 1234

✓ BERHASIL DIDEKRIPSI!
File tersimpan: decrypted_text_20251103_134600.txt

Hasil dekripsi:
Rahasia dari Data Science!

```

---

### Menu 3: Enkripsi File

```

Pilih (0-4): 3

📤 Upload file yang akan dienkripsi...
[Pilih file data.csv atau dokumen apapun]

Password: 1234

⏳ Mengenkripsi...
✓ FILE BERHASIL DIENKRIPSI!
File input: data.csv
File output: data.csv_encrypted.json

📥 File otomatis disave!

```

---

### Menu 4: Dekripsi File

```

Pilih (0-4): 4

📤 Upload file JSON terenkripsi...
[Pilih file data.csv_encrypted.json]

Password: 1234

⏳ Mendekripsi...
✓ FILE BERHASIL DIDEKRIPSI!
File output: decrypted_data.csv

📥 File otomatis disave!

```

---

## 🔒 Keamanan

### Algoritma Aman
- **AES-256**: Standar enkripsi Pentagon USA, Bank Dunia, EU
- **PBKDF2**: Password Key Derivation Function standard NIST
- **CBC Mode**: Cipher Block Chaining mencegah pola
- **Random IV/Salt**: Berbeda setiap enkripsi

---

### Workflow Data Science
```

Raw Data (data.csv)
↓
Enkripsi (data.csv_encrypted.json)
↓
Upload ke Cloud/Drive Aman
↓
Download \& Dekripsi saat dibutuhkan

```

---

## 📁 File Structure

```

aes256-cbc-crypto/
├── README.md                                                 \# Dokumentasi ini
├── Tugas_Kriptografi_Fauzan_Ahsanudin_Alfikri.ipynb          \# Main notebook untuk Colab ⭐
├── Flowchart aplikasi crypto.png                             \# flowchart
├── pseudocode.txt
└── example.csv                                               \# contoh file csv

```

---

### Referensi Teknis:
1. NIST FIPS 197 - Advanced Encryption Standard
2. NIST SP 800-38A - Block Cipher Modes of Operation
3. RFC 8018 - PBKDF2: Password-Based Key Derivation Function
4. Cryptography.io Documentation

---
