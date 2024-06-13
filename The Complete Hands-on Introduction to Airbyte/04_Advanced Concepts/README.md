## 🗂️ 4: Advanced Concepts
✒️ разделы №№ 21-29:

### 21. How does a sync work?

Схема работы представлена на картинке

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/47%20-%20how%20does%20a%20sync%20work.png)

Когда дело доходит до Worker, он выполняет 4 стадии:
1. check - проверка
2. platform - подготавливает платформу
3. source - исполняет инструкции из docker image source 
4. destination - исполняет инструкции из docker image destination
   
### 22. Side notes for Postgres

Если вы работаете с базой данных Postgres, надо создать read-only Postgres user. Пока мы используем Airbyte Postgres database, этот пользователь автоматически уже существует.

### 23. Discover the sync modes

Существует 2 части имени sync mode, они разделены прямой чертой |
- левая часть указывает, как мы читаем данные из источника
- правая - как записываем в место назначения

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/48%20-%20two%20part%20of%20name.png)

Существуют разные варианты sync mode:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/49%20-%20sync%20mode.png)

Для инкрементального чтения понадобится указать дополнительные опции:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/50%20-%20incremental%20reading%20mode.png)

Интересный метод - инкрементальный, но без дублей:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/51%20-%20incremental%20dedupted.png)

### 24. Handling schema changes

Новая колонка, изменение типа данных, переименование колонки или удаление её - всё это schema changes. Поведение Airbyte можно настроить при помощи параметра Detect and propagate schema changes.

Изменения могут нарушить работу пайплайна или не повлиять на него.

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/52%20-%20schema%20changes.png)

По умолчанию Detect changes and manually approve - это значит Airbyte уведомит об изменениях, но не изменит настройки пайплайна (нужно будет вручную подтвердить внесение изменений).

Когда появились изменения висточнике → соединение отработает, но в раделе Replications будет уведомление Non-breaking schema updates detected → можно перейти в Review changes → Airbyte укажет, где именно и какие изменения → вы можете нажать Ок и сохранить эти изменения (Save changes).

Есть и другие варианты поведения:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/53%20-%20schema%20changes%20options.png)

Автор рекомендует не использовать первые два варианта, а предпочитать третий (или четвертый).

Airbyte сам проверяет изменения в источнике:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/54%20-%20Airbyte%20checks%20schema%20changes.png)

Но если у вас есть сомнения и вы хотие дополнительно проверить, можете использовать кнопочку "Refresh source schema".

Что касается изменений, которые нарушат работу пайплайна, то это удаление primary key или cursor:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/55%20-%20breaking%20changes.png)

### 25. What is Change Data Capture (CDC)?

Это способность отслеживать изменения в базе данных

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/56%20-%20change%20data%20capture.png)

Это реализовано с помощью системы логов:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/57%20-%20transaction%20logs.png)

### 26. Enable CDC with Postgres

Начать созавать новый источник POstgres → сбоку в документации будет Advanced Configuration - Setup using CDC

Подробнее можно посмотреть в этом [видео](https://www.udemy.com/course/the-complete-hands-on-introduction-to-airbyte/learn/lecture/40236680#content)

### 27. Syncing data between Postgres and BigQuery using CDC
### 28. The Sync Modes cheat sheet
### 29. CDC under the hood
