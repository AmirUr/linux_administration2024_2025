## Напишем докерфайл

<img width="312" alt="image" src="https://github.com/user-attachments/assets/c286f4a9-a2e3-4216-a8fa-a0e9872562b6" />


## Настроим конфигурацию нашего веб-сервера на NGINX.
1. Добавим количество одновременных соединений в блоке EVENTS.
2. Включим поддержку Mime типов.
3. Настроим прослушивание нашего сервера на 443 порт.
4. Установим корневой каталог для обслуживания наших веб-ресурсов.
5. Добавляем обработку CSS и JS файлов, кеширование ресурсов.


<img src="images/nginx.jpg" alt="nginx.jpg" width="400">

## 5. Билдим и запускаем контейнер с веб-сервером.

<img width="525" alt="image" src="https://github.com/user-attachments/assets/f0f72805-7797-494f-9b71-e68adf18fff9" />




В браузере делаем запрос на localhost:443 и радуемся нашему рабочему сайту

<img src="images/production.jpg" alt="production.jpg" width="400">
