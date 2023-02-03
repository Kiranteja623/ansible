OPENMRS
-------

manual steps
-------------
```
sudo apt update
sudo apt install openjdk-11-jdk -y
sudo apt install maven -y
git clone https://github.com/openmrs/openmrs-core.git
cd openmrs-core
mvn clean package
cd openmrs-core/webapp
mvn jetty:run

```
* to check maven version use mvn --version
* for viewing the application use ip:8080/openmrs
 