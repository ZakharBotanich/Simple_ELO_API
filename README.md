# Для запуска API (nginx + backend + db)
1) Создать папку data для БД
```
mkdir ./db/data
```
2)  Выполнить команду
```
 sudo docker-compose up
```
# Примеры обращения к API
1) Добавление нового пользователя с рейтингом
```
curl -X POST http://localhost/users -H "Content-Type: application/json" -d '{"name": "Alice", "elo": 1200}'
curl -X POST http://localhost/users -H "Content-Type: application/json" -d '{"name": "Bob", "elo": 1400}'
```
2) Расчет рейтинга ЭЛО после
```
curl -X POST http://localhost/match \
  -H "Content-Type: application/json" \
  -d '{
        "user_a": "Alice",
        "user_b": "Bob",
        "score_a": 1
      }'
```
3) Получение рейтинговой таблицы - http://localhost/users
   
   
