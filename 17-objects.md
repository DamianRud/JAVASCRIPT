# JavaScript — Конспект

## 17. Объекты (Object)

### Что такое объект?

Объект позволяет хранить **несколько связанных данных в одной переменной**.

Вместо:

```javascript
let name = "Damian";
let age = 16;
let city = "Tallinn";
```

Можно написать:

```javascript
let person = {
  name: "Damian",
  age: 16,
  city: "Tallinn",
};
```

---

### Структура объекта

```javascript
let person = {
  name: "Damian",
  age: 16,
  city: "Tallinn",
};
```

Каждая строка состоит из:

```text
ключ : значение
```

Например:

```javascript
name: "Damian"
```

* `name` — ключ
* `"Damian"` — значение

---

### Получить значение

Используется точка (`.`).

```javascript
console.log(person.name);
```

Результат:

```text
Damian
```

```javascript
console.log(person.age);
```

Результат:

```text
16
```

```javascript
console.log(person.city);
```

Результат:

```text
Tallinn
```

---

### Изменить значение

```javascript
person.age = 17;
```

Теперь

```javascript
console.log(person.age);
```

выведет

```text
17
```

---

### Добавить новое свойство

Если свойства ещё нет:

```javascript
person.language = "JavaScript";
```

Теперь объект стал:

```javascript
let person = {
  name: "Damian",
  age: 17,
  city: "Tallinn",
  school: "TTHK",
  language: "JavaScript",
};
```

---

## Массив объектов

Иногда нужно хранить **несколько объектов**.

Для этого используется массив.

```javascript
let games = [
  {
    name: "CS2",
    price: 75,
  },
  {
    name: "Minecraft",
    price: 30,
  },
  {
    name: "GTA V",
    price: 55,
  },
];
```

### Как получить объект?

Первый элемент массива:

```javascript
games[0]
```

Второй:

```javascript
games[1]
```

Третий:

```javascript
games[2]
```

---

### Получить свойство объекта

Название первой игры:

```javascript
console.log(games[0].name);
```

Результат:

```text
CS2
```

Цена второй игры:

```javascript
console.log(games[1].price);
```

Результат:

```text
30
```

Название третьей игры:

```javascript
console.log(games[2].name);
```

Результат:

```text
GTA V
```

---

## Цикл по массиву объектов

Можно вывести все игры сразу.

```javascript
for (let i = 0; i < games.length; i++) {
  console.log(games[i].name);
}
```

Получится:

```text
CS2
Minecraft
GTA V
```

Можно вывести название и цену.

```javascript
for (let i = 0; i < games.length; i++) {
  console.log(games[i].name + " - " + games[i].price);
}
```

Получится:

```text
CS2 - 75
Minecraft - 30
GTA V - 55
```

---

## Использование DOM

Можно выводить данные не в консоль, а на страницу.

HTML

```html
<div id="games"></div>
```

JavaScript

```javascript
let container = document.getElementById("games");

for (let i = 0; i < games.length; i++) {
  let title = document.createElement("h2");

  title.textContent = games[i].name;

  container.appendChild(title);
}
```

На странице появится:

```text
CS2

Minecraft

GTA V
```

---

## Что важно запомнить

**Создать объект**

```javascript
let person = {
  name: "Damian",
  age: 16,
};
```

**Получить значение**

```javascript
person.name
```

**Изменить значение**

```javascript
person.age = 17;
```

**Добавить новое свойство**

```javascript
person.language = "JavaScript";
```

**Массив объектов**

```javascript
let games = [
  {},
  {},
  {},
];
```

**Получить объект**

```javascript
games[0]
```

**Получить свойство объекта**

```javascript
games[0].name
```

**Цикл по массиву объектов**

```javascript
for (let i = 0; i < games.length; i++) {

}
```

---

## Что уже изучено

- [x] Переменные (`let`, `const`)
- [x] Математические операции
- [x] `if`, `else`
- [x] Логические операторы
- [x] `for`
- [x] `while`
- [x] Массивы
- [x] Функции
- [x] `return`
- [x] DOM
- [x] `document.getElementById()`
- [x] `textContent`
- [x] `style`
- [x] `addEventListener()`
- [x] `createElement()`
- [x] `appendChild()`
- [x] `input.value`
- [x] Объекты (`Object`)
- [x] Массив объектов

---

## Моя шпаргалка

```text
object → хранит несколько связанных данных.

ключ → значение

person.name → получить значение.

person.age = 17 → изменить значение.

person.language = "JavaScript" → добавить новое свойство.

[] → массив.

{} → объект.

games[0] → первый объект массива.

games[0].name → свойство объекта.

for + games[i] → пройти по всему массиву объектов.
```
