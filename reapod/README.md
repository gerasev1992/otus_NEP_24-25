##манипуляции с хранилищем сертификатов Firefox##

root@cr-cli:~# mv /usr/lib/firefox/libnssckbi.so .

root@cr-cli:~# ln -s /usr/lib/x86_64-linux-gnu/pkcs11/p11-kit-trust.so /usr/lib/firefox/libnssckbi.so

root@cr-cli:~# scp user@cr-srv:/etc/ca/ca.crt /usr/local/share/ca-certificates

root@cr-cli:~# update-ca-certificates

### KEYCLOAK

unzip keycloak-22.0.1

sudo mv keycloak-22.0.1/ /opt/keycloak/

sudo apt install -y openjdk-19-jre

/opt/keycloak/keycloak-22.0.1/bin/kc.sh build --db=postgres

sudo nano /opt/keycloak/keycloak-22.0.1/conf/keycloak.conf

db=mariadb 

db-username=kkuser  

db-password=Qwerty123

db-url=jdbc:mariadb://192.168.3.200/kk      

health-enabled=true

metrics-enabled=true

https-certificate-file=/opt/keycloak/i.crt

https-certificate-key-file=/opt/keycloak/i.key

hostname=key.rea25.ru

https-port=443

### ---||||||||||||||||----------

export KEYCLOAK_ADMIN=admin
export KEYCLOAK_ADMIN_PASSWORD=admin

/opt/keycloak/keycloak-22.0.1/bin/kc.sh start --optimized

sudo touch /lib/systemd/system/keycloak.service
sudo chmod 664 /lib/systemd/system/keycloak.service

### ------------------------------------------------------------------------
Содержимое файла keycloak.service:

[Unit]
Description=Keycloak Server
After=network.target mariadb.service

[Service]
User=keycloak
Group=keycloak
SuccessExitStatus=0 143
ExecStart=/opt/keycloak/keycloak-22.0.1/bin/kc.sh start --optimized

[Install]
WantedBy=multi-user.target

----------------------------------------------------------------------

sudo setcap CAP_NET_BIND_SERVICE=+eip /usr/lib/jvm/java-19-openjdk-amd64/bin/java

sudo systemctl daemon-reload
sudo systemctl enable keycloak.service
sudo systemctl start keycloak.service
sudo systemctl status keycloak.service
