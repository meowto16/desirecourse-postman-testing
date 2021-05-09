# Рефакторим тест

1. Убираем повторения, выносим наверх все, что повторяется
2. Переименуем `jsonData` на `response`
3. Лучше использовать `const` вместо `var` х), окей

```js
const response = pm.response.json()

pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Board should be created", function () {
    pm.expect(response.name).to.eql("My new board");
    pm.expect(response.closed).to.eql(false)
});

pm.test('Board should be private', function () {
    pm.expect(response.prefs.permissionLevel).to.eql("private")
})
```
