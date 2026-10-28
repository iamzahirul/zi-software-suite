# AI Unified Inbox — সব ইনবক্স এক জায়গায় + AI সেলস এজেন্ট

Messenger, Instagram, WhatsApp আর ওয়েবসাইট চ্যাট — সব এক ইনবক্সে। সাথে Gemini AI এজেন্ট যে নিজে উত্তর দেয়, প্রোডাক্ট দেখায়, অর্ডার নেয়।
**কোনো মাসিক ফি নাই, কোনো paid API নাই।** শুধু নিজের হোস্টিং লাগবে (যেটা আপনার আগেই আছে)।

Developer: **Zahirul Islam (Rasel)** · https://iamzahirul.com

---

## কী কী আছে

| Feature | কীভাবে কাজ করে |
|---|---|
| 📥 এক ইনবক্স | Messenger, Instagram, WhatsApp, Website chat — সব কনভারসেশন একটা লিস্টে। সার্চ, ফিল্টার, unread count, নতুন মেসেজে sound |
| 👥 টিম | Admin / Agent রোল। চ্যাট কাউকে assign করা যায়, internal note (কাস্টমার দেখে না) |
| 🤖 AI এজেন্ট | Google Gemini (free)। কাস্টমারের ভাষায় (বাংলা/Banglish/English) উত্তর দেয় |
| 📸 ছবি / 🎤 ভয়েস | কাস্টমার ছবি বা ভয়েস পাঠালে AI বুঝে ঠিক প্রোডাক্ট খুঁজে দেয় |
| 🛍️ প্রোডাক্ট কার্ড | ছবি + দাম + "অর্ডার করুন" বাটন চ্যাটেই যায় |
| ⚡ ২ ট্যাপে অর্ডার | কার্ডের লিংকে প্রোডাক্ট পেজ, নাম/ফোন/ঠিকানা আগে থেকে ভরা — শুধু Confirm |
| 🧾 বিল চ্যাটে | অর্ডার হলেই বিল কাস্টমারের ইনবক্সে চলে যায় |
| 📦 অর্ডার ম্যানেজমেন্ট | Pending → Confirmed → Packed → Shipped → Delivered, পেমেন্ট (COD/bKash/Nagad), স্টক অটো কমে/ফেরত আসে, প্রিন্ট ইনভয়েস |
| 🚚 Steadfast কুরিয়ার | এক ক্লিকে পার্সেল বুক, ট্র্যাকিং কোড ও প্রতিটা আপডেট কাস্টমারের ইনবক্সে |
| 🔁 ফলো-আপ | দাম দেখে চলে গেলে কয়েক ঘণ্টা পর একবার মনে করিয়ে দেয় |
| 👤 কাস্টমার রেকর্ড | ফোন, ঠিকানা, মোট অর্ডার, মোট খরচ |
| 🌐 যেকোনো সাইটে | এক লাইন `<script>` — HTML, PHP, WordPress সবখানে চলে |

---

## খরচ — সত্যি কথা

| জিনিস | খরচ |
|---|---|
| এই সফটওয়্যার | ফ্রি (আপনার নিজের) |
| Gemini AI | **ফ্রি tier** — API key নিতে কার্ড লাগে না। ছোট/মাঝারি দোকানের জন্য যথেষ্ট। লিমিট শেষ হলে কিছুক্ষণ পর আবার চালু হয় |
| Messenger / Instagram API | **ফ্রি** |
| WhatsApp Cloud API | কাস্টমার মেসেজ দেওয়ার ২৪ ঘণ্টার মধ্যে রিপ্লাই **ফ্রি**। ২৪ ঘণ্টার পরে নিজে থেকে মেসেজ পাঠাতে paid template লাগে — এই সিস্টেম সেটা পাঠায় না |
| Steadfast API | ফ্রি (merchant account লাগবে) |
| হোস্টিং + ডোমেইন | আপনার আগের হোস্টিংই যথেষ্ট |

