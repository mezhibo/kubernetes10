**Задание 1. Подготовить Helm-чарт для приложения**

1. Необходимо упаковать приложение в чарт для деплоя в разные окружения.

2. Каждый компонент приложения деплоится отдельным deployment’ом или statefulset’ом.

3. В переменных чарта измените образ приложения для изменения версии.



**Решение 1**

Проверим наличие установленного Helm

![Image alt](https://github.com/mezhibo/kubernetes10/blob/4f73f36999141cd2e22341397543bf5aefc72c59/IMG/1.jpg)


Скачиваем файлы для подготовки деплоя. Файлы, которые применялись в лекции.



![Image alt](https://github.com/mezhibo/kubernetes10/blob/4f73f36999141cd2e22341397543bf5aefc72c59/IMG/2.jpg)


Создаем шаблон на базе данных файлов


![Image alt](https://github.com/mezhibo/kubernetes10/blob/4f73f36999141cd2e22341397543bf5aefc72c59/IMG/3.jpg)



Получаем что helm при запуске создаст service(port 80) и deployment(nginx version 1.16.0)

В переменных чарта меняем образ приложения


![Image alt](https://github.com/mezhibo/kubernetes10/blob/4f73f36999141cd2e22341397543bf5aefc72c59/IMG/4.jpg)


Смотрим измененный шаблон


![Image alt](https://github.com/mezhibo/kubernetes10/blob/4f73f36999141cd2e22341397543bf5aefc72c59/IMG/5.jpg)


И видим что версия нашего приложения изменилась



