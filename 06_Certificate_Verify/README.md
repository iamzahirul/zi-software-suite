# ZI Certify — Training Certificates with QR Verification

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

ট্রেনিং সেন্টার ও এনজিওর জন্য: ট্রেনিং, অংশগ্রহণকারী, একসাথে সার্টিফিকেট তৈরি ও প্রিন্ট, QR কোড দিয়ে অনলাইনে যাচাই।

- **Online demo — office app:** https://zi-certify-demo.vercel.app → name din → "স্যাম্পল ডেটা দেখুন".
- **Online demo — public verify page:** https://zi-certify-demo.vercel.app/verify.html (same browser-e demo; try `RTC-2026-A0001`, revoked: `RTC-2026-A0004`).
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- Trainings: organiser/donor, venue, dates, hours, trainer; per-training certificate design (Classic border / Modern band / Elegant gold), colour, heading and text with {name} {training} {organizer} {venue} {from} {to} {hours} {organization} {designation}.
- Participants: add or **import from Excel (CSV)**, organisation, designation, district, NID, attendance %.
- **Issue certificates to the whole batch** (attendance limit, e.g. 80%), automatic numbers `PREFIX-2026-A0001`, **bulk print** (A4 landscape, one per page) with QR code and two signatures.
- Certificate register: search, print, **revoke with reason / restore**, CSV export, quick check box.
- Public verify page: scan QR or type number → genuine / revoked (with reason) / not found. Name and training are copied into the certificate, so later edits don't change what was issued.
- Bangla/English, dark mode, PIN lock, backup, offline.

## Verification online (one-time per client)
1. Free Supabase project → SQL Editor: `_source/zi-software/supabase/zi_sync.sql`, then `certify_verify.sql`.
2. Authentication → Users → organisation email + password.
3. App: Settings → Cloud sync → connect. Print certificates after that — their QR codes open the online verify page.

Only one public function is exposed (`certify_verify`); the data table stays private. Tested with `node tools/test-certify-sql.mjs`.

## Changelog

### v1.0.1 — 28 Oct 2026
- Verify page and the office "Check a certificate" box accept numbers typed with Bangla digits, small letters or spaces (e.g. "rtc-২০২৬-a০০০১").
- Issue certificates: you now choose the issue date (default: last day of the training).
- Correcting a training's title, organiser, dates or hours after issuing asks to correct the issued certificates too, so the verify page shows the right details.
- Trainings can be deleted (only when no certificate was issued).
- Attendance must be 0–100%; hours cannot be minus.
- Excel/CSV import understands Bangla and common English column names (নাম, মোবাইল, Full Name, Mobile…), skips people already in the training, and says clearly when the name column is missing.
- Certificate text no longer shows an empty "( , …)" or "0 hours" when venue or hours are left empty.
- Certificate number prefix keeps only letters and digits (no spaces or Bangla letters that are hard to type on the verify page).
- Dashboard: "by organiser" chart showed counts as Taka — fixed; "this year" counts only valid certificates.
- Certificate CSV export: status in words and the revoke reason added.
- Search with Bangla digits works for participants and certificates.