> ⚠️ Gemini free tier-এ Google আপনার ডাটা তাদের প্রোডাক্ট উন্নত করতে ব্যবহার করতে পারে। কাস্টমারের সংবেদনশীল তথ্য (কার্ড নম্বর, পাসওয়ার্ড) কখনো চায় না — AI-কে সেভাবেই বলা আছে।

---

## ১. যা লাগবে

- cPanel হোস্টিং: **PHP 8.0+**, **MySQL/MariaDB**, cURL (প্রায় সব হোস্টিংয়ে থাকে)
- **HTTPS (SSL)** — Meta webhook শুধু https-এ কাজ করে। cPanel → SSL/TLS Status → AutoSSL (ফ্রি)
- একটা Google account (Gemini key-এর জন্য)
- একটা Facebook Page (+ চাইলে Instagram professional account, WhatsApp Business নম্বর)

## ২. ইনস্টল (১০ মিনিট)

1. এই পুরো ফোল্ডারটা zip করে cPanel → File Manager → `public_html/inbox/` এ আপলোড করে Extract করুন।
   (অন্য নামও দিতে পারেন, যেমন `public_html/chat/`)
2. cPanel → **MySQL Databases** → নতুন database + user বানান, user-কে database-এ **ALL PRIVILEGES** দিন।
3. ব্রাউজারে খুলুন: `https://আপনার-ডোমেইন.com/inbox/install.php`
4. Database তথ্য, দোকানের নাম, admin email/password দিন → **Install**।
5. ✅ ইনস্টল হলে **`install.php` ফাইলটা ডিলিট করে দিন।**
6. লগইন: `https://আপনার-ডোমেইন.com/inbox/admin/`

> Nginx সার্ভার হলে `.htaccess` কাজ করে না — `includes/`, `database/`, `storage/` ফোল্ডার ব্লক করে দিন এবং `uploads/` এ PHP চলা বন্ধ রাখুন।

## ৩. প্রোডাক্ট যোগ করুন

Admin → **Products** → Add product। AI শুধু এখানের প্রোডাক্টই বিক্রি করবে।

টিপস — AI যেন ঠিক প্রোডাক্ট খুঁজে পায়:
- **Search words** ঘরে কাস্টমার যেসব শব্দ লেখে সব দিন: `earphone, এয়ারফোন, হেডফোন, earbuds, black, কালো`
- Description-এ রং, সাইজ, ফিচার, ওয়ারেন্টি লিখুন
- ভালো ছবি দিন (প্রথম ছবিটা কার্ডে যায়)

## ৪. AI চালু করুন (Gemini — ফ্রি)

1. https://aistudio.google.com/apikey → Google দিয়ে লগইন → **Create API key**
2. Admin → Settings → **AI agent** → key পেস্ট → Save → **Test Gemini**
3. Settings → **Shop** এ দোকানের তথ্য লিখুন (সময়, পেমেন্ট, ডেলিভারি, রিটার্ন পলিসি) — AI এখান থেকে উত্তর দেয়।

AI কী করে: প্রোডাক্ট খোঁজে → কার্ড পাঠায় → নাম/ফোন/ঠিকানা নেয় → অর্ডার করে → বিল পাঠায়। রাগী কাস্টমার বা "মানুষের সাথে কথা বলতে চাই" বললে চ্যাট টিমকে দিয়ে দেয় (AI off হয়ে যায়, ইনবক্সে নোট আসে)।

টিমের কেউ চ্যাটে রিপ্লাই দিলে সেই চ্যাটে AI থেমে যায় (Settings থেকে বদলানো যায়)। ইনবক্সের **AI** সুইচ দিয়ে যেকোনো চ্যাটে আবার চালু করা যায়।

## ৫. ওয়েবসাইট চ্যাট (HTML / PHP / WordPress)

Settings → **Website chat** থেকে কোড কপি করুন:

```html
<script src="https://আপনার-ডোমেইন.com/inbox/widget/widget.js" defer></script>
```

