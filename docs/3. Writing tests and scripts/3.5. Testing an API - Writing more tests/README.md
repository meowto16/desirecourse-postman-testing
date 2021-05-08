# Тестируем API - Пишем больше тестов

Пока ничего супер особенного. Это можно узнать почитав доку.

```js
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Board should be created", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.name).to.eql("My new board");
    pm.expect(jsonData.closed).to.eql(false)
});

pm.test('Board should be private', function () {
    var jsonData = pm.response.json()
    pm.expect(jsonData.prefs.permissionLevel).to.eql("private")
})
```
