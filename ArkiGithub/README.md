# Super Estimator RAB - ArkiDigital

## PENTING: Cara Upload ke GitHub yang Benar

Saat upload ke GitHub, pastikan struktur seperti ini:

```
repository/                    <- ROOT repo GitHub
  .github/
    workflows/
      build.yml
  app/
    src/...
    build.gradle
  build.gradle
  settings.gradle
  gradlew
  gradlew.bat
  KEYSTORE_BASE64.txt
  README.md
```

BUKAN seperti ini (SALAH):
```
repository/
  ArkiGithub/         <- JANGAN ada folder ini
    .github/
    app/
    build.gradle
```

---

## Setup GitHub Actions

### Step 1: Tambah Secret
- Buka repo GitHub > Settings > Secrets and variables > Actions
- Klik New repository secret
- Name: KEYSTORE_BASE64
- Value: copy-paste seluruh isi file KEYSTORE_BASE64.txt
- Klik Add secret

### Step 2: Push File ke GitHub

Buka CMD di dalam folder ArkiGithub (bukan folder luarnya):
```
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO.git
git push -u origin main
```

### Step 3: Run Workflow
- Buka tab Actions di GitHub
- Klik Build APK & AAB
- Klik Run workflow > Run workflow
- Tunggu 5-10 menit
- Download APK/AAB dari bagian Artifacts

---

## Login App
- Username: kontraktor
- Password: arkidigital

## Keystore
- File: app/arkidigital.jks
- Store password: arkidigital2025
- Key alias: arkidigitalkey
- Key password: arkidigital2025
