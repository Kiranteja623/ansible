INSTALL NOPCOMMERCE MANUAL COMMANDS
-----------------------------------
* to  view installation [Refer here](https://docs.nopcommerce.com/en/installation-and-upgrading/installing-nopcommerce/installing-on-linux.html)
manual steps
------------
```
 wget https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
 sudo dpkg -i packages-microsoft-prod.deb
 sudo apt-get update
 sudo apt-get install -y apt-transport-https aspnetcore-runtime-7.0
 sudo apt-get install nginx
 sudo systemctl status nginx
 sudo nano /etc/nginx/sites-available/default
 sudo mkdir /var/www/nopCommerce
 cd /var/www/nopCommerce
 sudo wget https://github.com/nopSolutions/nopCommerce/releases/download/release-4.60.1/nopCommerce_4.60.1_NoSource_linux_x64.zip
 sudo apt-get install unzip
 sudo unzip nopCommerce_4.60.1_NoSource_linux_x64.zip
 sudo mkdir bin
 sudo mkdir logs
 cd ..
 sudo chgrp -R www-data nopCommerce/
 sudo chown -R www-data nopCommerce/
 sudo nano /etc/systemd/system/nopCommerce.service
 sudo systemctl start nopCommerce.service
 sudo systemctl status nopCommerce.service
 sudo systemctl restart nginx
 sudo systemctl status nopCommerce.service

```
* to view the application use public ip/install
![Preview](nopcom(1).png)


app playbook
------------
[Refer here](https://github.com/Kiranteja623/ansible/blob/master/nopcom.yaml)
and page of the app
![Preview](nopcom2.png)



```
1  sudo apt update && sudo apt install software-properties-common && sudo add-apt-repository --yes --update ppa:ansible/ansible && sudo apt install ansible -y
    2  sudo adduser teja
    3  ansible -i host -m ping localhost
    4  vi jdk.yaml
    5  ansible-playbook -i host jdk.yaml
    6  vi jdk.yaml
    7  ansible-playbook -i host jdk.yaml
    8  java --version

---
- name: installing jdk
  hosts: localhost
  become: yes
  tasks:
    - name: installing jdk
      ansible.builtin.apt:
        name: openjdk-17-jdk
        state: present
        update_cache: yes

```

