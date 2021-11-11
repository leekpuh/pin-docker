FROM python:3.9

# Рабочая директория в нашем контейнере
WORKDIR /usr/src/pin-app/

# Копируем файл зависимостей в контейнер
COPY requirments.txt /usr/src/requirments.txt 

# Запускаем установку зависимостей
RUN pip install --upgrade pip && pip install -r /usr/src/requirments.txt 

# Копируем весь проект в контейнер
COPY . /usr/src/pin-app

# Контейнер слушает порт 8080
EXPOSE 8000

# Инструкция запуска при старте контейнера
ENTRYPOINT ["python", "/usr/src/pin-app/manage.py"]