# Тестируем API

1. Создаем аккаунт в Trello
2. Забираем app-key https://trello.com/app-key
3. Вручную генерим токен, нажав на ссылку *Token* на данной странице
4. Создаем новую коллекцию в Postman
5. Задаем переменные API_KEY и API_TOKEN, закидываем туда наши key и token. Задаем ``{{baseUrl}}`` - https://api.trello.com
6. Создаем новый запрос `{{baseUrl}}/1/boards/?name=My new board&key={{API_KEY}}&token={{API_TOKEN}}&defaultLists=false`
7. Пробуем сделать запрос
8. PROFIT!
