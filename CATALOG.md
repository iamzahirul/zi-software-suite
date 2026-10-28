# ZI Software Catalog

Developer: **Zahirul Islam (Rasel)** · https://iamzahirul.com

Every app runs on **Android (APK)** and **laptop (installable web app / PWA)**, works **offline**,
has **Bangla + English**, backup/restore, optional **cloud sync** (Supabase), and shows the developer credit.
Every app also gets an **online demo link** for showing clients.

Stack: TypeScript + React 19 + Vite 8 + Tailwind 4 + Dexie (offline DB) + Capacitor 8 (APK). Source code lives in
`C:\ZI` (node_modules can't live on Google Drive); a copy is kept in `_source/`. See `_source/zi-software/README.md`.

Status: ✅ done · 🔨 in progress · ⏳ queued

## A) Ready products — customise and sell
| # | Software | Buyer | Price (৳) | Folder | Status |
|---|---|---|---|---|---|
| 01 | POS / Billing & Stock (barcode, due, invoice 80mm/A4) — demo: https://zi-pos-demo.vercel.app | Mobile/accessories shop, grocery, cosmetics | 15,000–20,000 | `01_POS_Billing` | ✅ |
| 02 | Pharmacy Management (batch, expiry alert, due) — demo: https://zi-pharmacy-demo.vercel.app | Pharmacy, drug store | 15,000–20,000 | `02_Pharmacy` | ✅ |
| 03 | Coaching / Online Course LMS (course, quiz, certificate, bKash TrxID) — demo: https://zi-academy-demo.vercel.app · student portal: https://zi-academy-demo.vercel.app/portal.html | Coaching, trainer, IT institute | 15,000–20,000 | `03_Coaching_LMS` | ✅ |
| 04 | E-commerce website (WooCommerce) | F-commerce seller, gadget shop | 12,000–20,000 | | ⏸ later |
| 05 | AI Chatbot (website/FB support, Bangla) | Shop, clinic, institute | 10,000–15,000 + API | | ⏸ later |
| 06 | Certificate verify with QR — demo: https://zi-certify-demo.vercel.app · verify page: https://zi-certify-demo.vercel.app/verify.html | Training center, NGO | 8,000–12,000 | `06_Certificate_Verify` | ✅ |

## B) New, simple, high demand
| # | Software | Buyer | Price (৳) | Status |
|---|---|---|---|---|
| 07 | F-commerce Order Manager (Steadfast/Pathao, COD) — demo: https://zi-orders-demo.vercel.app · folder `07_FCommerce_Orders` | Facebook page seller | 12,000–18,000 | ✅ |
| 08 | Coaching / Tuition Management (student, fee, attendance, SMS) — demo: https://zi-coaching-demo.vercel.app · folder `08_Coaching_Tuition` | Coaching, tutor | 12,000–18,000 | ✅ |
| 09 | School Result + Admit Card + Fee — demo: https://zi-school-demo.vercel.app · folder `09_School_Result` | Kindergarten, school, madrasa | 15,000–20,000 | ✅ |
| 10 | Restaurant POS (table, KOT, kitchen screen, bill) — demo: https://zi-resto-demo.vercel.app · folder `10_Restaurant_POS` | Restaurant, cafe | 15,000–20,000 | ✅ |
| 11 | Baki Khata / Customer Ledger (dues, reminders, cash box) — demo: https://zi-khata-demo.vercel.app · folder `11_Baki_Khata` | Small shop, wholesaler | 8,000–12,000 | ✅ |
| 12 | HR, Attendance & Payroll (overtime, advances, salary sheet) — demo: https://zi-hr-demo.vercel.app · folder `12_HR_Payroll` | Office, showroom, factory | 12,000–18,000 | ✅ |
| 13 | Doctor Chamber (serial + prescription print) — demo: https://zi-chamber-demo.vercel.app · folder `13_Doctor_Chamber` | Doctor, dental chamber | 15,000–20,000 | ✅ |
| 14 | Bari Vara Management (rent, meter bill, receipt) — demo: https://zi-rent-demo.vercel.app · folder `14_Bari_Vara` | Landlord, building manager | 10,000–15,000 | ✅ |
| 15 | Somiti / Savings-Loan Management (collection sheet, passbook, loan card) — demo: https://zi-somiti-demo.vercel.app · folder `15_Somiti` | Somiti, cooperative | 15,000–20,000 | ✅ |
| 16 | Masjid / Madrasa Donation & Fee (funds, chanda, monthly notice) — demo: https://zi-masjid-demo.vercel.app · folder `16_Masjid_Madrasa` | Masjid committee, madrasa | 10,000–15,000 | ✅ |
| 17 | Survey / Data Dashboard (KoBo/SurveyCTO → dashboard, cross-tab, data quality) ★ — demo: https://zi-survey-demo.vercel.app · folder `17_Survey_Dashboard` | NGO, research firm | 15,000–20,000 | ✅ |
| 18 | Landing Page + Order Form (page builder, WhatsApp / Google Sheet orders) — demo: https://zi-landing-demo.vercel.app · sample page: https://zi-landing-demo.vercel.app/sample.html · folder `18_Landing_Page` | Single-product seller | 8,000–12,000 | ✅ |
| 47 | AI Unified Inbox (Messenger + Instagram + WhatsApp + web chat, Gemini AI agent, orders, Steadfast) — PHP/MySQL server app, `47_AI_Unified_Inbox` · upload zip `deploy/` · Android app `apk/AI-Unified-Inbox-v1.0.0.apk` (asks for the site address) | F-commerce seller, shop with FB page | 15,000–20,000 | 🔨 |

## C) Shop & service business
| # | Software | Buyer | Price (৳) | Status |
|---|---|---|---|---|
| 19 | Mobile Servicing Job Card (IMEI, pattern lock, parts, ready SMS, warranty) — demo: https://zi-repair-demo.vercel.app · folder `19_Mobile_Servicing` | Mobile/laptop repair | 10,000–15,000 | ✅ |
| 20 | Pre-owned Phone Register (IMEI, NID, NEIR check, warranty, exchange) — demo: https://zi-usedphone-demo.vercel.app · folder `20_Used_Phone_Register` | Used phone shop | 10,000–15,000 | ✅ |
| 21 | Salon / Parlour (appointment board, bill, staff commission, client history) — demo: https://zi-salon-demo.vercel.app · folder `21_Salon_Parlour` | Parlour, salon | 10,000–15,000 | ✅ |
| 22 | Tailor Shop (measurements, order, cutting slip, karigor wage, Eid load) — demo: https://zi-tailor-demo.vercel.app · folder `22_Tailor_Shop` | Tailor, boutique | 8,000–12,000 | ✅ |
| 23 | Laundry Order Tracker (piece tags, express, rack, home delivery, monthly accounts) — demo: https://zi-laundry-demo.vercel.app · folder `23_Laundry_Tracker` | Laundry, dry cleaner | 8,000–12,000 | ✅ |
| 24 | Gym Membership (check-in, packages, renewal alert, ID card, body progress) — demo: https://zi-gym-demo.vercel.app · folder `24_Gym_Membership` | Gym, fitness center | 10,000–15,000 | ✅ |
| 25 | Token / Queue System (counter calling, Bangla voice, TV display, wait time) — demo: https://zi-token-demo.vercel.app · folder `25_Token_Queue` | Chamber, clinic, service center | 8,000–12,000 | ✅ |

## D) Distribution, wholesale & field
| # | Software | Buyer | Price (৳) | Status |
|---|---|---|---|---|
| 26 | SR / DSR Order App (orders, dealer due, target, load sheet, DSR settlement) — demo: https://zi-sr-demo.vercel.app · folder `26_SR_Order_App` | Distributor, brand | 18,000–20,000 | ✅ |
| 27 | Dealer Ledger + Warranty Claim (serials, RMA) — demo: https://zi-dealer-demo.vercel.app · folder `27_Dealer_Warranty` | Accessories brand, wholesaler | 12,000–18,000 | ✅ |
| 28 | Fleet / Truck Trip (trip, fuel, driver cost, papers expiry) — demo: https://zi-fleet-demo.vercel.app · folder `28_Fleet_Trip` | Transport, rent-a-car | 15,000–20,000 | ✅ |
| 29 | Petrol Pump Shift Sales (Sheikh Filling Station logic) — demo: https://zi-pump-demo.vercel.app · folder `29_Petrol_Pump` | Fuel station | 15,000–20,000 | ✅ |

## E) Industry, agriculture & construction
| # | Software | Buyer | Price (৳) | Status |
|---|---|---|---|---|
| 30 | Construction Site Expense Tracker (material, labour, bill) — demo: https://zi-site-demo.vercel.app · folder `30_Construction_Expense` | Contractor, developer | 12,000–18,000 | ✅ |
| 31 | Flat Booking + Installment — demo: https://zi-flat-demo.vercel.app · folder `31_Flat_Booking` | Real estate developer | 15,000–20,000 | ✅ |
| 32 | Garments Buying House Order/Sample Tracker — demo: https://zi-garments-demo.vercel.app · folder `32_Garments_Tracker` | Buying house, small factory | 15,000–20,000 | ✅ |
| 33 | Poultry / Dairy / Fish Farm (feed, mortality, sales, profit) — demo: https://zi-farm-demo.vercel.app · folder `33_Farm_Manager` | Farmer | 10,000–15,000 | ✅ |
| 34 | Brick Field / Rice Mill (labour, stock, sales) — demo: https://zi-mill-demo.vercel.app · folder `34_Brick_Rice_Mill` | Brick field, rice mill | 12,000–18,000 | ✅ |

## F) Travel, manpower & professional
| # | Software | Buyer | Price (৳) | Status |
|---|---|---|---|---|
| 35 | Recruiting Agency (passport, medical, visa, flight) — demo: https://zi-recruit-demo.vercel.app · `35_Recruiting_Agency` | Manpower agency | 15,000–20,000 | ✅ |
| 36 | Travel Agency (ticket, visa, Hajj-Umrah) — demo: https://zi-travel-demo.vercel.app · `36_Travel_Agency` | Travel agency | 15,000–20,000 | ✅ |
| 37 | Hotel / Resort Room Booking — demo: https://zi-hotel-demo.vercel.app · `37_Hotel_Booking` | Small hotel | 15,000–20,000 | ✅ |
| 38 | Lawyer Case Diary (hearing date, reminder, client fee) — demo: https://zi-lawyer-demo.vercel.app · `38_Lawyer_Case_Diary` | Lawyer, law firm | 10,000–15,000 | ✅ |

## G) Education
| # | Software | Buyer | Price (৳) | Status |
|---|---|---|---|---|
| 39 | Online MCQ Exam / Admission Test — demo: https://zi-exam-demo.vercel.app · candidate portal: https://zi-exam-demo.vercel.app/exam.html · `39_MCQ_Exam` | Coaching, admission center | 12,000–18,000 | ✅ |
| 40 | Hostel / Mess Management (meal count, mess bill) — demo: https://zi-mess-demo.vercel.app · `40_Hostel_Mess` | Hostel, mess | 8,000–12,000 | ✅ |
| 41 | Library Management — demo: https://zi-library-demo.vercel.app · `41_Library` | School, college | 8,000–12,000 | ✅ |
| 42 | ID Card + Admit Card Generator — demo: https://zi-idcard-demo.vercel.app · `42_ID_Admit_Card` | School, madrasa | 8,000–10,000 | ✅ |

## H) Low price, sell many times
| # | Product | Buyer | Price (৳) | Status |
|---|---|---|---|---|
| 43 | WooCommerce plugin: bKash/Nagad manual payment verify (TrxID, duplicate guard, advance/delivery-charge payment, verify screen) — demo: https://zi-woo-bkash-demo.vercel.app (live WordPress Playground) · `43_Woo_bKash_Verify/zi-bkash-nagad-verify.zip` | Online shop | 3,000–6,000 | ✅ |
| 44 | WooCommerce plugin: WhatsApp order button + Bangla invoice (quick order form saves the order, A4/80mm, amount in words) — demo: https://zi-woo-whatsapp-demo.vercel.app (live WordPress Playground) · `44_Woo_WhatsApp_Invoice/zi-whatsapp-order-invoice.zip` | Online shop | 2,000–5,000 | ✅ |
| 45 | Bulk product import + logo watermark tool (ZI Product Studio: Excel/CSV import with profit rule, photo crop/logo/resize ZIP, WooCommerce / Facebook catalog / Shopify CSV) — demo: https://zi-catalog-demo.vercel.app · `45_Bulk_Import_Watermark` | Reseller, dropshipper | 5,000–10,000 | ✅ |
| 46 | FB ad / post designer (ZI Post Designer: 8 templates, 8 Bangla fonts, post/story/cover/ad sizes, PNG/JPG, batch ZIP) — demo: https://zi-designer-demo.vercel.app · `46_FB_Post_Designer` | F-commerce seller | 5,000–10,000 | ✅ |
