# ZI Somiti — Savings & Loan Management

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

সমিতি, সমবায় ও ক্ষুদ্র ঋণ দলের জন্য: সদস্য, সাপ্তাহিক / মাসিক সঞ্চয়, ঋণ ও কিস্তি, সভার দিনের আদায় শিট, পাসবই, ঋণ কার্ড, ক্যাশ বই ও সমিতির আয়-ব্যয়।

- **Online demo:** https://zi-somiti-demo.vercel.app → সমিতির নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Somiti-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Members:** member no (M-A1001…), photo, father / husband, mobile, NID, address, group, nominee, joining date, fixed savings per week / month. Admission fee and shares taken on joining.
- **Savings:** deposits, withdrawals (never below the balance), savings arrears worked out from the plan; **passbook** print.
- **Loans:** amount, flat interest %, number of installments, weekly / monthly, service charge, purpose, guarantor → total payable, installment amount and full schedule. Overdue amount and late installments; loan closes itself when paid off. **Loan card** with schedule and signature column.
- **Collection sheet (meeting day):** every member's savings and installment due; "fill all dues" then change only who paid less; one save posts everything with receipt numbers. Printable sheet for the field officer.
- **Cash book:** deposits, installments, admission, shares, fines, service charges, other income vs loans given, withdrawals, office costs; opening / closing cash.
- **Reports:** month by month (deposits, withdrawals, loans given / collected, interest earned, office expense, net income), member-wise savings and loans, overdue list, group-wise. Portfolio at risk (PAR). Installment reminders by SMS / WhatsApp.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for office computer + field officer phones.

## Changelog

### v1.0.1 — 28 Oct 2026
- Collection sheet: "Fill all dues" no longer asks again for savings / installments already collected that day (pressing it twice used to collect twice); members who paid show "Paid today".
- A new loan's first installment is no longer asked for on the day the loan is given — only when an installment falls due before the next meeting.
- A loan can no longer be paid beyond what is left on it from the collection sheet; negative or zero amounts are refused everywhere.
- Small loans with many installments no longer get a negative last installment.
- Receipt printed right after a deposit / installment now shows the balance after that payment.
- Deleting a repayment from the member page reopens a loan that had been marked fully paid.
- New: close a member's account (pays back savings as a withdrawal, only when no loan is owed) and open it again.
- New: delete a loan entered by mistake (before any repayment).
- Loan form no longer looks like a member is chosen when none is; mobile number and amounts are checked.
- Sample data now leaves today's meeting uncollected so you can try the collection sheet.
