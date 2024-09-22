### Загрузка образов  
**docker pull imageName** - получить образ latest  

**docker pull imageName:Tag** - получить образ с конкретным тегом (версией)  

### Работа с образами  
**docker image ls** - посмотреть список образов  

**docker images** - тоже самое  

**docker images -q** - вывести список Image ID  

**docker history imageName:Tag** - посмотреть список слоёв  

**docker rmi imageName:Tag \[imageName:Tag\]** - удалить образ(образы) с конкретным тегом  

### Работа с контейнерами  
**docker run imageName** - поднять контейнер на основе образа  
(если образа нет, то демон скачает - latest, если тег не указан)  
Возможные опции после **run** :  
**--rm**   - удалить контейнер после завершения его работы  
**--name** - присвоить контейнеру имя (contName)  
**--it**  - направить поток ввода в контейнер  
**-d**     - запустить контейнер в фоновом режиме  
**-e env_var=12414** - добавить переменную env_var  
**--env_file .env** - добавить в образ переменные окружения из .env

**docker ps** - показать список активных контейнеров  
**-a**     - показать список всех контейнеров  

**docker stop contName \[contName\]**  - оставновить контейнер\\ы  

**docker start contName \[contName\]** - запустить контейнер\\ы  

**docker rm contName \[contName\]** - удалить контейнер\\ы  

**docker exec contName command**  - запустить команду в работающем контейнере  

**docker exec -it contName bash** - запустить bash и войнте в контейнер   

**docker build -t imageName /your_dir** - собрать образ с именем imageName на основе  
Dockerfile находящегося по адресу /your_dir  

**docker run --rm -d -v $(pwd)/dir_on_host:/dir_on_container contName** - прокидываем связь вольюма между
конкретной папкой. Изменению подлежат все файлы внутри папки






