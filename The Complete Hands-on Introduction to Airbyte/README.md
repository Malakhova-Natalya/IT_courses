# The Complete Hands-on Introduction to Airbyte 🗃️
Get started with Airbyte and learn how to use it with Apache Airflow, Snowflake, dbt and more

Авторы: [Marc Lamberti](https://www.udemy.com/course/the-complete-hands-on-introduction-to-airbyte/?couponCode=ST19MT60324#instructor-1)

## 🗂️ 1: Welcome!
✒️ разделы:

- **1. Welcome!**

Курс посвящён основам Airbyte. Здесь - всё, что нужно для быстрого старта в этом инструменте. Здесь только основы и конкретные примеры.

- **2. Prerequisites**
  
Для прохождения курса понадобится Docker, аккаунт на AWS, знание Python будет плюсом.

- **3. Who am I?**
  
Автор - дата-инженер из Франции. Автор курсов по Airflow. 

- **4. Learning Advice**

Автор рекомендует обязательно практиковаться + не спешить, можно ставить закладки на видео Udemy и возвращаться к некоторым местам, чтобы обязательно попробовать их на практике. не расстраиваться, если возникают трудности. Лучший способ научиться - это самостоятельно преодолеть эти вопросы (возможно обратившись к StackOverFlow, Airbyte community, ChatGPT, etc.). В крайнем случае автор предлагает обращаться к нему в разделе Q&A - писать обращение со скриншотами и ссылками.

## 🗂️ 2: Airbyte Fundamentals
✒️ разделы:
- **5. Why Airbyte?**

Для начала надо всегда спрашивать себя - а зачем мне вообще тот или иной инструмент? Вот и мы рассмотрим этот вопрос: а зачем нам вообще Airbyte?

Предположим, у нас есть источник данных и база данных. Мы можем сделать интеграцию/написать python-скрипт и всё будет работать. Но, если у вас:
  - много источников и мест назначений
  - вы работаете не один, а есть и другие команды,

то избежать хаоса при множестве подключений поможет Airbyte.

Также, если что-то сломалось, вы можете видеть единую картину подключения всех данных в Airflow. Если что-то изменится/поломается (например, изменится схема) - вы увидите уведомления и сможете настроить то, что вам нужно в одном интерфейсе, а не заниматься исправлениями в куче разных скриптов.
- **6. What is Airbyte?**

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

- **7. The Core Concepts**

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

- **8. The Core Components**

Главные компоненты Airbyte:
- Airbyte DataBase (or Config DataBase) - по умолчанию это база данных Postgres, в ней хранится вся информация по подключениям (метадата коннекшенов: учётные данные (credentials), настройки (settings) и тд)
- Airbyte WebApp - пользовательский интерфейс (подключается на 8000 порту)
- Airbyte Server (API) - API технически исполняет то, что "заказывает" пользователь в интерфейсе
- Temporal (Scheduler) 


## 🗂️ 3: Getting Started with Airbyte

## 🗂️ 4: Advanced Concepts

## 🗂️ 5: The Fraud Project

