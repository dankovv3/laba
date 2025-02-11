# Юнусова Ильмира К-ИСП-39-2


Вводим команду  _sudo yum install wget_ она устанавливает утилиту wget в системах

Она используется для установки утилиты **wget**     


![image](https://github.com/user-attachments/assets/a08f9d7c-3a60-44c8-ba96-dc90fe3f7a3b)

Вышла ошибка, ввела команду _su root_ далее _vi /etc/sudoers_ и добавляю себе права в файле

![image](https://github.com/user-attachments/assets/6cd9e547-7ae2-4da8-90b9-4b54109ccfbf)


Установила **wget**


 _wget — мощная утилита для загрузки файлов_

![image](https://github.com/user-attachments/assets/24aded6d-a101-49af-ae9b-1139d1bdf3fb)


Ввела команду _sudo yum install curl_ для установки утилиты curl

_Утилита **curl** нужна для передачи данных с использованием различных протоколов_

![image](https://github.com/user-attachments/assets/6187fc0b-4127-4456-84fd-e100986616d5)


Ввела команду _sudo wget -P /etc/yum.repos.d/ https://download.docker.com/linux/centos/docker-ce.repo_

Эта команда скачивает файл репозитория Docker с сайта, это необходимо для установки Docker

![image](https://github.com/user-attachments/assets/4bed3310-f14d-4592-9989-f42ba831d899)


Скачала сам докер _sudo yum install docker-ce docker-ce-cli containerd.io_

![image](https://github.com/user-attachments/assets/dc0d2dd3-4a2b-4f6b-b582-105bd895892d)


Ввела команду _sudo systemctl enable docker --now_ что бы запустить Doker 

**Эта команда настраивает автозапуск Docker при старте системы**

![image](https://github.com/user-attachments/assets/c49bfd42-da32-483e-98f5-faf52e32ba3a)


