**Готовое окружения Docker для 1C-Bitrix(Битрикс) CMS**

**Основные возможности:**

В зависимости от требований, проект на Битрикс может разворачиваться из бэкапа или клонироваться из репозитория(приватного или открытого). Обычно из проектов на Битрикс исключается директория /bitrix. Поэтому при развертывании из репозитория, после клонирвоания, скачивается бэкап проекта и из него берется директория /bitrix тем самым получается готовое рабочее окружение для разработки. Последним шагом необходимо только развернуть базу данных (дамп .sql будет в корне /src)

1) При установленнном флаге **INIT_PROJECT=true**
Проект автоматически загружается и разворачивается из бэкапа сайта битрикса вида:
http://****/bitrix/backup/example.com_20180415_103035_full_bb768f2f.tar.gz

2) При установленнном флаге **INIT_PROJECT=false**
Проект клонируется из репозитория после чего доустанавливается директория /bitrix из бэкапа

**Окружение (похоже на конфигурацию BitrixVM)**

- Nginx
- Apache
- php-pfm
- mysql
- phpMyAdmin

**Чтобы начать работу необходимо:**

1) Установить Docker **https://docs.docker.com/install/**

2) Клонировать репозиторий 

3) Переименовать файл **.env.template** в **.env**

4) Заполнить параметры файла **.env** согласно инструкции

5) Запустить проект командой **docker-compose up --build -d**

6) 🍺🍺🍺 