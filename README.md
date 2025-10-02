Perfect 👍 Let’s make a clean, professional **README.md** for your project.
You can copy-paste this into your repo root file as `README.md`.

---

# 📧 Personalized Cold Email Automation (n8n Workflow)

This project is an **n8n workflow** that automates sending **personalized cold emails** using customer data stored in Google Sheets. It extracts business details, creates tailored email templates, and sends emails via Gmail automatically on a schedule.

---

## 🚀 Features

* 🔄 **Automated Workflow**: Runs on a schedule (daily/hourly, as configured).
* 📊 **Google Sheets Integration**: Reads customer/business data directly from Google Sheets.
* ✍ **Personalized Emails**: Dynamically generates subject lines and messages tailored to each business.
* 📬 **Gmail Integration**: Sends emails directly from your Gmail account.
* 🕒 **Smart Delays**: Adds wait time between emails to avoid spam filters.
* ✅ **Status Tracking**: Updates Google Sheet with email delivery status.

---

## 📂 Project Structure

```
n8n-email-workflow/
│── workflow.json   # Exported n8n workflow
```

---

## ⚡ How It Works

1. **Schedule Trigger** → Runs the workflow at the set time.
2. **Read Google Sheet** → Fetches business data (name, type, email, product/service, platform).
3. **Extract Data** → Parses the sheet data into structured JSON.
4. **Check Data** → Ensures required fields (email, name, etc.) exist.
5. **Create Personalized Email** → Generates subject + message dynamically using JavaScript logic.
6. **Send Email (Gmail)** → Sends the email to the business.
7. **Wait Between Emails** → Adds delay before next email to reduce spam risk.
8. **Update Sheet** → Marks status as *Sent* or *Invalid Email*.

---

## 📋 Prerequisites

* [n8n](https://n8n.io/) account (self-hosted or cloud)
* Gmail account (for sending emails)
* Google Sheets (for storing customer data)

---

## 🛠 Setup Instructions

1. Clone this repo:

   ```bash
   git clone https://github.com/<your-username>/n8n-email-workflow.git
   cd n8n-email-workflow
   ```
2. Open [n8n](https://n8n.io/) → **Import workflow** → Upload `workflow.json`.
3. Connect your **Gmail** and **Google Sheets** credentials in n8n.
4. Edit your Google Sheet with the following columns:

   ```
   Business Name | Business Type | Platform | Product/Service | Location | Email
   ```
5. Customize the email body & subject logic inside the **"Create Personalized Email"** function node.
6. Activate the workflow → n8n will start sending personalized cold emails automatically.

---

## 📧 Example Email Format

**Subject:**

```
Loved your Jeans collection on Instagram
```

**Body:**

```
Hi Focus Jeans India,

I came across your Instagram page showcasing your Jeans/Apparel, and I really liked how you present your collection. It's clear that many people are noticing your products in India.

One thing I noticed is that you don’t seem to have a dedicated website. A website can help you display your full catalog, take online orders, and reach more customers outside Instagram.

I’m a freelancer helping small businesses like yours set up simple, affordable websites that attract more customers. If you'd like, I can share some quick ideas tailored to your fashion business.

Would you be open to a quick chat?

Best regards,  
Mohamed  
abc@gmail.com / +91-XXXXXXXXXX
```

---

## 🔧 Customization

* Edit **senderName** and **senderContact** in the **Code node**.
* Modify **business-type-specific subject lines** for different industries.
* Adjust **email wait time** in the **Wait Between Emails node**.

---

## 🤝 Contributing

Pull requests are welcome! If you have improvements, fork this repo and submit a PR.

---

## 📜 License

MIT License. Free to use and modify.

---

