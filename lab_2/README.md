
# Загальне
Використовуваний дистрибутив **Linux Debian**

# 2
### Команди для створення віртуального середовища
```
python3 -m pip install pipenv;
python3 -m pipenv --python 3.7;
	
```
---

# 3
### Команди для завантаження бібліотек
```
python3 -m pipenv install requests;
python3 -m pipenv install ntplib;
```
---

# 5
### Перевірка роботи програми
```
python3 -m pipenv run python app.py
========================================
Результат без параметрів: 
No URL passed to function
========================================
Результат з правильною URL: 
Time is:  06:18:31 PM
Date is:  18-01-2021
Доброї ночі

```
---

# 6
### Команда для завантаження бібліотеки для тестів
```
python3 -m pipenv install pytest;
```
---

# 7 
### Перевірка та запуск тестів
```
python3 -m pipenv run pytest tests/tests.py
========================================================================= test session starts ==========================================================================
platform linux -- Python 3.7.5, pytest-6.1.1, py-1.9.0, pluggy-0.13.1
rootdir: /home/user/lab/lab_2/
collected 4 items

tests/tests.py ....          