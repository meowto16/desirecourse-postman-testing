# Pre-request скрипты

- Тоже самое, что и скрипты в тестах, но без assertion'ов
- Хорошо подходит, чтобы сделать запросы динамичными
- Обычно используется в комбинации с переменными

```javascript
pm.environment.set('boardName', getRandomBoardName())

function getRandomBoardName() {
  return "My board name " + parseInt(Math.random() * 10000)
}
```

Из полезного: в Pre-request можно установить переменную, а юзать уже в Params или Body запроса, что очень удобно.
Особенно когда необходимо сгенерировать какой-либо параметр
