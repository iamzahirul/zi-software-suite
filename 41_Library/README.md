# ZI Library — Books, issue & return

Developed by **Zahirul Islam (Rasel)** · https://iamzahirul.com

স্কুল, কলেজ, মাদ্রাসা ও পাঠাগারের জন্য: প্রতিটি কপির অ্যাকসেশন নম্বর, বারকোড স্ক্যান করে ইস্যু-ফেরত-মেয়াদ বাড়ানো, দেরির জরিমানা, হারানো বই, লাইব্রেরি কার্ড, মেয়াদোত্তীর্ণ এসএমএস, অ্যাকসেশন রেজিস্টার ও রিপোর্ট।

- **Online demo:** https://zi-library-demo.vercel.app → প্রতিষ্ঠানের নাম দিন → "স্যাম্পল ডেটা দেখুন".
- **Bangla tutorial video:** `video/ZI-Library-Tutorial-Bangla.mp4` — show this to clients.
- **Android APK:** `apk/` folder. **Laptop:** demo link → Chrome/Edge "Install". **Web build:** `web/`.

## Features
- **Circulation desk:** scan (USB/Bluetooth scanner or phone camera) or type an accession number or a library card number. A book on the shelf → find the member → issue with the due date by member type. A book that is out → borrower, due date, days late and fine → return (take or waive the fine), renew, or mark lost (charge the price). Limits on books per member and warnings for unpaid fines. Today's activity and overdue list.
- **Books:** title, author, publisher, category (textbook, reference, novel, Liberation War, science, religion…), language, ISBN, edition, year, shelf, price; adding N copies gives N accession numbers automatically; each copy's condition (good / damaged / lost / weeded out), who has it, history; **barcode labels** (24 per A4).
- **Members:** students (class, section, roll), teachers and staff, phone; CSV import of whole classes; **library cards** with barcode (CR80 size, 10 per A4); each member's books and fines.
- **Loans:** issued now, overdue (SMS / WhatsApp reminders, printed list), returned, lost.
- **Reports:** most borrowed books, categories (titles, copies, value), top readers, reading by class, fines collected; **accession register** print (A4 landscape) as kept in a register book; CSV export.
- **Rules (Settings):** days a student / teacher keeps a book, books at a time, fine per late day, renewals allowed.
- Bangla/English, dark mode, PIN lock, backup, offline; optional cloud sync (Supabase) for more than one desk.

## Needs from the client
- Nothing paid is required. A USB barcode scanner (≈৳1,500–3,000) makes the desk faster; phone cameras work in Chrome on Android. Automatic bulk SMS would need an SMS gateway account.
