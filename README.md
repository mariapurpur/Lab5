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

![image](https://github.com/user-attachments/assets/a38325dd-0a24-49b6-be5d-7d2ec16044e2)

3. Начнём работу над feature. Создадим файл task_manager.py, введём код из примера в него и заккомитим изменения. Далее пропишем команду `git flow feature finish task-management`.

![image](https://github.com/user-attachments/assets/a7a534b2-8803-4a92-806a-599843f5e1f0)

4. Переключимся на ветку develop. Создадим релиз и закоммитим его.

![image](https://github.com/user-attachments/assets/f037e912-bf66-4aa0-9d0f-45d09193de2a)

![image](https://github.com/user-attachments/assets/adfc124a-090f-441e-a5eb-bcd9e1dae5fa)

5. Пропишем `git flow release finish v1.0.0`, чтобы закончить работу над релизом, а затем создадим hotfix.

![image](https://github.com/user-attachments/assets/c18e1786-3eeb-4aa6-b1d2-ae5b623d49bb)

6. После успешной работы над hotfix пропишем `git flow hofix finish hotfix-1.0.1`.

![image](https://github.com/user-attachments/assets/424fee29-f5a0-4ee5-aee9-a4bb9d4d925e)

7. Завершим работу и загрузим изменения при помощи `git push origin develop`. Не забудем про `git push origin main`.

![image](https://github.com/user-attachments/assets/0329e810-b810-43c6-931a-2f5c7bb3d8aa)

![image](https://github.com/user-attachments/assets/52e762c7-566e-40b1-a8e8-163a341c0989)
