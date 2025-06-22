Напишем скрипт который потребляет память.

<img width="387" alt="image" src="https://github.com/user-attachments/assets/ff03611c-f648-46bd-bac9-f3d60cd90d6e" />

Проверим работоспособность и как постоянно поедается память.

<img width="873" alt="image" src="https://github.com/user-attachments/assets/8097f1ed-2c1e-4b33-9fab-3404cb571582" />

Создадим зомби процесс через команду
```
bash -c 'sleep 1 & child_pid=$!; echo "CHILD PID: $child_pid"; wait'
```
Найдем зомби процесс

<img width="848" alt="image" src="https://github.com/user-attachments/assets/98c7d046-16c6-4e65-9b27-f23852939727" />


Создание 3 кронтаб записей

1. Ежемесячная очистка кеша Docker:
```
0 3 1 * * docker system prune -af --volumes
```

2. Еженедельная проверка места на диске
```
0 6 * * 0 df -h > /var/log/disk_space_report.log
```

3. Еженедельно обновлять пакеты и чистить кэш
```
0 3 * * 1 apt update && apt upgrade -y && apt autoremove -y
```
