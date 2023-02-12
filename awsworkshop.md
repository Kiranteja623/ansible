* create a vpc with one subnet public
* create an ec2 instance in public subnet ensure the security group rules is open for port 22 80
* create ec2 with predefined private ip
* create an ec2 instance and ensure you you execute the following coomands
```
sudo apt update
sudo apt install apache2 stress -y
sudo apt install php libapache2-mod-php php-mysql -y
sudo -i
echo "<?php phpinfo(); ?>" > /var/www/html/info.php
```