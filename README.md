# AWS EC2 Nginx Web Server

## Technologies Used

- AWS EC2 (Ubuntu)
- Nginx
- HTML5
- Linux Commands
- Git & GitHub

---

# Step 1: Launch EC2 Instance

1. Login to AWS Console.
2. Navigate to EC2 Dashboard.
3. Click **Launch Instance**.
4. Select **Ubuntu Server 24.04 LTS**.
5. Choose **t2.micro**.
6. Create or select an existing Key Pair.
7. Allow:
   - SSH (Port 22)
   - HTTP (Port 80)
8. Launch the instance.

---

# Step 2: Connect to EC2

```bash
ssh -i your-key.pem ubuntu@<Public-IP>
```

Or connect using EC2 Instance Connect.

---

# Step 3: Update the Server

```bash
sudo apt update
sudo apt upgrade -y
```

---

# Step 4: Install Nginx

```bash
sudo apt install nginx -y
```

Verify installation:

```bash
sudo systemctl status nginx
```

Start Nginx if required:

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

---

# Step 5: Replace Default Nginx Webpage

Navigate to:

```bash
cd /var/www/html
```

Edit the default page:

```bash
sudo nano index.html
```

Replace the default HTML with your custom HTML page.

Restart Nginx:

```bash
sudo systemctl restart nginx
```

---

# Step 6: Verify Website

Open your browser and visit:

```
http://<EC2-Public-IP>
```

Example:

```
http://13.234.xxx.xxx
```

---

# Useful Linux Commands

Update packages

```bash
sudo apt update
```

Upgrade packages

```bash
sudo apt upgrade -y
```

Install Nginx

```bash
sudo apt install nginx -y
```

Check Nginx status

```bash
sudo systemctl status nginx
```

Restart Nginx

```bash
sudo systemctl restart nginx
```

Check disk usage

```bash
df -h
```

Check memory usage

```bash
free -h
```

Check CPU usage

```bash
top
```

Check public IP

```bash
curl ifconfig.me
```

---
# Git Commands Used

Initialize repository

```bash
git init
```

Add files

```bash
git add .
```

Commit changes

```bash
git commit -m "Initial Commit"
```

Add remote repository

```bash
git remote add origin < repo url >

Push code

```
bash
git branch -M main
git push -u origin main
```


