# Введение и первые шаги в Postman (продолжение)

###  Проброс данных между запросами

1. Создаем новый GET запрос `httpbin.org/uuid` (он возвращает JSON, с рандомным uuid)
2. Заходим во вкладку Tests для этого запроса. Пишем следующий код:

```javascript
const { uuid } = pm.response.json() // Забираем uuid из ответа
pm.globals.set("uuid", uuid) // Устанавливаем глобальную переменную
```

3. Заходим в наш POST запрос, меняем body, используя `{{uuid}}` переменную
```json
{
    "name": "John",
    "email": "john@example.com",
    "uuid": "{{uuid}}"
}
```

4. Готово, теперь нам не надо копировать в тупую, а мы используем переменные, вау.

## Простенький тест для запроса.

```javascript
pm.test('Status code is 200', function () {
  pm.response.to.have.status(200)
})
```

Вкладка **Test results**

![1. Test results](./images/1.%20Test%20results.png)

## Runner

В Postman есть Runner для коллекций, он запускает все запросы и показывает — прошли они тесты или нет.

![2. Runner](./images/2.%20Runner.png)
