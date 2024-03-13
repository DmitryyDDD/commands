# **Выполненные шаги**
1. Создание локального репозитория
```
git init
```
2. Создание пустого текстового документа в папке
```
> textdoc.txt
```
3. Добавление абзаца в документ и фиксация изменений
```
echo Абзац >> textdoc.txt
git add textdoc.txt
git commit -m "Абзац"
```
4. Проверка статуса репозитория
```
git status
```
5. Добавление другого файла в репозиторий
```
> newdoc.txt
```
6. Создание коммита
```
git commit -m "Другой файл"
```
7. Просмотр протокола коммитов
```
git log
```
8. Просмотр изменений относительно последнего коммита из файла
```
git diff
```
9. Удаление изменений относительно последнего коммита из файла
```
git checkout -- textdoc.txt
```
10. Просмотр существующих веток
```
git branch
```
11. Создание новой ветки
```
git branch newbranch
```
12. Переключение на новую ветку
```
git checkout newbranch
```
13. Создание ветки и переключение на неё
```
git checkout -b +branch
```
14. Удаление ветки
```
git checkout newbranch
git branch -d +branch
```
15. Добавление изменений из указанной ветки в текущую
```
git merge master
```
16. Создание конфликта
    * переключение на ветку master
        ```
        git checkout master
        ```
    * внесение изменений в файл textdoc.txt, добавление и создание коммита
        ```
        git add textdoc.txt
        git commit -m "Удаление всех абзацев кроме первого"
        ```
    * переключение на ветку newbranch и повторение действий выполненных для ветки master
        ```
        git add textdoc.txt
        git commit -m "Удаление всех абзацев кроме первого"
        ```
    * переход на ветку master  попытка слияния веток
        ```
        git checkout master	
        git merge newbranch
        ```
17. Просмотр файлов с конфликтами
    ```
    git status
    ```
18. Устранение конфликта: удаление разметки из файла, добавление и создание коммита
    ```
    git add textdoc.txt
		git commit -m "Конфликт слияния устранён"
    ```
19. Переключение на указанный коммит
    ```
    git checkout 3390448
    ```
20. Ребазирование
    ```
    git rebase master
    ```
21. Удаление ветки
    ```
    git branch -d newbranch
    ```
22. Пропуск текущего конфликтного коммита и переход к следующему
    ```
    git rebase --skip
    ```
23. Отправление изменений для локального репозитория для указанной ветки в удалённый
    ```
    git remote add origin https://github.com/DmitryyDDD/commands.git
	  git push origin master
    ```
24. Забор изменения из репозитория, для которого были созданы удалённые ветки по умолчанию
    ```
    git pull origin master
    ```
25. Забор изменения удалённой веткииз репозитория основной ветки по умолчанию
    ```
    git checkout -b feature-branch
	  git push origin feature-branch
	  git pull origin feature-branch:master
    ```
26. 
    ```
    git clone https://github.com/DmitryyDDD/commands.git
    ```
   
