
# Практическая работа по администрированию БД (3)

## Задание:
Необходимо создать приложение хранящую информацию о магазине. Данное приложение должно состоять из трёх компонентов: базы данных PostgreSQL, базы данных mongodb и сервера приложение (API) (Язык программирования используете любой доступный, все библиотеки, фрймворки, утилиты и тд разрешены). API должно выводить и сохранять информацию о товарах в MongoDB, а информацию о работниках хранить в PostgreSQL. 

Каждый компонент должен находится в разных контейнерах. Определите Docker Images для каждого контейнера, включая соответствующие зависимости и конфигурационные файлы. Используйте Docker Compose для запуска контейнеров для MongoDB, PostgreSQL и сервера приложений. 
Для хранения данных PostgreSQL и MongoDB должны быть определены  Docker Volumes. Все значения для подключения и работы с базами данных включая настройки баз данных, такие как имя пользователя, пароль и название базы данных, должны хранится в переменных среды (environment).

Приложение должно реализовывать следующие функции:
- получение списка товаров;
- добавление товара в базу данных;
- удаление товара из базы данных;
- получение списка сотрудников;
- добавление сотрудника в базу данных;
- удаление сотрудника из базы данных.

Используйте Docker Compose для масштабирования сервера приложений. Используйте Docker Compose для обновления версии приложения. Измените версии Docker Images и перезапустите контейнеры, чтобы проверить, что обновление прошло успешно.
Остановите и удалите контейнеры и Docker Volumes, чтобы освободить ресурсы системы.

Стек:
- Python 3.10
- FastAPI
- docker

✔️ Первый запуск
```
docker build . -t admin_api__app:latest  
```


✔️ Запуск docker compose
```
docker compose up --build --force-recreate
```