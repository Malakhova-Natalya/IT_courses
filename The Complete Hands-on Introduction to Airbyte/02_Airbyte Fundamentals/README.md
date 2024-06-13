## 🗂️ 2: Airbyte Fundamentals
✒️ разделы 5 -10:
### 5. Why Airbyte?

Для начала надо всегда спрашивать себя - а зачем мне вообще тот или иной инструмент? Вот и мы рассмотрим этот вопрос: а зачем нам вообще Airbyte?

Предположим, у нас есть источник данных и база данных. Мы можем сделать интеграцию/написать python-скрипт и всё будет работать. Но, если у вас:
  - много источников и мест назначений
  - вы работаете не один, а есть и другие команды,

то избежать хаоса при множестве подключений поможет Airbyte.

Также, если что-то сломалось, вы можете видеть единую картину подключения всех данных в Airflow. Если что-то изменится/поломается (например, изменится схема) - вы увидите уведомления и сможете настроить то, что вам нужно в одном интерфейсе, а не заниматься исправлениями в куче разных скриптов.
### 6. What is Airbyte?

Open-source data-integration tool that moves data from one system to another

Benefits:
  - Open-Source (на практике это значит, что вы можете залезть в код любого коннектора и изменить его под себя + это достаточно большое community)
  - User Interface & User Experience (документация и подсказки в самом Airbyte)
  - Scalable (масштабируемый - вы можете добавлять много источников и много соединений)
  - Extensible (расширяемый - вы можете создавать свои собственные коннекторы)

Where does it fit in your pipelines?

Где место Airbyte, например, в такой схеме?
![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/01%20-%20Airbyte%20in%20ELT%20ETL%20processes.png)

Airbyte используется для задач загрузки данных (Extract&Load)
![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/02%20-%20Airbyte%20in%20ELT%20ETL%20processes.png)

и для выгрузки (Publish)
![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/03%20-%20Airbyte%20in%20ELT%20ETL%20processes.png)

вот пример более цельной картины использования из статьи
![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/04%20-%20Airbyte%20in%20ELT%20ETL%20processes.png)

### 7. The Core Concepts

Основные понятия в Airbyte:
- source - источник данных
- destination - место назначения

  ![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/05%20-%20source%20and%20destination.png)

  
- connector - коннектор это, можно так сказать, проводник - это технический компонент, который собственно скачивает или загружает данные

  ![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/06%20-%20connector.png)

  
- stream - стрим можно обозначить как поток данных - группа связанных данных, например, отдельный лист в google sheets

  ![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/07%20-%20stream.png)

  
- field - поле - это, например, отдельная это колонка в данных

  ![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/08%20-%20field.png)

  
- connection - соединение - его можно рассматривать как автоматизированный пайплайн, который копирует данные из источника в место назначения. К нему пользователь может задавать настройки, например, частоту соединения, способ добавления данных (добавление новых записеей к имеющимся или полная перезапись), также есть другие настройки.

  ![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/09%20-%20connection.png)

### 8. The Core Components

Главные компоненты Airbyte:
- Airbyte DataBase (or Config DataBase) - по умолчанию это база данных Postgres, в ней хранится вся информация по подключениям (метадата коннекшенов: учётные данные (credentials), настройки (settings) и тд)

  ![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/10%20-%20Airbyte%20DB.png)

  
- Airbyte WebApp - пользовательский интерфейс (подключается на 8000 порту)

  ![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/11%20-%20Airbyte%20WebApp.png)

  
- Airbyte Server (API) - API технически исполняет то, что "заказывает" пользователь в интерфейсе

  ![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/12%20-%20Airbyte%20Server%20(API).png)

  
- Temporal (Scheduler) - open source orchestrator - его функция запускать по времени процессы, запрашиваемые API: синхронизация, проверки и тд. Он ставит запросы в очередь.

  ![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/13%20-%20Temporal%20(Scheduler).png)

  
- Airbyte Worker - берёт запросы из очереди и исполняет их.

  ![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/14%20-%20Airbyte%20Worker.png)

Полная схема на примере выглядит так:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/15%20-%20core%20components%20full%20schema.png)

Пользователь в интерфейсе (UI) создаёт connection, например, к БД MySQL → информацию получает Server API, а данные подключения сохраняются в Airbyte DB.

Server API обрабатывает информацию → далее действие переходит к Scheduler (делает проверку, ставит в очередь) → далее  Worker берёт запрос из очеред и исполняет его. После исполнения запроса снова мяч на стороне Sheduler (он будет проверять, не настало ли время следующего действия).

### 9. Why not Airbyte?

Для чего Airbyte не подходит?
- Streaming

Airbyte обрабатывает данные порциями, поэтому у вас всегда будет некоторая задержка. Плюс иногда Airbyte долго обрабатывает данные (это зависит от коннектора, от количества ресурсов).

Также некоторым ограничением может быть то, что в Airbyte нет нужного вам коннектора.
Однако это не является в чистом виде ограничением, поскольку вы можете сами написать его. Есть два способа создать свой коннектор:
1. при помощи Airbyte CDK - это фреймворк, который даёт всё для написания своего собственного коннектора
2. при помощи connector builder - это low-code-way для создания собственных коннекторов

### 10. Airbyte Cloud or OSS?
  
Есть 3 разных способа использования Airbyte. Данный курс рассматривает Self-Managed Community version. Для компаний можно рассмотреть Self-Managed Enterprise или Airbyte Cloud.
