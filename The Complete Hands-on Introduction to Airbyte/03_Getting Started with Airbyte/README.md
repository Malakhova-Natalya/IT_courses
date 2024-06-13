## 🗂️ 3: Getting Started with Airbyte
✒️ разделы №№ 11 -20:

- **11. Introduction to Docker (Optional)**: [здесь](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/03_Getting%20Started%20with%20Airbyte/11.%20Introduction%20to%20Docker%20(Optional)/README.md)


- **12. Running Airbyte with Docker**: [здесь](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/03_Getting%20Started%20with%20Airbyte/12.%20Running%20Airbyte%20with%20Docker/README.md)


- **13. The Airbyte UI tour**: [здесь](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/03_Getting%20Started%20with%20Airbyte/13.%20The%20Airbyte%20UI%20tour/README.md)

- **14. The Bank Pipeline**

Далее будет разобран пример для данных банка. Например, у вас есть две страницы документа в Google Sheets с разными данными и вы хотите их загрузить в базу данных в соответствующие таблицы:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/44%20-%20from%20Google%20Sheets%20to%20DW.png)

- **15. Create your first source (Google Sheets)**

В этом [видео](https://www.udemy.com/course/the-complete-hands-on-introduction-to-airbyte/learn/lecture/40239172#content) подробно разобрано, как создать проект в Google Sheets и получить json-key. В результате получится создать source.
 
- **16. Create your first destination (BigQuery)**

 В этом [видео](https://www.udemy.com/course/the-complete-hands-on-introduction-to-airbyte/learn/lecture/40239174#content) рассказано о Billing Account, без которого не получится подключиться к Big Query, и о самом подключении к Big Query. В результате получится создать destination.

- **17. Configure your first connection**

К этому моменту уже созданы source и destination → создаём connection и прописываем его настройки.

Detect and propagate schema changes - эта настройка позволит своевременно узнать об изменениях в источнике (новая колонка, изменение типов данных и тд и тп). В этой настройке есть несколько вариантов.

Streams - можно не только включать одни и выключать другие, можно ещё нажать на какой-либо stream и увидеть, какие у него внутри колонки, и также что-то отключить с помощью бегунка слева.

Sync mode - две опции: 
  - Full refresh | Overwrite
  - Full refresh | Append

- **18. Make your first sync!**

- **19. Raw tables and additional columns?**

- **20. Connector classifications (Certified, Community, etc)**

Примечание: видео доступны с vpn + с доступом к курсу
