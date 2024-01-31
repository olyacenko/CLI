## CLI (terminal) commands ##
# Task 1 
1. Посмотреть где я - `pwd`

---

2. Создать папку - `mkdir terminal_trainig`

---

3. Зайти в папку - `cd terminal_trainig`

---

4. Создать 3 папки - `mkdir {fold_1,fold_2,fold_3}`

---

5. Зайти в любую папку - `cd fold_1` 

---

6. Создать 5 файлов (3 txt, 2 json) - `touch file_1.txt file_2.txt file_3.txt file_4.json file_5.json`

---

7. Создать 3 папки - `mkdir {dir_1,dir_2,dir_3}`

---

8. Вывести список содержимого папки:
    - `ls` - содержимое директории  
    - `ls -l` - содержимое директории + разрешения, владелец, размер и дата изменения 
    - `ls -la` содержимое директории, включая скрытые папки + разрешения, владелец, размер и дата изменения

---

9. Открыть любой txt файл - `vim file_1.txt` 

---

10. Hаписать туда что-нибудь, любой текст:
    - `i` - начать редактирование 
    - клавишa `esc` - выйти из режима редактирования   

---

11. Cохранить и выйти:
    - клавиши `shift+:` - назначить команду
    - `wq` - записать и закрыть редактор 

---

12. Выйти из папки на уровень выше - `cd ..`

---

13. Переместить любые 2 файла, которые вы создали, в любую другую папку - 

`mv file_4.json file_5.json /Users/ostalskyi/terminal_trainig/fold_2`

---

14. Скопировать любые 2 файла, которые вы создали, в любую другую папку -  

`cp file_1.txt file_2.txt /Users/ostalskyi/terminal_trainig/fold_3`

---

15. Найти файл по имени - `find . -iname "file_4*"` (без учета регистра)

---

16. Просмотреть содержимое в реальном времени (команда grep) -
 
 `grep -in "error" ./file_1.txt | tail -f`
 
 (Эта команда позволит просматривать содержимое файла по мере его обновления, отображая только номер строки без учета регистра содержащую слово "error". Остановить команду - клавиши `Ctrl+C`.) 

---

17. Вывести несколько первых строк из текстового файла - `head -n5 file_1.txt` (выведет первые 5 строк) 

---

18. Вывести несколько последних строк из текстового файла - `tail -n5 file_1.txt` (выведет последние 5 строк)

---

19. Просмотреть содержимое длинного файла (команда less):
   
    - `less file_1.txt` откроет файл 
    - `/нужное слово` выделит слово которое ввели 
    - `q` закроет файл 

---

20. Вывести дату и время - `date` 

---

## Задание № 1 ##
1. Отправить http запрос на сервер. http://162.55.220.72:5005/terminal-hw-request  
### Ответ ###

`curl  http://162.55.220.72:5005/terminal-hw-request`

---
## Задание № 2 ##
2. Написать скрипт который выполнит автоматически пункты:
   - 3.Зайти в папку
   - 4.Создать 3 папки
   - 5.Зайти в любую папку 
   - 6.Создать 5 файлов (3 txt, 2 json)
   - 7.Создать 3 папки
   - 8.Вывести список содержимого папки
   - 13.Переместить любые 2 файла, которые вы создали, в любую другую папку
### Ответ ###

Создать пустой файл - `touch first_script`

Открыть текстовый редактор - `vim first_script`

Начать редактирование `i` и ввести текст:   

``` 
#!/bin/sh

cd /Users/ostalskyi/terminal_trainig
mkdir {dir_1,dir_2,dir_3}
cd dir_1
touch file_1.txt file_2.txt file_3.txt file_4.json file_5.json
mkdir {dir_1_1,dir_2_2,dir_3_3}
ls -la
mv file_1.txt file_2.txt /Users/ostalskyi/terminal_trainig/dir_2
 ```

Выйти из режима редактировани `esc`

Назначить команду `shift+:`

Записать и закрыть редактор `wq` 

Сделать файл исполняемым `chmod u+x first_script`

Запустить скрипт `./first_script`


# Task 2


1. Сделать папку dir_1 - `mkdir dir_1`

---

2. Зайти в папку dir_1 - `cd dir_1`

----

3. Создать папку inner_dir_1 - `mkdir inner_dir_1`

---

4. Посмотреть где ты находишься- `pwd`

----

5. Находясь в папке dir_1 создать пустой текстовый файл tf_1.txt - `touch tf_1.txt`

----

6. Находясь в папке dir_1 через команду cat создать текстовый файл tf_2.txt со следующими строками:
   - the first 1
   - the second 2
   - the third 3
   
 ```
 cat > tf_2.txt
 
the first 1
the second 2
the third 3
```
выйти из режима редактирования `control+c`.

