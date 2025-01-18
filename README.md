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




**Задание 2. Запустить две версии в разных неймспейсах**

1. Подготовив чарт, необходимо его проверить. Запуститe несколько копий приложения.

2. Одну версию в namespace=app1, вторую версию в том же неймспейсе, третью версию в namespace=app2.

3. Продемонстрируйте результат.




**Решение 2**


Проверка


![Image alt](https://github.com/mezhibo/kubernetes10/blob/b11a524751fc3f8ca045e25569e11f0cee48b61a/IMG/6.jpg)


![Image alt](https://github.com/mezhibo/kubernetes10/blob/b11a524751fc3f8ca045e25569e11f0cee48b61a/IMG/7.jpg)


![Image alt](https://github.com/mezhibo/kubernetes10/blob/b11a524751fc3f8ca045e25569e11f0cee48b61a/IMG/8.jpg)


![Image alt](https://github.com/mezhibo/kubernetes10/blob/0ebbb2c6f1801e9684d26cf54da03ce20596853e/IMG/9.jpg)


Запустим несколько версий приложения

![Image alt](https://github.com/mezhibo/kubernetes10/blob/0ebbb2c6f1801e9684d26cf54da03ce20596853e/IMG/10.jpg)


Удалим наш helm demo чтобы потом создать новый в namespace из условия задачи


![Image alt](https://github.com/mezhibo/kubernetes10/blob/0ebbb2c6f1801e9684d26cf54da03ce20596853e/IMG/11.jpg)


Создаем helm по заданию в п.2


![Image alt](https://github.com/mezhibo/kubernetes10/blob/0ebbb2c6f1801e9684d26cf54da03ce20596853e/IMG/12.jpg)




