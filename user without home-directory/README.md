# 👤 Linux Task: Create Service User

## 📌 Task
Create a user named **mark** on **App Server 3** without a home directory.

---

## 🖥️ Commands

```bash
ssh user@app-server-3
sudo useradd -M mark
id mark
ls /home