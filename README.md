# 📧 Shipout sender

**A bulk HTML email sender** with attachments, multiple SMTP support, delivery logging, CLI interface.

---

## ✅ Features

* Send HTML emails to many recipients
* Attach any files (PDF, DOCX, etc.)
* Use multiple SMTPs — auto-tries the next if one fails
* Keeps track of sent and failed emails
* Easy-to-edit config and input files

---

## 📂 All in zip

| File Name      | Description                              |
| -------------- | ---------------------------------------- |
| `shipout.exe / .app`      | The app                      |
| `emails.txt`   | List of emails to send to (one per line) |
| `smtps.txt`    | Your SMTP logins (format below)          |
| `config.txt`   | Subject and reply email settings         |
| `email.html`   | The HTML content of your email           |
| `attachments/` | Folder for any attachments. No attachment no problem.
| `sent.txt`     | Auto-generated list of sent emails       |
| `fail.txt`     | Auto-generated list of failed emails     |

---

## ✏️ How to Edit Input Files

### 1. `emails.txt`

Add one recipient email per line:

```
alice@example.com
bob@example.com
charlie@example.com
```

---

### 2. `smtps.txt`

Each line is:

```
SMTP_HOST:PORT|EMAIL|PASSWORD
```

Example:

```
smtp.gmail.com:465|yourname@gmail.com|yourpassword
smtp.mailtrap.io:2525|test@domain.com|yourpassword
```

✅ You can add more than one — if the first fails, the tool tries the next.

---

### 3. `config.txt`

Set your subject and reply-to email:

```
subject=Test Mail from Underground
replyto=admin@example.com
```

---

### 4. `email.html`

Paste or edit your HTML message here. Example:

```html
<html>
  <body>
    <h1>Hello!</h1>
    <p>This is a test message from <b>underGround sender</b>.</p>
  </body>
</html>
```

---

### 5. `attachments/`

Put any files you want to attach inside the `attachments` folder.
Example:

* `invoice.pdf`
* `terms.docx`

They will be attached to every email.

---

## ▶️ How to Run

### 1. Open the app:

You will see a banner:

```
underGround sender...
⚡ Press ENTER to begin...
```

Press ENTER to start sending emails.

---

## 📝 What Happens After?

* Emails that are sent successfully → saved in `sent.txt`
* Emails that failed → saved in `fail.txt`
* Emails in `emails.txt` are **automatically updated** (successful ones removed)

---

## 🚨 Notes & Tips

* Make sure SMTP credentials are correct
* Gmail users may need to allow “less secure apps” or use an **App Password**
* Avoid spam keywords in your HTML (buy now, free, etc.)
* Test with 1–2 emails first

---

## 👨‍💻 Built by

**underGround red team** was created by the guy gameThe0ry for fast, smart, and reliable bulk messaging.
for any question contact the developer on telegram @gamethe0ry or visit https://undergr0und.com
Use it responsibly.