- **HTML/PHP সাইট:** প্রতিটা পেজের `</body>` এর আগে বসান (বা footer ফাইলে একবার)।
- **WordPress:** "WPCode" প্লাগিন → Code Snippets → Add → Footer-এ পেস্ট। অথবা Appearance → Theme File Editor → `footer.php` এ `</body>` এর আগে।
- অন্য ডোমেইনের সাইটেও কাজ করে।

`https://আপনার-ডোমেইন.com/inbox/shop.php` — রেডিমেড প্রোডাক্ট পেজ/শপ, এখানেও চ্যাট আছে।

## ৬. Messenger + Instagram কানেক্ট (Meta — ফ্রি)

1. https://developers.facebook.com → **My Apps → Create App** → use case: *Engage with customers on Messenger from Meta* (বা Business টাইপ)।
2. **App settings → Basic** থেকে **App ID** আর **App Secret** কপি করে Settings → Messenger & Instagram এ বসান।
3. App-এ **Messenger** প্রোডাক্ট যোগ করুন → *Messenger API Settings*:
   - **Configure webhooks**: Callback URL = Settings পেজে দেখানো `webhook.php` লিংক, Verify token = Settings পেজে দেখানো টোকেন → Verify and save
   - Webhook fields: `messages`, `messaging_postbacks`, `message_echoes` টিক দিন
   - **Generate access tokens**: আপনার Page কানেক্ট করে **Generate** → টোকেন কপি করে **Page access token** ঘরে বসান → Save → **Test Page token**
   - Page-এর পাশে **Add subscriptions** → একই fields সিলেক্ট করুন
4. **Instagram**: Instagram account টা *Professional* করে Facebook Page-এর সাথে লিংক করুন। Instagram অ্যাপ → Settings → Messages → *Connected tools* → **Allow access to messages** অন করুন। Meta App-এ Instagram প্রোডাক্ট যোগ করে webhook-এ `messages` field subscribe করুন (একই callback URL ও verify token)।
5. **Live করা (জরুরি):** App যতক্ষণ *Development mode*-এ, শুধু app-এর admin/tester-রাই মেসেজ দিলে কাজ করবে। আসল কাস্টমারদের জন্য:
   - **App Review** → `pages_messaging` (আর Instagram হলে `instagram_manage_messages`) এর **Advanced Access** চান — ফ্রি, ভিডিও ডেমো দিতে হয়
   - **Business verification** করতে হতে পারে
   - তারপর App Mode → **Live**

## ৭. WhatsApp কানেক্ট (Cloud API — রিপ্লাই ফ্রি)

1. একই Meta App-এ **WhatsApp** প্রোডাক্ট যোগ করুন → *API Setup*।
2. নিজের নম্বর যোগ করুন (এই নম্বর সাধারণ WhatsApp অ্যাপে চালু থাকা যাবে না, অথবা Meta-র "coexistence" অপশন ব্যবহার করুন)। **Phone number ID** কপি করুন।
3. স্থায়ী টোকেন: business.facebook.com → Settings → **System users** → Add (Admin) → *Generate token* → আপনার App সিলেক্ট করে `whatsapp_business_messaging` ও `whatsapp_business_management` পারমিশন দিন → Expiry: Never।
4. Settings → **WhatsApp** এ Phone number ID ও token বসান → Save → **Test WhatsApp**।
5. WhatsApp → *Configuration* → Webhook: একই Callback URL ও Verify token → `messages` field subscribe।

> Meta কখনো কখনো WhatsApp Manager-এ payment method যোগ করতে বলে — কাস্টমারের মেসেজের ২৪ ঘণ্টার মধ্যে রিপ্লাই তারপরও ফ্রি।

## ৮. Steadfast কুরিয়ার

Steadfast merchant panel → **API** → Api-Key ও Secret-Key কপি করে Settings → Courier এ বসান → **Test Steadfast**।
অর্ডার পেজে **📦 Book with Steadfast** চাপলেই পার্সেল বুক হয়, কাস্টমার ট্র্যাকিং কোড পায়, ডেলিভারি হলে অর্ডার অটো *Delivered* হয়।
Pathao/RedX/অন্য কুরিয়ার: অর্ডার পেজে হাতে ট্র্যাকিং কোড লিখে দিলেও কাস্টমার মেসেজ পাবে।

