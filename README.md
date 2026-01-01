# Hi there 👋

## ⏱️ Weekly Development Breakdown

<!--START_SECTION:waka-->
<!--END_SECTION:waka-->

---

## 🔥 Tutorial: WakaTime Stats Auto-Update di GitHub README

### Hasil Akhir
Stats akan otomatis update seperti ini:
```
C        714 hrs 33 mins  ████████████░░░░░░░░░ 18.97 %
Python   589 hrs 55 mins  ██████████░░░░░░░░░░  15.66 %
Assembly 479 hrs 58 mins  █████████░░░░░░░░░░░ 12.75 %
C++      402 hrs 41 mins  ████████░░░░░░░░░░░░ 10.69 %
Other    323 hrs 13 mins  ██████░░░░░░░░░░░░░░ 08.58 %
```

---

### 1️⃣ Buat Akun WakaTime

1. Buka 👉 [https://wakatime.com](https://wakatime.com)
2. Sign up (pakai GitHub / email)
3. Masuk ke **Settings** → **API Key**
4. Copy API Key 🔑

---

### 2️⃣ Install WakaTime di Editor

Pilih sesuai editor yang kamu pakai:

- **VS Code** → Install extension WakaTime
- **JetBrains** → Plugin WakaTime
- **Vim / Neovim / Sublime** → tersedia semua

📌 **Setelah install** → login pakai API Key tadi  
📌 **Coding seperti biasa** → waktu akan otomatis tercatat

---

### 3️⃣ Siapkan Repo Profile GitHub

**Nama repo HARUS sama dengan username GitHub kamu**

Contoh:
- Username: `slowy07`
- Repo: `slowy07`

Di dalam repo itu harus ada: `README.md`

---

### 4️⃣ Tambahkan Placeholder di README.md

Tempel kode ini di README.md kamu:

```markdown
## ⏱️ Weekly Development Breakdown

<!--START_SECTION:waka-->
<!--END_SECTION:waka-->
```

📌 **Jangan diubah** teks `START_SECTION` & `END_SECTION`

---

### 5️⃣ Aktifkan GitHub Action (AUTO UPDATE)

Di repo profile kamu:

1. Buat folder: `.github/workflows/`
2. Buat file: `waka-readme.yml`
3. Isi dengan kode ini:

```yaml
name: Waka Readme

on:
  schedule:
    - cron: "0 0 * * *" # update tiap hari
  workflow_dispatch:

jobs:
  update-readme:
    name: Update WakaTime stats
    runs-on: ubuntu-latest
    steps:
      - uses: athul/waka-readme@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          SHOW_TIME: true
          SHOW_TOTAL: true
          BLOCKS: ░▒▓█
```

---

### 6️⃣ Simpan API Key sebagai Secret

Di repo profile:

1. **Settings** → **Secrets and variables** → **Actions**
2. Klik **New repository secret**
3. Isi:
   - **Name:** `WAKATIME_API_KEY`
   - **Value:** (paste API key kamu)
4. **Save** ✅

---

### 7️⃣ Jalankan & Tunggu

1. Klik **Actions**
2. Jalankan workflow **Waka Readme**
3. Tunggu ±1–2 menit
4. README akan update otomatis

🎉 **DONE!**

---

## 🔧 Custom (Optional tapi Keren)

Kamu bisa atur:
- Jumlah bahasa ditampilkan
- Bentuk bar
- Weekly / All time
- Hide bahasa tertentu

Contoh tambahan di `waka-readme.yml`:

```yaml
LANG_COUNT: 6
IGNORED_LANGUAGES: YAML JSON
```

---

## 🎯 Tips Biar Kelihatan Profesional

✔ Jangan kebanyakan widget  
✔ Taruh WakaTime di tengah README  
✔ Cocok banget buat:
- Mahasiswa
- Researcher
- Student exchange
- Developer portfolio

---

## 📫 Connect with Me

- GitHub: [@hendrawanwawan](https://github.com/hendrawanwawan)
- WakaTime: Track your coding activity automatically!
