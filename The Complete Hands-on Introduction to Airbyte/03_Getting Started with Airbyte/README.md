## 🗂️ 3: Getting Started with Airbyte

- **11. Introduction to Docker (Optional)**

Разбираемся на примере, для чего и как используется Docker.

Предположим, у вас есть два разных приложения. Одно использует python 3.6, другое - python 3.8. Вы можете установить их в разные контейнеры, чтобы не возникло конфликта версий.

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/16%20-%20Docker%20containers.png)

Таким образом могут работать параллельно несколько версий python 

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/17%20-%20different%20python%20versions.png)

Как это реализуется? Пишем Dockerfile:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/18%20-%20Dockerfile.png)

Из Dockerfile → при помощи команды docker build → создаём Docker Image → из него при помощи команды docker run → запускаем Docker Container

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/19%20-%20Docker%20full%20schema.png)

Вкратце это все основные сведения, которые нужны для понимания материалов этого курса.

- **12. Running Airbyte with Docker**

Когда вы скачаете [папку](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/airbyte.zip) со всем необходимым для установки Airbyte в Docker, вы обнаружите там следующие файлы:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/20%20-%20Docker%20download%20files.png)

Далее надо запустить команду:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/21%20-%20Docker%20command.png)

Когда загрузка завершится, вы увидите все основные компоненты Airbyte:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/22%20-%20core%20components%20in%20Docker.png)

Перечислим ещё раз эти компоненты и их предназначение:
- temporal - Airbyte Scheduler
- server - config API
- cron - for differnet cron jobs
- webapp - Airbyte user interface
- proxy - for authentification part
- api-server - the public API of Airbyte
- worker - runs jobs from Airbyte scheduler
- connector-builder-server - this is useful to test your own connector that you build with the connector builder
- db - Airbyte database powered by Postgres

Далее нам надо перейти в пользовательский интерфейс программы. Для этого находим webapp и справа кликаем на место, где указаны порты (8000)

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/23%20-%208000%20port%20-%20click%20here.png)

Появится окно, где надо ввести логин и пароль:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/24%20-%20UI%20sign%20in.png)

Далее появится ещё одно окно, которое надо заполнить:

![cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/25%20-%20specify%20your%20preferences.png)

и после этого вы попадёте в пользовательский интерфейс Airbyte.

- **13. The Airbyte UI tour**

Стартовая страница выглядит, например, вот так:

!{cover](https://github.com/Malakhova-Natalya/IT_courses/blob/main/The%20Complete%20Hands-on%20Introduction%20to%20Airbyte/26%20-%20UI%20start%20page.png)

здесь мы видим слева направо:
- SOURCE NAME
- DESTINATION NAME
- FREQUENCY
- LAST SYNC
- ENABLED
- кнопка (шестеренка)
- 
Автор рекомендует давать отдельные названия для соединений, иначе, если у ва будут соединения с одинаковыми именами - вы легко в них запутаетесь.
Названия состоят из: название коннектора - название места назначения. Иногда это одно и тоже.


