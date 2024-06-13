## 13. The Airbyte UI tour

Пользовательский интерфейс имеет несколько больших разделов:
- Connections
- Sources
- Destinations

Они отображены в левой части интерфейса.
  
### Раздел Connections

Здесь - всё о соединениях.

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

### Раздел Sources

Здесь представлены имеющиеся источники. А если их ещё нет - то все возможные виды источников.

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/33%20-%20Sources.png)

В возможных видах источников можно увидеть, что коннекторы бывают двух видов: 
  - community - созданные сообществом
    
  ↓
  
  - certified - сертифицированные

Рассмотрим пример: вы хотите подключить Google Sheets. Вы можете ввести в поиск название, и увидите, что есть предлагаемый коннектор и есть возможность создать свой коннектор.

Чтобы создать новый коннектор, есть 2 способа:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/35%20-%20two%20ways%20of%20creating%20new%20connector.png)
- справа - low-code connector-builder
- внизу - request a new connector

  Если воспользоваться предлагаемым коннектором, и нажать на него, то мы попадём на страницу, где можно заполнять свои данные (слева) и параллельно видеть документацию (справа)

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/36%20-%20example%20of%20Google%20Sheets.png)

### Раздел Destinations

Здесь -  имеющиеся места назначения

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/34%20-%20Destinations.png)


