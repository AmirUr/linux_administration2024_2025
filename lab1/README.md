# Лабораторная работа 1 
Создал 4 пользователей с помощью:
```
sudo useradd -m -s /bin/bash test1
sudo useradd -m -s /bin/bash test2
sudo useradd -m -s /bin/bash test3
sudo useradd -m -s /bin/bash test4
```

Добавим этих пользователей в группу sudo:

```
sudo usermod -aG sudo test1
sudo usermod -aG sudo test2
```
Добавление файлов в домашний каталог test3

<img width="249" alt="image" src="https://github.com/user-attachments/assets/25293dc8-2344-4ebf-abf1-25fa036772bc" />

Через sudo visudo добавил запись
``` 
test3 ALL=(root) NOPASSWD: /usr/sbin/tcpdump *
```

Проверка работоспособности:

<img width="378" alt="image" src="https://github.com/user-attachments/assets/3e7d8379-14a0-4cee-b478-0dda5ec982bd" />

Создаем группы и назначаем пользователям их:

<img width="341" alt="image" src="https://github.com/user-attachments/assets/8bee4f23-f4ad-4196-8c7b-574b59f17078" />

Далее через sudo visudo добавил строчку %group1 ALL=(ALL:ALL) ALL

Создадим файл и проверим настройки доступа

<img width="384" alt="image" src="https://github.com/user-attachments/assets/b3ad2191-1f03-43e3-8c73-10c31fb87295" />