----

7. Зайти в папку inner_dir_1 - `cd inner_dir_1`

----

8. Через cat сделать текстовый файл tf_3.txt  c любыми строками - 

```
cat > tf_3.txt

string 1 
string 2 
string 3
string 4
string 5
```
выйти из режима редактирования `control+c`

----

9. Через cat добавить в текстовый файл tf_3.txt строку “the second 2” 
10. Через cat добавить в текстовый файл tf_3.txt строку “the sec 2”
11. Через cat добавить в текстовый файл tf_3.txt строку “the SeCoNd 2”
```
cat >> tf_3.txt

the second 2
the sec 2
the SeCoNd 2

```
выйти из режима редактирования `control+c`

----

12. Через cat добавить в текстовый файл tf_2.txt строку “the sec 3”
13. Через cat добавить в текстовый файл tf_2.txt строку “the seConD 2”
```
cat >> /Users/ostalskyi/hw_ksendzov_courses/dir_1/tf_2.txt

the sec 3
the seConD 2
```
выйти из режима редактирования `control+c`

----

14. Сделать текстовый файл tf_4.txt в котором будет 15 строк - `vim tf_4.txt`,

`i` - начать редактирование, 

ввести 15 строк,

клавишa `esc` - выйти из режима редактирования, 

клавиши `shift+:` - назначить команду,

`wq` - записать и закрыть редактор

----

15. Сделать текстовый файл tF_5.txt в котором будет 13 строк - `vim tF_5.txt`

`i` - начать редактирование, 

ввести 13 строк,

клавишa `esc` - выйти из режима редактирования, 

клавиши `shift+:` - назначить команду,

`wq` - записать и закрыть редактор

----

16. Вывести список всех файлов в папке - 
```
ls -la

total 24
drwxr-xr-x  5 dmitrijostalskij  staff  160 Apr 24 17:48 .
drwxr-xr-x  5 dmitrijostalskij  staff  160 Apr 24 14:13 ..
-rw-r--r--  1 dmitrijostalskij  staff  121 Apr 24 17:48 tF_5.txt
-rw-r--r--  1 dmitrijostalskij  staff   83 Apr 24 14:57 tf_3.txt
-rw-r--r--@ 1 dmitrijostalskij  staff  141 Apr 24 17:32 tf_4.txt
```
----

17. Выйти из папки inner_dir_1 - `cd ..`

----

18. Вывести содержимое файла tf_3.txt в терминал - 
```
cat inner_dir_1/tf_3.txt 

string 1 
string 2 
string 3
string 4
string 5
the second 2
the sec 2
the SeCoNd 2

```

----

19. Найти путь к файлу tf_4.txt -
```
find . -name  tf_4.txt

./hw_ksendzov_courses/dir_1/inner_dir_1/tf_4.txt
```
----

20. Отчистить файл tf_4.txt от содержимого без удаления самого файла - `cat /dev/null > tf_4.txt`

---

21. Найти путь к файлам у которых есть  “tf” в названии -
```
find . -name "tf*"

./hw_ksendzov_courses/dir_1/tf_1.txt
./hw_ksendzov_courses/dir_1/tf_2.txt
./hw_ksendzov_courses/dir_1/inner_dir_1/tf_3.txt
./hw_ksendzov_courses/dir_1/inner_dir_1/tf_4.txt
```
----

22. Найти путь к файлам у которых есть  “tf” в названии и буквы в любом регистре -
```
find . -iname "tf*"

./hw_ksendzov_courses/dir_1/tf_1.txt
./hw_ksendzov_courses/dir_1/tf_2.txt
./hw_ksendzov_courses/dir_1/inner_dir_1/tf_3.txt
./hw_ksendzov_courses/dir_1/inner_dir_1/tF_5.txt
./hw_ksendzov_courses/dir_1/inner_dir_1/tf_4.txt
```
----

23. Найти строки в файлах где есть комбинация букв “sec” в текущей папке -
```
grep "sec" ./*

grep: ./inner_dir_1: Is a directory
./tf_2.txt:the second 2
./tf_2.txt:the sec 3

```
-----

24. Найти строки в файлах где есть комбинация букв “sec” в любом регистре в текущей папке -
```
grep -i "sec" ./*

grep: ./inner_dir_1: Is a directory
./tf_2.txt:the second 2
./tf_2.txt:the sec 3
./tf_2.txt:the seConD 2

```
----

25. Найти строки в файлах где есть только комбинация букв “sec” в текущей папке -
```
grep -w "sec" ./*

grep: ./inner_dir_1: Is a directory
./tf_2.txt:the sec 3
```
----

