Task: Create a user named `yousuf` with a non-interactive shell on App Server 1.

Steps:
1. Login to App Server 1:
```bash
ssh tony@stapp01
```
Type `yes` if prompted, and enter the password from "Details of all Users and Servers".

2. Create the user with a non-interactive shell:
```bash
sudo useradd -s /sbin/nologin yousuf
```
If `/sbin/nologin` doesn’t work, use:
```bash
sudo useradd -s /usr/sbin/nologin yousuf
```

3. Verify the user:
```bash
grep yousuf /etc/passwd
```

Expected output:
```
yousuf:x:1005:1005::/home/yousuf:/sbin/nologin
```

Final command (what lab expects):
```bash
sudo useradd -s /sbin/nologin yousuf
```

Important checks:
- Must be on `stapp01` (App Server 1).
- Username must be exactly `yousuf`.
- Shell must be non-interactive (`nologin`).
