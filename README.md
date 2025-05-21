#  راه اندازی نود Blockcast

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

**دانلود ایمیج‌های داکر    و  راه‌اندازی نود**
```
docker compose pull
docker compose up -d
```

**رجیستر نود**

درمرحله  اطلاعات که داده میشه رو  سیو کنید   Hardwar id  -  challenge key -Registration URL


```
docker compose exec blockcastd blockcastd init
```



**رجیستر کردن  نودتون**

با استفاده از این  لینک https://app.blockcast.network?referral-code=zh6QZH      از قسمت پروفایل   دیسکورد و  والتون و توییترتون رو وصل کنید 
بعد از قسمت mange node  اطلاعاتی  که سیو کرده بودید رو میدید و نودتون رو ریجستر میکنید

![image](https://github.com/user-attachments/assets/379beb60-81f4-4799-8941-2b16bea58ba7)



و خروجی  این باید باشه  وضعیت افلاین  به انلاین تغیر کنه 
![image](https://github.com/user-attachments/assets/88fa0348-ddf9-44f9-9b9e-4b7acb074a83)




لینک کانال ما : https://t.me/crypto_treasure_hunt_air





