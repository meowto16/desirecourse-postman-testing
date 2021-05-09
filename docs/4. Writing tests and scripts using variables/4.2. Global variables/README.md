# Глобальные переменные (Global variables)

`{{myVariable}}` - Доступ к переменной.

## Примеры

![1. In request body](./img/1.%20In%20request.png)

![2. In request body](./img/2.%20In%20request%20body.png)

## Установка переменных в скрипте

```js
pm.globals.get('variable_key') // Получение глобальной переменной

pm.globals.set('variable_key', 'variable_value') // Установка глобальной переменной

pm.globals.unset('variable_key') // Очищает конкретную глобальную переменную

pm.globals.clear() // Удаляет все глобальные переменные
```
