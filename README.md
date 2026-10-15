# 99.co Homepage Automation — Rumah123 Automation Challenge

Automation test untuk bagian revamp homepage aplikasi 99.co, menggunakan:
- WebdriverIO (CommonJS)
- Appium (UiAutomator2 driver, Android)
- Cucumber / Gherkin untuk test case
- Page Object Model untuk struktur kode

## Struktur Folder

```
automation-challenge/
├── package.json
├── wdio.conf.js
├── pageobjects/
│   ├── base.page.js
│   └── homepage.page.js
├── test/
│   ├── features/
│   │   └── homepage.feature
│   └── step-definitions/
│       └── homepage.steps.js
└── README.md
```

## ⚠️ Yang WAJIB kamu lakukan sebelum test bisa jalan

Scaffold ini sudah lengkap secara struktur, tapi locator di `pageobjects/homepage.page.js`
masih **placeholder**. Kamu harus:

1. Download app 99.co (versi terbaru, **bukan Pro**) dan install di emulator/device Android.
2. Jalankan Appium server dan buka **Appium Inspector**, connect dengan capability yang sama
   seperti di `wdio.conf.js`.
3. Scan elemen-elemen asli di homepage (search bar, promo banner, tab kategori, listing card,
   bottom navigation), lalu catat accessibility id / resource-id / xpath-nya.
4. Ganti semua locator placeholder di `pageobjects/homepage.page.js` dengan hasil scan tersebut.
5. Sesuaikan `appPackage`, `appActivity`, dan path APK di `wdio.conf.js` dengan app asli.

## Cara Install & Menjalankan

```bash
# 1. Install dependencies
npm install

# 2. Install Appium driver untuk Android
npx appium driver install uiautomator2

# 3. Jalankan Appium server di terminal terpisah (jika tidak pakai service otomatis)
npx appium

# 4. Jalankan test
npm test
```

## Checklist Submission (sesuai instruksi di README repo original)

- [ ] Fork repository ini ke akun GitHub kamu
- [ ] Invite `indra99co` sebagai collaborator di repo hasil fork
- [ ] Isi semua locator asli hasil scan Appium Inspector
- [ ] Pastikan semua scenario di `homepage.feature` berjalan dan pass
- [ ] Commit & push ke branch kamu
- [ ] Buat Pull Request ke repository original
