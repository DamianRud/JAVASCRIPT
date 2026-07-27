# 📘 JavaScript — Конспект: Получение данных из `<input>`

## 📑 Содержание

- [Что такое `<input>`?](#-что-такое-input)
- [Получить поле](#-получить-поле)
- [Что такое value?](#-что-такое-value)
- [Получить кнопку и элемент вывода](#-получить-кнопку-и-элемент-вывода)
- [Полный пример](#-полный-пример)
- [Проверка через if](#-проверка-через-if)
- [console.log() и textContent](#-consolelog-и-textcontent)
- [Шпаргалка](#-шпаргалка)
- [Что уже изучено](#-что-уже-изучено)

---

## 🧩 Что такое `<input>`?

`<input>` — это поле, в которое пользователь может вводить текст.

### HTML

```html
<input id="name" type="text" placeholder="Введите имя">
```

---

## 🔍 Получить поле

Используется:

```javascript
document.getElementById()
```

### Пример

```javascript
let input = document.getElementById("name");
```

> Теперь переменная `input` хранит поле ввода.

---

## 📥 Что такое `value`?

У каждого `<input>` есть свойство:

```javascript
input.value
```

Оно содержит **то, что ввёл пользователь**.

Если пользователь написал:

```text
Damian
```

то

```javascript
console.log(input.value);
```

выведет

```text
Damian
```

---

## 🔘 Получить кнопку и элемент вывода

**Кнопка:**

```javascript
let button = document.getElementById("btn");
```

**Элемент для вывода:**

```javascript
let result = document.getElementById("result");
```

Например:

```html
<h2 id="result"></h2>
```

---

## 🧪 Полный пример

```javascript
let input = document.getElementById("name");
let button = document.getElementById("btn");
let result = document.getElementById("result");

button.addEventListener("click", function () {
    result.textContent = "Привет, " + input.value + "!";
});
```

Если пользователь введёт:

```text
Damian
```

То получится:

```text
Привет, Damian!
```

---

## ☑️ Проверка через if

Можно проверить, пустое ли поле.

```javascript
if (input.value === "") {
    result.textContent = "Введите имя!";
} else {
    result.textContent = "Привет, " + input.value + "!";
}
```

---

## 🖥️ `console.log()` и `textContent`

### `console.log()`

Используется для программиста.

```javascript
console.log(input.value);
```

Результат видно только в:

```text
F12 → Console
```

### `textContent`

Используется для пользователя.

```javascript
result.textContent = "Введите имя!";
```

> Сообщение появится прямо на странице.

---

## 🧠 Что важно запомнить

```javascript
// Получить input
let input = document.getElementById("name");

// Получить текст
input.value;

// Изменить текст
result.textContent = "...";

// Проверить пустое поле
if (input.value === "") {

}

// Нажатие кнопки
button.addEventListener("click", function () {

});
```

---

## ✅ Что уже изучено

- [x] Переменные (`let`, `const`)
- [x] Математические операции
- [x] `if`, `else`
- [x] Логические операторы (`&&`, `||`, `!`)
- [x] `for`
- [x] `while`
- [x] Массивы
- [x] Функции
- [x] `return`
- [x] DOM
- [x] `document.getElementById()`
- [x] `textContent`
- [x] `style`
- [x] `onclick`
- [x] `addEventListener()`
- [x] `createElement()`
- [x] `appendChild()`
- [x] `input.value`

---

## 📋 Шпаргалка

| Метод/свойство | Назначение |
|---|---|
| `document.getElementById()` | найти элемент |
| `textContent` | изменить текст (для пользователя) |
| `style` | изменить CSS |
| `addEventListener()` | ждать событие |
| `createElement()` | создать HTML-элемент |
| `appendChild()` | добавить элемент |
| `input.value` | получить то, что ввёл пользователь |
| `console.log()` | вывод для программиста |

