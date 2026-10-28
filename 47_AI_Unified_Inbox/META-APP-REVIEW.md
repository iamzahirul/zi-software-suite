# Meta App Review — A-One Gadgets Inbox

App: **A-One Gadgets Inbox** (ID 1921147092221153) · Business portfolio: **A One Gadgets** (1830367847998947)
Where: developers.facebook.com → your app → **Publish / App Review** → request the permissions below.

Meta reviewers read English. Write every answer in English, make the recordings in English (or with English captions), and send the test messages in English so the reviewer understands them.

---

## 0. Before you start (one-time checks)

| Item | Value | Status |
|---|---|---|
| Privacy Policy URL | https://aonegadgets.com/inbox/privacy.php | live ✓ |
| Data Deletion URL | https://aonegadgets.com/inbox/data-deletion.php | live ✓ |
| App icon 1024×1024 | uploaded | ✓ |
| Category | Business and Pages | check in App settings → Basic |
| Business verification | Security Center → upload trade licence + utility bill/bank statement | **you — in progress** |
| Domain | www.aonegadgets.com | verified ✓ |
| Reviewer login for the inbox | create in Inbox → **Team** → add agent "Meta Reviewer" with its own email + a new password | **you** |

> Never show the App Secret, Page token, WhatsApp token or Gemini key on screen. Open Settings only on tabs where they are hidden, or blur them while editing the recording.

---

## 1. `pages_messaging` (Messenger) — the important one

**How will your app use this permission? (paste)**

> A-One Gadgets (aonegadgets.com) is an electronics shop in Dhaka, Bangladesh. Our app is our own customer-support inbox, used only by our staff for our own Facebook Page "A One Gadget". When a customer sends a message to our Page, the message arrives in our inbox through the Messenger webhook. An AI assistant answers common questions (product availability, price, delivery charge) using our own product catalogue, and our staff can read the conversation and reply themselves from the same screen. Replies are sent with the Send API inside the 24-hour standard messaging window, only in response to a customer's message. We do not send promotional or unsolicited messages. The AI hands the chat to a human whenever the customer asks for a person, complains, or the AI is unsure. Customers can ask us to delete their data at https://aonegadgets.com/inbox/data-deletion.php.

**Screen recording plan (1½–3 minutes)**

1. Browser: open https://aonegadgets.com/inbox/admin/ and log in. *(caption: "Our staff inbox")*
2. Click **Settings → Messenger**: show the connected Page name "A One Gadget" (tokens hidden). *(caption: "Our Page is connected")*
3. On a phone (or a second account), open the **A One Gadget** Page → press **Message** → send:
   `Hi, do you have a 20000mAh power bank? What is the price?`
4. Back in the inbox: the chat appears under **Messenger**. Open it — the customer's message is there. *(caption: "Message received via webhook")*
5. Wait a few seconds: the AI reply with product cards appears in the inbox. Switch to the phone: the same reply is in Messenger. *(caption: "Reply sent with the Send API")*
6. In the inbox, type a reply yourself: `Thank you! A team member here — anything else I can help with?` → Send. Show it arriving in Messenger. *(caption: "Staff can reply directly")*
7. In the phone send `I want to talk to a person`. Show the inbox: AI turns off and a note says the chat was handed to the team. *(caption: "Human handoff")*

**Notes for the reviewer (paste)**

> 1. Log in at https://aonegadgets.com/inbox/admin/ with the reviewer account below.
> 2. Send any message to our Facebook Page "A One Gadget" (https://www.facebook.com/aonegadgetsbd).
> 3. The message appears in the inbox under the "Messenger" filter and is answered automatically within a few seconds; you can also type a reply in the inbox.
> Login: (reviewer email) / (reviewer password)

If the dashboard also lists **`pages_manage_metadata`** and **`pages_show_list`** for the Messenger use case, request them too with:

- **pages_manage_metadata:** "Used to subscribe our app to our own Page's webhooks (messages, message_echoes, messaging_postbacks) so customer messages reach our inbox." — recording: steps 2–4 above.
- **pages_show_list:** "Used to let our admin choose which of their Pages to connect to the inbox." — recording: the Page picker when generating the Page token in the Messenger settings.

---

## 2. WhatsApp — `whatsapp_business_messaging` + `whatsapp_business_management`

> Do this **after** business verification is approved. First I set up the **Connect WhatsApp** button (Facebook Login for Business configuration ID); you record while it is used.

**whatsapp_business_messaging — how will your app use it? (paste)**

> Our app is A-One Gadgets' own customer-support inbox. Customers message our WhatsApp Business number (+880 1310-902812). Their messages arrive in our inbox through the WhatsApp Cloud API webhook, and our AI assistant or our staff reply from the same inbox within the 24-hour customer service window. We also show messages our staff send from the WhatsApp Business app (coexistence), so the conversation stays complete. We do not send marketing or bulk messages.

**whatsapp_business_management — how will your app use it? (paste)**

> Used during onboarding (Embedded Signup) to read our WhatsApp Business Account and phone number, subscribe our app to the account's webhooks, and sync contacts and recent chat history from our WhatsApp Business app (coexistence) into our inbox. It is only used for our own business account.

**Screen recording plan (2–3 minutes)**

1. Inbox → **Settings → WhatsApp** → press **Connect WhatsApp**. *(caption: "Embedded Signup")*
2. In the Meta popup choose the business **A One Gadgets** → "Connect your existing WhatsApp Business app" → scan the QR code with the phone's WhatsApp Business app → finish. *(caption: "Coexistence onboarding")*
3. Inbox shows "WhatsApp connected" and the number. Older chats appear under **WhatsApp**. *(caption: "Contacts + history synced")*
4. From another phone send WhatsApp: `Hello, is the A69 PD 20W charger in stock?` Show it in the inbox and the AI reply arriving on that phone. *(caption: "Receive + reply via Cloud API")*
5. In the WhatsApp Business app on the shop phone, type a reply. Show it appearing in the inbox too. *(caption: "Replies from the phone app are mirrored")*

---

## 3. After approval

1. App Dashboard → **Publish** → switch the app to **Live**. Only then do ordinary customers' Messenger messages reach the inbox (today only people with a role on the app do).
2. Delete the "Meta Reviewer" agent from Inbox → Team once the review is done.

## Common rejection reasons (avoid these)

- Recording does not show **both** the message arriving in the app **and** the reply arriving in Messenger/WhatsApp.
- UI or messages only in Bangla without captions.
- Secrets visible on screen.
- Reviewer login missing or not working.
- Privacy policy URL not reachable or not mentioning Facebook/WhatsApp data (ours covers both).
