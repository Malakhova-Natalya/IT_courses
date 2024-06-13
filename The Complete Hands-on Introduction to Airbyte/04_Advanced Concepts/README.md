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

### 23. Discover the sync modes
### 24. Handling schema changes
### 25. What is Change Data Capture (CDC)?
### 26. Enable CDC with Postgres
### 27. Syncing data between Postgres and BigQuery using CDC
### 28. The Sync Modes cheat sheet
### 29. CDC under the hood