26. Найти строки в файлах где есть только комбинация букв “sec” в любом регистре в текущей папке - 
```
grep -wi "sec" ./*

grep: ./inner_dir_1: Is a directory
./tf_2.txt:the sec 3
./tf_2.txt:the SeC 4

```
-----

27. Найти строки в файлах где есть комбинация букв “second” в текущей папке -
```
 grep 'second' ./*
 
grep: ./inner_dir_1: Is a directory
./tf_2.txt:the second 2
```
----

28. Найти строки в файлах где есть комбинация букв “second” в любом регистре в текущей папке -
```
grep -i  'second' ./*

grep: ./inner_dir_1: Is a directory
./tf_2.txt:the second 2
./tf_2.txt:the seConD 2
```
----

29. Найти строки в файлах где есть комбинация букв “second” во всех папках ниже уровнем -
```
grep -r  'second' ./*

./inner_dir_1/tf_3.txt:the second 2
./tf_2.txt:the second 2

```
----

30. Найти только путь и название файла в строках которых есть комбинация букв “second” в текущей папке -
```
grep -l  'second' ./*

grep: ./inner_dir_1: Is a directory
./tf_2.txt

```
----

31. Найти все строки во всех файлах где нет комбинации “second” -
```
grep -vr 'second' ./* 

./inner_dir_1/tf_3.txt:string 1 
./inner_dir_1/tf_3.txt:string 2 
./inner_dir_1/tf_3.txt:string 3
./inner_dir_1/tf_3.txt:string 4
./inner_dir_1/tf_3.txt:string 5
./inner_dir_1/tf_3.txt:the sec 2
./inner_dir_1/tf_3.txt:the SeCoNd 2
./inner_dir_1/tF_5.txt:string 1
./inner_dir_1/tF_5.txt:string 2
./inner_dir_1/tF_5.txt:string 3
./inner_dir_1/tF_5.txt:string 4
./inner_dir_1/tF_5.txt:string 5
./inner_dir_1/tF_5.txt:string 6
./inner_dir_1/tF_5.txt:string 7
./inner_dir_1/tF_5.txt:string 8
./inner_dir_1/tF_5.txt:string 9
./inner_dir_1/tF_5.txt:string 10
./inner_dir_1/tF_5.txt:string 11
./inner_dir_1/tF_5.txt:string 12
./inner_dir_1/tF_5.txt:string 13
./tf_2.txt:the first 1
./tf_2.txt:the third 3
./tf_2.txt:the sec 3
./tf_2.txt:the seConD 2
./tf_2.txt:the SeC 4

```
----

32. Найти только название и путь к файлам где нет комбинации “second” -
```
grep -Lr 'second' ./* 

./inner_dir_1/tF_5.txt
./inner_dir_1/tf_4.txt
./tf_1.txt

```
-----

33. Вывести в терминал 4 последних строк любого текстового файла - 
```
tail  -n4 tF_5.txt

string 10
string 11
string 12
string 13
```
-----

34. Вывести в терминал 4 первые строки любого текстового файла -
```
head -n4 tF_5.txt 

string 1
string 2
string 3
string 4
```
-----

35. Команда в одну строку. Создать папку и создать текстовый файл с содержиммым -
```
mkdir inner_dir_2  && cat > inner_dir_2/tf_6.txt
```
ввести текст и выйти из режима редактирования `control+c`

----

36. Команда в одну строку. Переместить в любую одну папку текстовые файлы у которых в содержимом есть слово “sec” -

```
grep -rli 'sec' ./* | xargs -I {} mv {} /Users/ostalskyi/hw_ksendzov_courses/dir_1/inner_dir_2

```
`-I` используется для указания символа, который будет использоваться для замены места, где должен быть подставлен каждый файл. В данном случае символ `{}` заменяет каждый файл, найденный командой `grep`.

-----

37. Команда в одну строку. Скопировать в любую одну папку текстовые файлы у которых в содержимом есть слово “sec” -

```
grep -rli 'sec' ./* | xargs -I {} cp {} /Users/ostalskyi/hw_ksendzov_courses/dir_1

```
----

38. Команда в одну строку. Найти все строки c “sec” во всех текстовых файлах, скопировать и вставить эти строки в один новый созданный текстовый файл -

```
grep -rh 'sec' ./* >>new_file.txt

```
----

39. Команда в одну строку. Удалить текстовые файлы у которых в содержимом есть слово “sec” -

```
grep -rl 'sec' ./* | xargs -I {} rm -r {}

```
----

40. Просто вывести в терминал строку “Good job!!” -

`echo 'Good job!!'`
