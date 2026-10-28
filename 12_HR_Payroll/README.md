# ZI HR — Attendance & Payroll

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

অফিস, শোরুম ও ছোট কারখানার জন্য: কর্মচারী তথ্য, প্রতিদিনের হাজিরা (উপস্থিত / অনুপস্থিত / ছুটি / অর্ধদিবস, দেরি, ওভারটাইম), অগ্রিম ও লোন, মাস শেষে এক ক্লিকে বেতন শিট ও বেতন স্লিপ।

- **Online demo:** https://zi-hr-demo.vercel.app → প্রতিষ্ঠানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-HR-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Employees:** ID (E-A1001…), photo, designation, department, joining date, blood group, NID, salary parts (basic, house rent, medical, transport) or daily rate for daily workers, overtime rate per hour, where salary goes (bKash / bank). Mark as left / rejoin. **ID cards** (8 per A4 with barcode).
- **Daily attendance:** everyone starts as present — tap অ (absent), ছু (leave), অর্ধ (half day), দেরি (late), and overtime hours. Holidays and weekly off days (Friday, or Friday + Saturday…). Works on a phone.
- **Employee page:** month calendar of attendance, leave used this year vs allowed, advance still owed, payslip history.
- **Advances & loans:** amount and monthly installment; cut from salary automatically until paid back.
- **Payroll (one click):** gross − absent days (gross ÷ 30) − late rule (e.g. every 3 late days = 1 day) − leave above the yearly quota + overtime + bonus − advance installment − other cuts = net pay. Recalculate any time before paying; mark paid (cash / bKash / Nagad / bank).
- **Prints:** salary sheet (A4 landscape with signature column), payslips (2 per A4, with salary breakdown), attendance register for the month, ID cards. CSV export for bKash / bank bulk payment.
- **Reports:** attendance % per employee, department-wise salary cost, month-by-month salary, overtime.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for several computers / phones.

## Note
Fingerprint / face attendance machines (ZKTeco etc.) can be connected later by importing their CSV export — ask if needed.

## Changelog

### v1.0.1 — 28 Oct 2026
- Staff who join or leave in the middle of a month now get salary only for the days they were on the books (before, they got the full month).
- Leave above the yearly quota is now cut only in the month it happens; leave taken later in the year no longer changes an earlier month's salary.
- Advance cut can no longer be bigger than the pay left (an employee absent all month no longer shows the advance as repaid), and an advance given after a month is not cut from that month's salary.
- Overtime worked on a weekly off day (Friday) is now paid; daily workers are paid for the day.
- Attendance: overtime like 1.5 hours can now be typed; marking someone absent or on leave clears their late mark and overtime.
- New: festival (Eid / Puja) bonus for everyone in one step (% of basic, fixed amount for daily workers, optional 1-year service rule).
- New: send each employee their salary by SMS / WhatsApp from the payroll page.
- New: "OT by law" button fills the overtime rate (basic ÷ 208 × 2); setting to cut absent days from basic ÷ 30 instead of gross ÷ 30.
- Payroll: delete a wrong unpaid slip, or mark a paid slip as unpaid again.
- Checks: negative amounts, missing salary, wrong mobile number, monthly cut bigger than the advance are refused with a clear message; advance form no longer shows an employee as chosen when none is.
- Employee page calendar shows weekday names; phone layout of the attendance list and employee header fixed; Bangla wording ("ওটি", "পরিশোধ").
