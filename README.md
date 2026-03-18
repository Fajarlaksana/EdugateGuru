<div align="center">

<br/>

# 🎓 Edugate Guru

### *Best Solution for your school — Aplikasi manajemen tugas dan profil guru berbasis Android.*

<br/>

[![Java](https://img.shields.io/badge/Java-Android-ED8B00?style=flat-square&logo=openjdk&logoColor=white)](https://www.java.com/)
[![Android](https://img.shields.io/badge/Android-API_15+-3DDC84?style=flat-square&logo=android&logoColor=white)](https://developer.android.com/)
[![Material Design](https://img.shields.io/badge/Material_Design-1.0-757575?style=flat-square&logo=materialdesign&logoColor=white)](https://material.io/)
[![CardView](https://img.shields.io/badge/CardView-25.3.1-9C27B0?style=flat-square)](https://developer.android.com/guide/topics/ui/layout/cardview)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

<br/>

> Aplikasi Android native untuk guru yang memudahkan pengelolaan tugas, agenda, dan profil.
> Dibangun oleh tim **SchoolTech** — 5 siswa SMK 4 Bandung — sebagai proyek pelajaran PKK.

<br/>

> A native Android app for teachers that simplifies task management, scheduling, and profile management.
> Built by **SchoolTech** — 5 students of SMK 4 Bandung — as a PKK (Entrepreneurship) school project.

<br/>

---

</div>

## 📋 Daftar Isi / Table of Contents

- [Tentang Aplikasi / About](#-tentang-aplikasi--about)
- [Fitur / Features](#-fitur--features)
- [Alur Navigasi / Navigation Flow](#-alur-navigasi--navigation-flow)
- [Tech Stack & Libraries](#-tech-stack--libraries)
- [Memulai / Getting Started](#-memulai--getting-started)
- [Struktur Proyek / Project Structure](#-struktur-proyek--project-structure)
- [Keterbatasan & Ide Pengembangan](#-keterbatasan--ide-pengembangan--limitations--future-development)
- [Tim / Team](#-tim--team)
- [Kontribusi / Contributing](#-kontribusi--contributing)
- [Kontak / Contact](#-kontak--contact)
- [Lisensi / License](#-lisensi--license)

<br/>

---

## 🌟 Tentang Aplikasi / About

**🇮🇩 Bahasa Indonesia**

**Edugate Guru** adalah aplikasi Android native yang dirancang untuk membantu guru dalam mengelola kegiatan sekolah sehari-hari — mulai dari membuat tugas, melihat agenda, hingga mengelola profil pribadi. Aplikasi ini dikembangkan sebagai proyek pelajaran **PKK (Produk Kreatif dan Kewirausahaan)** di **SMK 4 Bandung** oleh tim **SchoolTech**.

**🇬🇧 English**

**Edugate Guru** is a native Android application designed to help teachers manage their daily school activities — from creating assignments, viewing schedules, to managing their personal profile. This app was developed as a **PKK (Creative Product and Entrepreneurship)** school project at **SMK 4 Bandung** by team **SchoolTech**.

<br/>

---

## ✨ Fitur / Features

| Layar / Screen | Fitur / Feature |
|---|---|
| 🚀 **Landing Page** | Halaman selamat datang dengan branding Edugate + tombol "Get Started" / Welcome screen with Edugate branding + "Get Started" button |
| 🏠 **Home Dashboard** | 4 menu utama dalam grid CardView: Agenda, Tugas, Profil, About / 4 main menus in CardView grid |
| 📋 **Tugas / Assignment** | Form buat tugas: Nama Tugas, Deskripsi, Tanggal, dan Waktu / Assignment form: Name, Description, Date, and Time |
| 👤 **Profil / Profile** | Tampilkan profil guru: foto, nama, NIS, telepon, email, ID Guru, kota / Teacher profile: photo, name, NIS, phone, email, teacher ID, city |
| ✏️ **Edit Profil** | Form edit: Nama, No. Telepon, Email, Kota, Password / Edit form: Name, Phone, Email, City, Password |
| ℹ️ **About** | Informasi tentang aplikasi dan tim SchoolTech / App info and SchoolTech team description |

<br/>

---

## 🗺️ Alur Navigasi / Navigation Flow

```
┌──────────────────────┐
│    MainActivity      │  ← Launcher Activity
│    (Landing Page)    │
│   Tombol "Get Started"│
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│    HomeActivity      │
│  + FragmentHome      │
│                      │
│  [ Agenda ] [ Tugas ]│──── Tugas ──→ TugasActivity ──→ HomeActivity
│  [ Profil ] [ About ]│──── Profil ──→ ProfileActivity
└──────────────────────┘         ↓
                          EditProfileActivity
                                 ↓
                          ProfileActivity
```

> ⚠️ Menu **Agenda** dan **About** dari `FragmentHome` belum terhubung ke activity-nya masing-masing.

<br/>

---

## 🛠 Tech Stack & Libraries

| Kategori | Library / Tool | Versi |
|---|---|---|
| **Language** | Java | - |
| **Min SDK** | API 15 (Android 4.0.3 Ice Cream Sandwich) | - |
| **Target SDK** | API 29 (Android 10) | - |
| **UI** | AppCompat, ConstraintLayout | 1.0.2 / 1.1.3 |
| **Card UI** | [CardView](https://developer.android.com/guide/topics/ui/layout/cardview) | 25.3.1 |
| **Design System** | [Material Components for Android](https://material.io/develop/android) | 1.0.0 |
| **Custom Font** | Viga Regular (`viga_reguler.ttf`) | - |
| **Testing** | JUnit, Espresso | 4.12 / 3.2.0 |

<br/>

---

## 🚀 Memulai / Getting Started

### Prasyarat / Prerequisites

- [Android Studio](https://developer.android.com/studio) versi terbaru / latest version
- JDK 8+
- Android device atau emulator **API 15+** (Android 4.0.3+)

### Instalasi / Installation

```bash
# 1. Clone repository
git clone https://github.com/Fajarlaksana/EdugateGuru.git

# 2. Buka di Android Studio
# File → Open → pilih folder EdugateGuru

# 3. Sync Gradle
# Android Studio akan otomatis menawarkan Gradle sync

# 4. Run aplikasi
# Klik tombol ▶ Run atau tekan Shift+F10
```

### Penggunaan / Usage

1. Buka aplikasi → halaman **Landing** dengan logo *"Edugate"* dan tagline *"Best Solution for your school"*
2. Tekan **"Get Started"** untuk masuk ke **Home Dashboard**
3. Pilih menu dari grid CardView:
   - **Tugas** → isi Nama Tugas, Deskripsi, Tanggal, Waktu → tekan **"Buat"**
   - **Profil** → lihat data profil guru → tekan **"Edit Profile"** untuk mengubah data
   - **About** → lihat informasi tim SchoolTech

<br/>

---

## 📁 Struktur Proyek / Project Structure

```
EdugateGuru/
│
├── 📄 build.gradle                         # Project-level Gradle config
├── 📄 settings.gradle                      # Project settings
├── 📄 gradle.properties                    # Gradle properties
├── 📄 gradlew / gradlew.bat                # Gradle wrapper scripts
│
├── 📂 gradle/wrapper/                      # Gradle wrapper files
│
└── 📂 app/
    ├── build.gradle                        # Dependencies, SDK config & build types
    ├── proguard-rules.pro                  # ProGuard rules
    │
    └── 📂 src/main/
        ├── AndroidManifest.xml             # App manifest & activity declarations
        │
        ├── 📂 java/com/example/edugateguru/
        │   │
        │   ├── MainActivity.java           # 🚀 Landing page (Launcher Activity)
        │   │                               #    Logo Edugate + btn "Get Started" → HomeActivity
        │   │
        │   ├── HomeActivity.java           # 🏠 Dashboard utama, host FragmentHome
        │   │
        │   ├── 📂 Fragment/
        │   │   └── FragmentHome.java       # 🔲 Grid 2x2 CardView
        │   │                               #    Agenda, Tugas → TugasActivity
        │   │                               #    Profil → ProfileActivity, About
        │   │
        │   ├── TugasActivity.java          # 📋 Form buat tugas
        │   │                               #    Input: Nama Tugas, Deskripsi, Date, Time
        │   │                               #    Btn "Buat" → kembali ke HomeActivity
        │   │
        │   ├── ProfileActivity.java        # 👤 Halaman profil guru (data statis)
        │   │                               #    Nama, NIS, Telepon, Email, ID Guru, Kota
        │   │                               #    Btn "Edit Profile" → EditProfileActivity
        │   │
        │   ├── EditProfileActivity.java    # ✏️ Form edit profil
        │   │                               #    Input: Nama, Telepon, Email, Kota, Password
        │   │                               #    Btn "Simpan" → ProfileActivity
        │   │
        │   └── AboutActivity.java          # ℹ️ Halaman About Us + deskripsi SchoolTech
        │
        └── 📂 res/
            │
            ├── 📂 font/
            │   ├── fonts.xml               # Font family definition
            │   └── viga_reguler.ttf        # Custom font Viga Regular (dipakai di landing)
            │
            ├── 📂 layout/
            │   ├── activity_main.xml       # Landing: Logo + tagline + btn "Get Started"
            │   ├── activity_home.xml       # Container fragment (fragment_container)
            │   ├── fragment_home.xml       # Grid 2x2 CardView menu utama
            │   ├── activity_tugas.xml      # Form: Nama Tugas, Deskripsi, Date, Time
            │   ├── activity_profile.xml    # Profil: foto, nama, NIS, info cards
            │   ├── activity_edit_profile.xml # Edit: Nama, Telp, Email, Kota, Password
            │   ├── activity_about.xml      # About Us + konten SchoolTech
            │   ├── main_toolbar.xml        # Custom toolbar utama
            │   ├── toolbar_tugas.xml       # Custom toolbar halaman Tugas
            │   └── toolbar_about.xml       # Custom toolbar halaman About
            │
            ├── 📂 drawable/
            │   ├── custom_button.xml       # Shape tombol ungu (#BE2EDD)
            │   ├── custom_shadow_button.xml # Efek bayangan di bawah tombol
            │   ├── boxbg.xml               # Background kotak EditText deskripsi
            │   ├── agenda.png              # Ikon menu Agenda
            │   ├── tugas.png               # Ikon menu Tugas
            │   ├── profil.png              # Ikon menu Profil
            │   ├── about.png               # Ikon menu About
            │   ├── circle_image.png        # Placeholder foto profil bulat
            │   ├── undraw_teacher_35j2.png # Ilustrasi guru di landing page
            │   └── ic_*.xml                # Icon set: back, person, phone, email, home, dll
            │
            └── 📂 values/
                ├── colors.xml              # Palet: purple #BE2EDD, deep purple, green, dll
                ├── strings.xml             # app_name + teks deskripsi About
                └── styles.xml              # AppTheme & style definitions
```

<br/>

---

## 🚧 Keterbatasan & Ide Pengembangan / Limitations & Future Development

**🇮🇩 Keterbatasan saat ini:**
- Data profil masih **hardcoded** (nama, NIS, telepon, dll) — belum terhubung ke database
- Form **Edit Profil** dan **Tugas** belum benar-benar menyimpan data ke mana pun
- Menu **Agenda** di `FragmentHome` belum terhubung ke Activity manapun
- Belum ada sistem **login / autentikasi** untuk guru
- Belum ada koneksi ke backend atau server

**🇬🇧 Current limitations:**
- Profile data is **hardcoded** (name, NIS, phone, etc.) — not connected to any database
- **Edit Profile** and **Tugas** forms do not actually persist any data
- **Agenda** menu in `FragmentHome` is not wired to any Activity
- No **login / authentication** system for teachers
- No backend or server connection

### 💡 Ide Pengembangan / Development Ideas

| Prioritas | Ide / Idea |
|---|---|
| 🔴 **High** | Database lokal dengan **Room** atau **SQLite** untuk simpan tugas & profil |
| 🔴 **High** | Implementasi fitur **Agenda** yang fungsional |
| 🔴 **High** | Sistem **login / autentikasi** guru |
| 🟡 **Medium** | Backend dengan **Firebase Firestore** atau **REST API** |
| 🟡 **Medium** | Migrasi ke **Kotlin** + **MVVM Architecture** |
| 🟡 **Medium** | Notifikasi pengingat deadline tugas |
| 🟡 **Medium** | Upload foto profil dari kamera / galeri |
| 🟢 **Low** | Migrasi UI ke **Material Design 3** |
| 🟢 **Low** | Dark mode support |
| 🟢 **Low** | Export tugas ke PDF |

<br/>

---

## 👥 Tim / Team

Aplikasi ini dibuat oleh tim **SchoolTech** — 5 siswa **SMK 4 Bandung** dalam pelajaran PKK.

This app was created by team **SchoolTech** — 5 students of **SMK 4 Bandung** during PKK class.

> *"Edugate adalah App yang dibuat oleh perusahaan SchoolTech pada saat pelajaran PKK. SchoolTech terdiri dari 5 orang yang bersekolah di SMK 4 Bandung."*

<br/>

---

## 🤝 Kontribusi / Contributing

**🇮🇩** Kontribusi sangat disambut! Silakan buat issue atau pull request.

**🇬🇧** Contributions are welcome! Feel free to open an issue or submit a pull request.

```bash
# 1. Fork repository ini / Fork this repository

# 2. Buat branch baru / Create a new branch
git checkout -b feature/nama-fitur

# 3. Commit perubahan / Commit your changes
git commit -m "feat: tambah fitur X"

# 4. Push ke branch / Push to branch
git push origin feature/nama-fitur

# 5. Buka Pull Request / Open a Pull Request
```

<br/>

---

## 📬 Kontak / Contact

**🇮🇩** Jika ada pertanyaan atau ingin berkolaborasi, silakan hubungi:

**🇬🇧** For questions or collaboration, feel free to reach out:

<div align="center">

**Fajar Laksana**

📧 [fajarlaksana13@gmail.com](mailto:fajarlaksana13@gmail.com)

🔗 [github.com/Fajarlaksana](https://github.com/Fajarlaksana)

</div>

<br/>

---

<div align="center">

Dibuat dengan ❤️ oleh **SchoolTech** — SMK 4 Bandung

*Edugate — Best Solution for your school.*

</div>
