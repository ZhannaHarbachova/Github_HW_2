# GitHub. HW_2


**1. На локальном репозитории сделать ветки для:**
- Postman
- Jmeter
- CheckLists
- Bag Reports
- SQL
- Charles
- Mobile testing

```
for b_name in {'Postman','Jmeter','CheckLists','Bug_Reports','SQL','Charles','Mobile_testing'};
do git branch $b_name
done
```

**2. Запушить все ветки на внешний репозиторий**

```
for b_name in {'Postman','Jmeter','CheckLists','Bug_Reports','SQL','Charles','Mobile_testing'};
do git push -u origin $b_name
done
```

**3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта**

```
git checkout Bug_Reports
touch bugrep.txt
vim bugrep.txt
i     # для перехода в режим редактирования
esc   # для выхода из режима редактирования после заполнения файла
:wq   # сохранение и выход из редактора
```
**4. Запушить структуру багрепорта на внешний репозиторий**
```
git add bugrep.txt
git commit -m "Add bugrep.txt"
git push
```
**5. Вмержить ветку Bag Reports в Main**
```
git checkout main
git merge Bug_Reports
```
**6. Запушить main на внешний репозиторий.**
```
git push
```
**7. В ветке CheckLists набросать структуру чек листа.**
```
git checkout CheckLists
touch checklist.txt
vim checklist.txt
i     # для перехода в режим редактирования
esc   # для выхода из режима редактирования после заполнения файла
:wq   # сохранение и выход из редактора
```
**8. Запушить структуру на внешний репозиторий**
```
git add .
git commit -m "Add checklist.txt"
git push
```
**9. На внешнем репозитории сделать Pull Request ветки CheckLists в main**

* Нажать на кнопку "Compare & pull request"
* При необходимости заполнить поле комментария
* Нажать на кнопку "Create pull request"
* Нажать на кнопку "Merge pull request" -> "Confirm merge"

**10. Синхронизировать Внешнюю и Локальную ветки Main**
```
git checkout main
git pull
```
