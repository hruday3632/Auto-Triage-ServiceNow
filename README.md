# Auto-Triage ServiceNow Project

This ServiceNow project automates incident creation, assignment, and email notifications based on custom user intake via Service Portal.

---

## 🔧 Key Features

- Custom table: `x_auto_request` to collect inputs
- Flow Designer-based automation
- Automatic Incident creation from custom table
- Assignment Group auto-assigned (Help Desk)
- Email sent to the caller
- Original record updated with status and linkage
- Fully working on PDI (Xanadu)

---

## 📐 Architecture Overview

1. **Trigger**: Record created in `x_auto_request` table
2. **Flow Designer**:
   - Creates Incident
   - Updates the original request record
   - Sends an email using Gmail SMTP
3. **Interface**:
   - Record Producer used in Service Portal
   - Selectable caller, description, and short description fields
   - Email confirms with incident number and assignment group

---

## 🛠 Technologies Used

- ServiceNow PDI (Xanadu version)
- Flow Designer
- Record Producer
- Email Notifications (via Gmail SMTP)
- Scoped Application
- Assignment group: Help Desk

---

## 📸 Screenshots

Screenshots available in `/screenshots` folder:
- Flow trigger
- Create Incident step
- Email logs
- Custom request record before/after
- Service Portal form

---

## 🚀 How to Run This

1. Clone this repo or import definitions into your PDI
2. Configure your Gmail App Password in Email Properties
3. Submit a new request using the Service Portal
4. Validate:
   - Incident created
   - Assignment group set
   - Email received
   - Auto-request record updated

## Scoped App Export

This repository includes the full scoped application as an update set.

✅ Import this file: `AutoTriageApp_UpdateSet.xml`  
📍 Go to: `System Update Sets > Retrieved Update Sets`  
🡒 Use “Import XML”, then Preview + Commit.

The app includes:
- Custom table: `auto_request`
- Flow Designer logic to create, assign, notify
- Record Producer integration
- Email integration using SMTP


---

## 🙋 Author

**D H Hruday Mohan**  
ServiceNow Developer 
[GitHub Profile](https://github.com/hruday3632)
