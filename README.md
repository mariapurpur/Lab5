# Лабораторная работа 5

В данной лбаораторной работе будут рассмотрены работа с Git Bash и Git Flow, а так же выполненны задания по ним.

## Задание 1:

Создайте bash-скрипт, который будет выполнять проверку того, что коммитится файл формата .txt и в файле присутствует какой-то текст. Далее поместите этот скрипт в нужную папку и проверьте, что перед каждым коммитом проходит проверка, например, добавьте вывод о результате проверки в консоль.

## Решение:

1. Создадим файл через консоль под названием script.bash командой `touch script.bash`. Учитываем, что наши файлы выглядят слеюущим образом:

**example.txt**

![image](https://github.com/user-attachments/assets/33d70f8b-2afd-4819-9157-b423ea40429e)

**2example.txt**

![image](https://github.com/user-attachments/assets/558d61ee-5753-4b13-a638-613df7a107ad)

2. Данный файл будет отвечать за проверку добавленных в коммит файлов во время коммита. Кроме того, предусмотрим сценарий, при котором пользователь не добавляет новых изменённых файлов. В него напишем следующий код, проверяющий формат и наличие автора:

![image](https://github.com/user-attachments/assets/048f06cc-ae86-40f8-b99f-a3feeedbb868)

3. Закроем script.bash, сохранив его. Сделаем этот код запускаемым командой `chmod +x script.bash`. Перейдём в папку .git/hooks. Там изменим файл pre-commit.sample:

![image](https://github.com/user-attachments/assets/3e22c011-7100-4b4f-aa01-250e92d18ba0)

4. Уберём из названия файла .sample, чтобы он мог быть запущен консолью.

5. Сделаем файл запускаемым командой `chmod +x pre-commit`.

6. Проверим, что всё работает:

![image](https://github.com/user-attachments/assets/672d4fbd-7295-47f2-b314-db7fc8296900)

## Задание 2:

Предположим, у вас есть задача на создание новой функциональности для вашего проекта с использованием Git Flow. Давайте рассмотрим конкретный пример.

## Решение:

1. Убедимся, что Git Flow установлен в системе.

![image](https://github.com/user-attachments/assets/cde0c91b-e061-4436-8dcf-7f80393afd32)

2. Инициализируем командой `git flow init` и создадим ветку для новой функциональности:

![image](https://github.com/user-attachments/assets/1c26b009-6f47-4d6c-9827-4d45121bd5f7)

3. 
