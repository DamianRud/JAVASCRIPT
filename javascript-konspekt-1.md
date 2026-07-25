# JavaScript — Конспект №1

## 1. Подключение JavaScript

Создаём файл:

```text
script.js
```

Подключаем его в конце файла `index.html`:

```html
<script src="script.js"></script>
```

## 2. console.log()

**Что делает?**
Выводит информацию в консоль браузера.

**Пример**

```javascript
console.log("Привет, JavaScript!");
```

**Результат**

```text
Привет, JavaScript!
```

`console.log()` нужен программисту для проверки работы программы.

## 3. Переменные

**Что такое переменная?**
Переменная — это место, где хранится информация.

**Создание переменной**

```javascript
let name = "Damian";
```

Здесь:
- `let` — создаёт переменную.
- `name` — имя переменной.
- `"Damian"` — значение.

**Вывод переменной**

```javascript
let name = "Damian";

console.log(name);
```

Результат:

```text
Damian
```

**Изменение значения**

```javascript
let product = "iPhone";

product = "Apple Watch";

console.log(product);
```

Результат:

```text
Apple Watch
```

После создания переменной её значение можно изменить.

## 4. Типы данных

**Текст (String)**

```javascript
let city = "Tallinn";
```

Текст всегда пишется в кавычках.

**Число (Number)**

```javascript
let age = 16;
```

Числа пишутся без кавычек.

**Логическое значение (Boolean)**

```javascript
let student = true;
```

или

```javascript
let student = false;
```

## 5. Арифметические операторы

**Сложение**

```javascript
let a = 10;
let b = 5;

console.log(a + b);
```

Ответ:

```text
15
```

**Вычитание**

```javascript
console.log(a - b);
```

Ответ:

```text
5
```

**Умножение**

```javascript
console.log(a * b);
```

Ответ:

```text
50
```

**Деление**

```javascript
console.log(a / b);
```

Ответ:

```text
2
```

**Остаток от деления**

```javascript
console.log(20 % 6);
```

Как считается:

```text
20 ÷ 6 = 3
3 × 6 = 18
20 - 18 = 2
```

Ответ:

```text
2
```

**Возведение в степень**

```javascript
console.log(2 ** 3);
```

Ответ:

```text
8
```

Потому что:

```text
2 × 2 × 2 = 8
```

## Что уже изучено

- ✅ Подключение JavaScript
- ✅ `console.log()`
- ✅ Переменные (`let`)
- ✅ Типы данных
- ✅ Арифметические операторы

## Моя шпаргалка

| Символ / Слово | Значение |
|---|---|
| `script.js` | файл JavaScript |
| `<script src="script.js"></script>` | подключение JavaScript |
| `console.log()` | вывод информации в консоль |
| `let` | создание переменной |
| `+` | сложение |
| `-` | вычитание |
| `*` | умножение |
| `/` | деление |
| `%` | остаток от деления |
| `**` | возведение в степень |
