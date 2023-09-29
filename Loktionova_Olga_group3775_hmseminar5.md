# Урок 5. Docker Compose и Docker Swarm
### 1) создать сервис, состоящий из 2 различных контейнеров: 1 - веб, 2 - БД (compose)

Проверяем естьт ли запущенные контейнеры и образы.  
Создаем новую директорию и заходим в нее.  
![](https://github.com/Lokotokk/Contarization-seminar5/blob/main/images/1.png)  

Создаем yml-файл.  
В первой строке описываем версию файла.  
Далее описываем сервисы, которые необходимо запустить:  
1. База данных MYSQ: задаем название сервиса (db), используем готовый образы с docker hub(image:  ), в блоке environment прописываем переменные, которые могут быть использованы для работы контейнера (переменная MY_ROOT_PASSWORD и ее значение).    
2. phpmyadmin: задаем название сервиса (admin), используем готовый образы с docker hub(image:  ), в блоке ports указываем на то, какие порты необходимо открыть для связи с контейнером.  
![](https://github.com/Lokotokk/Contarization-seminar5/blob/main/images/2.png)

Запускаем проект. В данном случае проект запустится в фоновом режиме, так как в команде присутствует флаг -d.  
![](https://github.com/Lokotokk/Contarization-seminar5/blob/main/images/3.png)  

Проверяем, что всё работает:  
![](https://github.com/Lokotokk/Contarization-seminar5/blob/main/images/4.png)  


