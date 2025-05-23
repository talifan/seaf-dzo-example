Файл описывает технологическую архитектуру: регионы, ЦОДы, зоны доступности, офисы, окружения, стенды, кластеры, серверы, сети, устройства, лицензии и т.д.
1. География и инфраструктура
   | Категория | Кол-во | Назначение/Примеры |
   |-------------------|--------|-----------------------------------------------------------------------------------|
   | Регионы | 1 | flix.dc_region.russia — регион Россия |
   | Зоны доступности | 1 | flix.dc_az.moscow — Москва |
   | ЦОДы | 3 | Sber Cloud DC, VK DC, Cloud.ru |
   | Офисы | 1 | Головной офис (Берёзовый бульвар, д.14) |
2. Окружения и стенды
   | Категория | Кол-во | Назначение/Примеры |
   |---------------|--------|------------------------------------------|
   | Окружения | 3 | dev, test, prod |
   | Стенды | 5 | dev, intest, ntest, prod, preprod |
3. Кластеры виртуализации
   | Кластер | Тип/Описание | Зона | Серверы/Компоненты |
   |--------------------------------|-------------------------------------|------|----------------------------|
   | cloud.01, cloud.02, vk.01 | Виртуализация в облаках Cloud/VK | Москва | 6 физических серверов, app-компоненты |
4. Сетевые устройства
   | Тип устройства | Кол-во | Модели/Назначение |
   |----------------|--------|--------------------------|
   | FortiGate | 4 | 4800F, пограничные маршрутизаторы |
   | Cisco ASR | 3 | 1001-X, маршрутизаторы |
5. Сети и сегменты
   | Категория | Кол-во | Примеры/Назначение |
   |-------------------|--------|-----------------------------------|
   | Сегменты сети | 9 | DMZ, Internal DC, Office, Inet Edge |
   | Внутренние сети | 4 | LAN 192.168.x.0 |
   | Внешние сети (WAN)| 5 | WAN 1.1.1.0/28, 2.2.2.0/28 и др. |
   | DMZ | 1 | 10.10.10.0/24 |
6. Сетевые линки
   | Линк | Тип | Провайдер | Пропускная способность |
   |---------------------|--------------------|-----------|------------------------|
   | vk_cloud | VPN Site-to-site | МТС | 100 |
   | cloud_hq | VPN Site-to-site | МТС | 100 |
   | cloud_laptop | SSL VPN | МТС | 10 |
7. Серверы
   Физические серверы
   | Кол-во | Модель | Назначение/Примечания |
   |--------|---------------|------------------------------|
   | 8 | HP DL360 G8 | 6 в кластере виртуализации, 2 с SDS |
   Виртуальные серверы
   | Кол-во | Назначение/Примечания |
   |--------|------------------------------|
   | 12 | Авторизация, k8s, backup, monitoring |
8. Хранилища
   | Тип | Кол-во | Примеры/Назначение |
   |--------------------|--------|----------------------------|
   | Аппаратные СХД | 1 | IBM Storwize 7000 |
   | Программные СХД | 1 | CEPH (SDS) |
   | Объектные хранилища| 2 | S3 Cloud, S3 VK |
9. Кластеры
   | Тип | Кол-во | Назначение/Примеры |
   |-------------|--------|----------------------------|
   | Wildfly | 1 | Приложения: catalog, canals|
   | K8s | 1 | Приложение: payments |
10. Сервисы
    | Сервис | Кол-во | Назначение/Примеры |
    |----------------|--------|----------------------------|
    | Мониторинг | 1 | Zabbix |
    | Бэкап | 1 | Acronis |
    | Лицензии | 2 | Acronis, CryptoPro |
11. Клиентские устройства
    | Тип устройства | Кол-во | Назначение |
    |----------------|--------|--------------------|
    | Ноутбуки | 1 | Внешние устройства сотрудников |