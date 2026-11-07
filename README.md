# Annual Attendance Record

Hospital staff leave, duty roster and Hijri / English attendance calendar.
Built with Next.js 16 + MongoDB. Deploys to Vercel.

## Quick start (local)

1. Install Node.js LTS (version 20.9 or newer) from https://nodejs.org
2. Copy `.env.example` to `.env.local` and fill in `MONGODB_URI`, `MONGODB_DB`, `JWT_SECRET`
3. In this folder run:

```
npm install
npm run dev
```

4. Open http://localhost:3000 - the first screen creates the **Main Admin** account.

## Features

- 3 admin accounts: 1 Main Admin (all privileges, final approvals) + 2 Admins
- Staff records: name, role, designation, department, phone
- Leave: any date range, 45 days per staff per calendar year (configurable), max 3 staff on leave on the same day (configurable)
- Admin leave requests wait for the Main Admin's approval; pending requests also count towards the limit of 3
- Shifts (Morning / Evening / Night by default, editable) with a 24-hour timeline for every day
- Assign, remove, substitute staff and move staff to another department
- English by default; one click switches to Arabic (right-to-left) with the Hijri (Umm al-Qura) calendar
- Annual sheet per staff per month with CSV export and print
- The app remembers where each admin left off (tab, month, language) in the database

## Who can do what

| Action | Main Admin | Admin (2nd / 3rd) |
|---|---|---|
| Add / edit staff | yes | yes |
| Duty roster: assign, substitute, transfer | yes | yes |
| Create / edit shifts | yes | yes |
| Assign leave | approved immediately | sent for approval |
| Approve / reject leave | yes | no |
| Remove staff | yes | sends a removal request |
| Delete shifts, manage admins, change settings | yes | no |

## Environment variables

| Name | Meaning |
|---|---|
| `MONGODB_URI` | MongoDB Atlas connection string |
| `MONGODB_DB` | Database name (created automatically), e.g. `annual_attendance` |
| `JWT_SECRET` | Long random text (32+ characters) used to sign login cookies |

Generate a secret: `node -e "console.log(require('crypto').randomBytes(32).toString('hex'))"`

## Deploy to Vercel

Push the project to GitHub, import it in Vercel, add the three environment variables, click Deploy.
In MongoDB Atlas > Network Access, allow `0.0.0.0/0` so Vercel can connect.

This approach helps me practice both understanding Devlopment and professional Git workflows.

---

## 🧠 Skills Being Developed

This repository focuses on building practical skills in:

* **Bash / Shell Scripting**
* **Linux Administration**
* **Command-Line Automation**
* **File & User Management**
* **Conditional Logic & Loops**
* **Debugging & Problem Solving**
* **Git & GitHub**
* **DevOps Automation Principles**

---

## 🔐 Scripting Best Practices

Scripts in this repository are developed with a focus on:

* **Readability & Maintainability**
* **Reusability**
* **Clear Documentation**
* **Input Validation**
* **Error Handling**
* **Troubleshooting & Debugging**

The repository also follows **professional Git practices**, including meaningful commits and organized branch management.

---

## 📊 Repository Philosophy

```text
Learn → Practice → Build → Test → Debug → Document → Commit → Improve
```

> **Every script is a step toward mastering Linux, Shell scripting, and DevOps automation.**

---

## 👨‍💻 Author

### Engg. Sayed Abdul Qayum

**Aspiring DevOps Engineer** | Building skills in **Linux, Shell Scripting, AWS, Git, CI/CD, Docker, Terraform, Ansible and Kubernetes**.

---

## 📌 Repository Status

🚧 **Active Development**

Continuously updated with new **Linux, Shell scripting, automation, and DevOps** concepts, scripts, and practical exercises.

---

⭐ If you find this repository useful, feel free to **explore, learn, and follow the journey**.

**Learn. Automate. Improve. Repeat. 🚀**

---
 ## Live Demo

[Visit Annual Attendance Record](https://project-annual-attendance-record.vercel.app/)

Testing
Testing-1
Testing-2
Testing-3
Testing-4


