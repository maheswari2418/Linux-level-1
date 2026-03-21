# 📂 Filter and Copy User-Specific Files with Directory Structure

## 🧾 Problem Statement

Due to an accidental data mix-up, user data was unintentionally mingled on **Nautilus App Server 2** at the `/home/usersdata` location.

To resolve this issue, perform the following:

- Locate all **files (excluding directories)**
- Owned by user **kirsty**
- Within `/home/usersdata`
- Copy them to `/news`
- Preserve the original directory structure

---

## ⚙️ Solution

Execute the following commands on **App Server 2**:

```bash
cd /home/usersdata
find . -type f -user kirsty -exec cp --parents {} /news \;
