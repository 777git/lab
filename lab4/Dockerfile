FROM python:3.9-slim

LABEL author="nazar"
LABEL version=1.0

# оновлюємо систему
RUN apt-get update && apt-get upgrade -y

# Встановлюємо потрібні пакети
RUN apt-get install git -y && pip install pipenv

# Створюємо робочу папку
WORKDIR /lab

# Завантажуємо файли з Git
RUN git clone https://github.com/777git/lab.git

# Створюємо остаточну робочу папку з Веб-сайтом та копіюємо туди файли
WORKDIR /app
RUN cp -r /lab/lab/lab3/* .

# Інсталюємо всі залежності

RUN pipenv install
RUN pipenv install django

# Відкриваємо порт 8000 на зовні
EXPOSE 8000


# Це команда яка виконається при створенні контейнера
RUN pipenv run python manage.py migrate

ENTRYPOINT ["pipenv", "run", "python", "manage.py", "runserver", "0.0.0.0:8000"]