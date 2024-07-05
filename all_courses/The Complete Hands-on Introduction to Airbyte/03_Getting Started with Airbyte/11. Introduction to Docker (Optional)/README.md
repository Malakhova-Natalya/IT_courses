## 11. Introduction to Docker (Optional)

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
