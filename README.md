#  راه انداری نود Blockcast

**نصب داکر** 
```
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done

# Add Docker repository
sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Install Docker Engine
sudo apt-get update
sudo apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Start and enable Docker
sudo systemctl start docker
sudo systemctl enable docker
```
**مخزن Blockcast رو کلون  میکنیم**
```
git clone https://github.com/Blockcast/beacon-docker-compose.git
cd beacon-docker-compose
```

**دانلود ایمیج‌های داکرو  راه‌اندازی نود**
```
docker compose pull
docker compose up -d
```

**رجیستر نود**

درمرحله  اطلاعات که داده میشه ()رو  سیو کنید 

```
docker compose exec blockcastd blockcastd init
```




