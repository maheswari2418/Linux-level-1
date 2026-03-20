# 👤 Linux Task: Create User with Expiry Date

## 📌 Task
Create a user named **ravi** on **App Server 3** with expiry date **2027-03-28**.

---

## 🖥️ Commands

```bash
ssh user@app-server-3
sudo useradd -e 2027-03-28 ravi
id ravi
chage -l ravi
