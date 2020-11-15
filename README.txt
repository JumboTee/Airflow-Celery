# Запускать в такой последовательности:
# 1. Создание БД
docker-compose up init_db

# 2. Запуск scheduler, worker, flower и их зависимостей (redis, webserver, postgres)
docker-compose up -d --scale worker=5 scheduler worker flower
