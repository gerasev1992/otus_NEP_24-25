манипуляции с хранилищем сертификатов Firefox

root@cr-cli:~# mv /usr/lib/firefox/libnssckbi.so .

root@cr-cli:~# ln -s /usr/lib/x86_64-linux-gnu/pkcs11/p11-kit-trust.so /usr/lib/firefox/libnssckbi.so

root@cr-cli:~# scp user@cr-srv:/etc/ca/ca.crt /usr/local/share/ca-certificates

root@cr-cli:~# update-ca-certificates

