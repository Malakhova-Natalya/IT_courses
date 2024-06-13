## 🗂️ 3: Getting Started with Airbyte

- **11. Introduction to Docker (Optional)**: [здесь](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/03_Getting%20Started%20with%20Airbyte/11.%20Introduction%20to%20Docker%20(Optional)/README.md)


- **12. Running Airbyte with Docker**: [здесь] (https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/03_Getting%20Started%20with%20Airbyte/12.%20Running%20Airbyte%20with%20Docker/README.md)


- **13. The Airbyte UI tour**

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
  
![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/27%20-%20details.png)

- Status
- Job History
- Replication
- Transformation
- Settings
