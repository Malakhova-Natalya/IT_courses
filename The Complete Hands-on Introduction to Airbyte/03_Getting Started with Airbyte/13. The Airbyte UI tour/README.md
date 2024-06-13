## 13. The Airbyte UI tour

Пользовательский интерфейс имеет несколько больших разделов:
- Connections
- Sources
- Destinations

Они отображены в левой части интерфейса.
  
**Раздел Connections**

Стартовая страница выглядит, например, вот так:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/26%20-%20UI%20start%20page.png)

здесь мы видим слева направо:
- SOURCE NAME
- DESTINATION NAME
- FREQUENCY
- LAST SYNC
- ENABLED
  
Автор рекомендует давать отдельные названия для соединений, иначе, если у вас будут соединения с одинаковыми именами - вы легко в них запутаетесь.
Названия состоят из: название коннектора - название места назначения. Иногда это одно и тоже.

- кнопка (шестеренка) появляется при наведении на строку конкретного соединения. Там можно посмотреть детали. Если мы нажмём на неё, то увидим дополнительные разделы:

  - Status
  - Job History
  - Replication
  - Transformation
  - Settings

  В разделе Status - информация по всем стримам.
![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/27%20-%20details.png)

  В разделе Job History - информация по прошлым отработкам соединения

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/28%20-%20Job%20History.png)

  В разделе Replication - информация о том, как скопированы данные
  
![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/29%20-%20Replication.png)

  В разделе Transformation - информация о том, как трансформируются данные

  ![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/30%20-%20Transformation.png)

  В разделе Settings - здесь можно поменять название соединения или удалить его

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/31%20-%20Settings.png)

Новое соединение можно создать, нажав на кнопку "+ New connection" справа в верхнем углу:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/32%20-%20New%20connection.png)

**Раздел Sources**

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/33%20-%20Sources.png)

**Раздел Destinations**
