# Юнусова Ильмира К-ИСП-39-2

![image](https://github.com/user-attachments/assets/ad7966b5-9668-4f1a-a012-a092ae46f8b5)

# Docker Compose

- установка гостевых дополнений в виртуальную машину с ос oracle linux

![image](https://github.com/user-attachments/assets/11941d7f-206a-4075-84d7-e5c543a15e7f)

- `sudo yum install wget`  устанавливает утилиту wget в системах

- `sudo yum install curl` устанавливает утилиту curl в системах
  
![image](https://github.com/user-attachments/assets/3abce5f2-b4b4-4b96-8634-08d7203d739e)

- `sudo wget -P /etc/yum.repos.d/ https://download.docker.com/linux/centos/docker-ce.repo` команда скачивает файл репозитория Docker с сайта, это необходимо для установки Docker

![image](https://github.com/user-attachments/assets/3ada9db2-4b04-42aa-9918-3fb89de64c4f)

- `sudo yum install docker-ce docker-ce-cli containerd.io` скачивание докера

![image](https://github.com/user-attachments/assets/3648fad2-23d1-49c1-a0cd-15548bcb31e0)

![image](https://github.com/user-attachments/assets/4a738989-cd4c-4aff-b4ac-54eb27169af2)

- `COMVER=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep 'tag_name' | cut -d\" -f4)` получение последнего докера

![image](https://github.com/user-attachments/assets/5448a9d2-1984-4be6-a3c2-8985c5d06079)

- `sudo curl -L "https://github.com/docker/compose/releases/download/$COMVER/docker-compose-$(uname -s)-$(uname -m)" -o /usr/bin/docker-compose` загрузка и установка последней версии докера

![image](https://github.com/user-attachments/assets/14f659fb-4c40-4b19-855d-cd1de7df4192)

- `sudo chmod +x /usr/bin/docker-compose` файл докера становится исполняемым

- `docker compose --version` смотрим версию нашего докера

![image](https://github.com/user-attachments/assets/6da0ceb9-c89f-4703-946d-5aacb10a7dc0)

- `ls -l /usr/bin/docker-compose` файл стал исполняемым

![image](https://github.com/user-attachments/assets/b0375637-91e6-400f-a232-67c8cb4fb1f0)

- `git clone https://github.com/skl256/grafana_stack_for_docker.git` 
выполняем клонирование удаленного репозитория git

![image](https://github.com/user-attachments/assets/5533cef0-7b0e-4583-b0f4-ee5e59ffb66c)

- `cd grafana_stack_for_docker смена директории

![image](https://github.com/user-attachments/assets/cd2b0fb2-41ee-4d08-9c85-22f2fa3e7149)

- `sudo mkdir -p /mnt/common_volume/swarm/grafana/config` выполняет создание директории (папки) с указанным путем

- `sudo mkdir -p /mnt/common_volume/grafana/{grafana-config,grafana-data,prometheus-data}` создает несколько директорийвнутри указанного пути.

- `sudo chown -R $(id -u):$(id -g) {/mnt/common_volume/swarm/grafana/config,/mnt/common_volume/grafana}` все файлы и каталоги в указанных директориях будут переданы текущему пользователю

- `touch /mnt/common_volume/grafana/grafana-config/grafana.ini файл grafana.ini` уже существует, команда обновит его временные метки

- `cp config/* /mnt/common_volume/swarm/grafana/config/`  команда копирует все файлы и подкаталоги из директории config в директорию /mnt/common_volume/swarm/grafana/config/.

- `mv grafana.yaml docker-compose.yaml` команда переименовывает файл grafana.yaml в docker-compose.yaml

![image](https://github.com/user-attachments/assets/649ecfce-02bd-43e7-9031-6aba88363cb2)

- `sudo docker compose up -d` создает и запускает контейнеры в фоновом режиме

![image](https://github.com/user-attachments/assets/02ffdd8f-6593-4761-a836-740aa88400c8)

![image](https://github.com/user-attachments/assets/814735e3-2833-4508-823b-770346b3eef0)

- `sudo vi docker-compose.yaml` команда открывает файл docker-compose.yaml в текстовом редакторе vi

![image](https://github.com/user-attachments/assets/fb7054f6-2fc7-4187-a97b-78c9a01c1596)

![image](https://github.com/user-attachments/assets/ada7b72b-736d-46c7-bf85-4d78fc4e514b)

- `pwd` вывод полного пути текущего каталога

![image](https://github.com/user-attachments/assets/483cca99-97cb-436a-9d39-41495339e775)

- `cd /mnt/common_volume/swarm/grafana/config` переход в директорию

![image](https://github.com/user-attachments/assets/880035b7-4dcc-4ae5-95bc-34a14ffc36e1)

- `sudo vi prometheus.yaml` переход в файл и замена exporter:9100

![image](https://github.com/user-attachments/assets/0d793aba-461e-4568-838d-0ac313b8e991)

![image](https://github.com/user-attachments/assets/f72b0996-ec38-463f-a15a-433877cca221)

- `sudo docker compose stop` остановка контейнеров без удаления

![image](https://github.com/user-attachments/assets/d92c8952-1f2d-46e0-a6fc-8f7579dcb4a5)

- `sudo docker compose down` остановка контейнеров и их удаление

![image](https://github.com/user-attachments/assets/b43a6ec1-585e-41f3-a9c5-96336f30b69e)

# Grafana

- запуск графаны с помощью `localhost:3000`

![image](https://github.com/user-attachments/assets/d9521743-4239-4b08-a93b-54ed58c85e4c)

- начальный экран графаны

![image](https://github.com/user-attachments/assets/63fa903b-6bf9-4ea5-9300-25085d2e2666)

- создание дашборда с визуализацией `Prometheus`

![image](https://github.com/user-attachments/assets/ba188928-35ca-40db-b464-48f971b37311)

![image](https://github.com/user-attachments/assets/f90e1ab2-4455-4b19-be3d-3df8e78d4884)

![image](https://github.com/user-attachments/assets/22e49310-2017-4712-b594-94cd6480d110)

- подключение `prometheus:9090`

![image](https://github.com/user-attachments/assets/86068921-52c3-4f4b-b5f6-9f494b5a8963)

![image](https://github.com/user-attachments/assets/c77cc21c-fdee-47c4-b66e-ca5c3f9919c5)

- импортирование дашборда 1860

![image](https://github.com/user-attachments/assets/aeb89232-250a-4142-aa76-ea347e282b2d)

![image](https://github.com/user-attachments/assets/0d428fdd-fe99-4944-a48e-edde412cfc3b)

- успешное завершение, работа мониторинга CPU

![image](https://github.com/user-attachments/assets/892bf58d-6f20-442a-92c4-09b475512a4a)
