## 30 комманд

1. Создал учетную запись

   ![](/images/git_config.png)
   
3. Создал локальный репозиторий:
    ```
    git init
    ```

    ![](/images/git_init.png)
   
5. Создал пустой текстовый документ в папке:
   
   ![](/images/empty_txt.png)
6. Добавил первый абзац в текстовый документ:

   ![](/images/par_1.png)

  Закоммитил:
  ![](/images/git_commit1.png)
  
  и так повторил 3 раза:
  
  ![](/images/par_2.png)
    
  ![](/images/txt3.png)
    
  ![](/images/par_3.png)
    
5. Просмотрел статус текущего репозитория:
    ```
    git status
    ```
    ![](/images/git_status.png)
6. Добавил еще один файл:

    ![](/images/empty_txt2.png)
8. Создал коммит:
    ```
    git commit -m "выполненные долги"
    ```
    ![](/images/git_commit2.png)
9. Посмотрел протокол коммитов:
    ```
    git log
    ```
    ![](/images/git_log.png)
10. Посмотрел изменения в файле по сравнению с последним коммитом:
    ```
    git diff HEAD~1 Выполнено.txt
    ```
     ![](/images/git_diff.png)
11. Убрал изменения относительно последнего коммита из файла:
    ```
    git checkout -- Выполнено.txt
    ```
    
    ![](/images/git_checkout1.png)
12. Посмотрел существующие ветки:
    ```
    git branch
    ```
    ![](/images/git_branch.png)
13. Создал новую ветку:
    ```
    git branch tasks
    ```

    ![](/images/git_branch1.png)
14. Переключился на новую ветку:
    ```
    git checkout tasks
    ```
    ![](/images/git_checkout.png)
15. Создал новую ветку и сразу же переключилися на нее:
    ```
    git checkout -b test
    ```
    ![](/images/git_checkout3.png)
16. Удалил ветку:
    ```
    git branch -d test
    ```
    ![](/images/branch_del.png)
17. Добавил merge изменения из указанной ветки в текущую:
    ```
    git checkout master
    git merge tasks
    ```
    ![](/images/git_merge.png)
19. Создал конфликт:
    Переключился на ветку master
    ```
    git checkout master
    ```
    Изменил файл Долги.txt, добавив текст

    ![](/images/conf1.png)
    
    Добавил и закоммитил в консоле
      
      ```
      git add Долги.txt
      git commit -m "гитхаб 30 команд"
      ```
      ![](/images/conf2.png)

    Переключился на ветку tasks
    ```
    git checkout tasks
    ```
    Изменил файл Долги.txt, добавив текст

    ![](/images/conf3.png)

    Добавил и закоммитил
    
      ```
      git add Долги.txt
      git commit -m "экзамен билеты"
      ```
      ![](/images/git_commit3.png)
    Переключился на ветку master и попытался выполнить merge:
      
      ```
      git checkout master
      git merge tasks
      ```
      ![](/images/conf4.png)
21. Посмотрел в каких файлах есть конфликты:
    ```
    git status
    ```
    ![](/images/git_status2.png)
22. Устранил конфликт:

    Конфликтный файл:
    ![](/images/solve_conf1.png)
    
    Выбрал текст, который хочу оставить в документе Долги.txt, удалил разметку Git

    ![](/images/solve_conf2.png)

    Добавил и закоммитил
      
      ```
      git add Долги.txt
      git commit -m "все долги"
      ```
      ![](/images/solve_conf3.png)
19. Переключился на указанный коммит:
    ```
    git checkout dc8216e
    ```
    ![](/images/git_checkout4.png)
18. Сделал rebase текущей ветки:
    ```
    git rebase master
    ```
18. Удалил ветку:
    ```
    git branch -d test2
    ```
19. Пропустил текущий конфликтный коммит и перешел к следующему:
    ```
    git rebase --skip
    ```
    ![](/images/rebase_skip.png)
20. Отправил изменения из локального репозитория для указанной ветки в удаленный (дистанционный):
    ```
    git remote add origin https://github.com/Lovell96/git30.git
    git push origin master
    ```
21. Забрал изменения из репозитория, для которого были созданы удаленные ветки по умолчанию:
    ```
    git pull origin master
    ```
22. Забрал изменения удаленной ветки из репозитория основной ветки по умолчанию:
    
23. Клонировал репозиторий:
    ```
    git clone https://github.com/Lovell96/git30.git
    ```
