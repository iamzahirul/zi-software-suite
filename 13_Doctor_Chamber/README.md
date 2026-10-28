# ZI Doctor Chamber — Serial & Prescription

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

ডাক্তারের চেম্বারের জন্য: রোগীর সিরিয়াল, দ্রুত প্রেসক্রিপশন লেখা ও নিজের প্যাডে প্রিন্ট, ফি আদায়, রোগীর ইতিহাস, ফলো-আপ রিমাইন্ডার।

- **Online demo:** https://zi-chamber-demo.vercel.app → চেম্বারের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Doctor-Chamber-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Serial (সিরিয়াল):** today's queue in order, next patient highlighted, waiting / seen / did-not-come, fee collected or due. New serial: search old patient by name / mobile / ID or add a new one; visit type (new / follow-up / report show) sets the fee automatically (follow-up within N days). Printable serial list.
- **Prescription:** patient header with allergy and history; vitals (BP, pulse, temp, weight, SpO₂, RBS); complaints (C/C), findings (O/E), diagnosis (Dx), tests (Ix) with one-tap common tests; medicines with autocomplete from the doctor's own list (usual dose, before/after meal, days filled in); one-tap advice; follow-up +7 / +15 / +30 days. Copy the last prescription, apply a template, save as template, "save & next patient".
- **Print:** A4 or A5 pad with doctor's name, degrees, speciality, BMDC no, chamber address and hours — or blank top for pre-printed pads. Bangla dose text ("১+০+১ — খাবারের পরে — ৫ দিন").
- **Patients:** ID (P-A1001…), age, sex, blood group, allergy, history; every past prescription, reprint any.
- **Medicines & templates:** the doctor's medicine list (sample list of 30 common brands) ordered by use; templates for common diseases.
- **Reports:** daily patients (new / follow-up / report), fee collected and due, diagnosis frequency, medicines written, upcoming follow-ups with SMS / WhatsApp reminders.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) so the assistant's serial desk and the doctor's laptop share data.

## Changelog

### v1.0.1 — 28 Oct 2026
- Saving a prescription no longer overwrites a fee the assistant collected at the desk while the doctor was writing.
- A5 prescriptions now fit on one page (before, even a short prescription spilled onto a second sheet).
- Medicine days typed in Bangla ("৭") now print as "৭ দিন".
- Giving a serial to the same patient (same name and mobile) again reuses the old record instead of making a duplicate; the "already waiting" check now works for them.
- Fee checks: paid more than the fee, negative amounts and wrong mobile numbers are refused with a clear message.
- Medicine "used" count goes up once per prescription (it used to rise on every re-save; duplicate lines no longer create duplicate medicines).
- New: "Message waiting patients" — send each waiting patient their serial number and the serial now being seen by SMS / WhatsApp.
- Prescription print hides empty age / sex; patient name on the prescription screen lines up properly on phones.