## ৯. Cron (ফলো-আপ + কুরিয়ার আপডেট)

cPanel → **Cron Jobs** → Every 10 minutes (`*/10 * * * *`) → Settings → *Cron & system* পেজের কমান্ডটা পেস্ট করুন:

```bash
wget -q -O /dev/null "https://আপনার-ডোমেইন.com/inbox/cron.php?key=আপনার_CRON_KEY"
```

## ১০. প্রতিদিনের ব্যবহার

- **Inbox:** বাম পাশে সব চ্যাট (🔵 Messenger, 🟣 Instagram, 🟢 WhatsApp, ⚫ Website)। ক্লিক করে রিপ্লাই। 📷 ছবি, 🛍️ প্রোডাক্ট কার্ড পাঠানো যায়।
- **Internal note:** টিমের জন্য নোট — কাস্টমার দেখে না।
- **AI সুইচ:** চ্যাট-বাই-চ্যাট AI on/off।
- **Assign:** ড্রপডাউন থেকে টিমের কাউকে দিন। "Mine" ফিল্টারে নিজের চ্যাট।
- **ডান পাশে:** কাস্টমারের নাম/ফোন/ঠিকানা, আগের অর্ডার, **+ New order**।
- **Orders:** আজকের অর্ডার/সেল, স্ট্যাটাস বদলালে কাস্টমার অটো মেসেজ পায় (Settings → Follow-up & alerts এ টেক্সট বদলান)।

## সমস্যা হলে

| সমস্যা | সমাধান |
|---|---|
| Meta webhook verify হচ্ছে না | URL `https://` দিয়ে কিনা, verify token হুবহু কপি হয়েছে কিনা দেখুন |
| মেসেজ আসছে না | Page-এ *Add subscriptions* করেছেন? App Live mode এ? `storage/app.log` দেখুন |
| "invalid signature" log-এ | Settings-এ App Secret ভুল |
| AI উত্তর দিচ্ছে না | Settings → AI → Test Gemini। ইনবক্সে হলুদ নোটে কারণ লেখা থাকে (যেমন free limit শেষ) |
| AI ভুল প্রোডাক্ট দেখাচ্ছে | প্রোডাক্টে Search words (বাংলা + English) আর description ভালো করে লিখুন |
| "Not delivered" ⚠ | মাউস রাখলে কারণ দেখায়। সাধারণত ২৪ ঘণ্টা পার হয়ে গেছে বা টোকেন expire |
| Steadfast error | API key/secret ঠিক আছে কিনা, ফোন নম্বর ১১ ডিজিট কিনা |

## নিরাপত্তা

- ইনস্টলের পর `install.php` ডিলিট করুন
- Webhook App Secret দিয়ে verify হয় — App Secret অবশ্যই দিন
- পাসওয়ার্ড hash করা, সব ফর্মে CSRF সুরক্ষা, আপলোড ফোল্ডারে কোড চলে না
- প্রোডাক্ট কার্ডের অর্ডার লিংকে কাস্টমারের নাম/ফোন/ঠিকানা আগে থেকে ভরা থাকে — লিংক শুধু সেই কাস্টমারকেই পাঠানো হয়

## ফোল্ডার

```
admin/      টিম প্যানেল (Inbox, Orders, Products, Customers, Team, Settings)
api/        ইনবক্স ও ওয়েবসাইট চ্যাটের JSON API
includes/   মূল কোড (AI, চ্যানেল, অর্ডার, কুরিয়ার)
widget/     ওয়েবসাইট চ্যাট উইজেট
webhook.php Meta webhook (Messenger + Instagram + WhatsApp)
shop.php    প্রোডাক্ট পেজ + অর্ডার ফর্ম
cron.php    ফলো-আপ + কুরিয়ার স্ট্যাটাস
```
