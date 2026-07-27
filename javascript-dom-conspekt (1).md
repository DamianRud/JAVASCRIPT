# 📘 JavaScript — Конспект: DOM (Document Object Model)

## 📑 Содержание

- [Что такое DOM?](#-что-такое-dom)
- [Получить элемент](#-получить-элемент)
- [Изменение текста](#-изменение-текста)
- [Изменение стилей](#-изменение-стилей)
- [Полный пример](#-полный-пример)
- [Кнопки и события](#-кнопки-и-события)
- [Шпаргалка](#-шпаргалка)
- [Что уже изучено](#-что-уже-изучено)

---

## 🧩 Что такое DOM?

**DOM** позволяет JavaScript работать с HTML-страницей.

С помощью DOM можно:

- ✏️ менять текст;
- 🎨 менять стили;
- 🖼️ менять картинки;
- 🖱️ реагировать на нажатия кнопок;
- ➕➖ создавать и удалять элементы.

---

## 🔍 Получить элемент

Используется метод:

```javascript
document.getElementById("id")
```

### Пример

**HTML:**

```html
<h1 id="title">Привет</h1>
```

**JavaScript:**

```javascript
let title = document.getElementById("title");
```

> Теперь переменная `title` хранит этот заголовок.

---

## ✏️ Изменение текста

Используется свойство:

```javascript
textContent
```

### Пример

```javascript
let title = document.getElementById("title");

title.textContent = "Добро пожаловать!";
```

| До | После |
|---|---|
| `Привет` | `Добро пожаловать!` |

---

## 🎨 Изменение стилей

Используется свойство:

```javascript
style
```

### Цвет текста

```javascript
title.style.color = "blue";
```

### Цвет фона

```javascript
title.style.backgroundColor = "gray";
```

### Размер текста

```javascript
title.style.fontSize = "48px";
```

### Выравнивание

```javascript
title.style.textAlign = "center";
```

---

## 🧪 Полный пример

```javascript
let title = document.getElementById("title");

title.textContent = "Добро пожаловать!";

title.style.color = "blue";
title.style.fontSize = "48px";
title.style.backgroundColor = "gray";
title.style.textAlign = "center";
```

---

## 🖱️ Кнопки и события

**HTML:**

```html
<h1 id="title">Привет</h1>

<button id="btn">Изменить текст</button>
```

Получаем кнопку:

```javascript
let button = document.getElementById("btn");
```

### `onclick`

Позволяет выполнить код после нажатия кнопки.

```javascript
button.onclick = function () {

};
```

### Пример

```javascript
let title = document.getElementById("title");
let button = document.getElementById("btn");

button.onclick = function () {
    title.textContent = "Привет, Damian!";
};
```

| До нажатия | После нажатия |
|---|---|
| `Привет` | `Привет, Damian!` |

---

## 🧠 Что важно запомнить

```javascript
// Получить элемент
document.getElementById("id");

// Изменить текст
element.textContent = "...";

// Изменить стиль
element.style.color = "...";
element.style.fontSize = "...";
element.style.backgroundColor = "...";
element.style.textAlign = "...";

// Нажатие кнопки
button.onclick = function () {

};
```

---

## ✅ Что уже изучено

- [x] Переменные (`let`, `const`)
- [x] Математические операции
- [x] Сравнение (`>`, `<`, `==`, `===`)
- [x] `if`, `else`
- [x] Логические операторы (`&&`, `||`, `!`)
- [x] `for`
- [x] `while`
- [x] Массивы
- [x] `push()`
- [x] `pop()`
- [x] `unshift()`
- [x] `shift()`
- [x] `for` + массив
- [x] Функции
- [x] Параметры
- [x] `return`
- [x] DOM
- [x] `document.getElementById()`
- [x] `textContent`
- [x] `style`
- [x] `onclick`

---

## 📋 Шпаргалка

| Метод/свойство | Назначение |
|---|---|
| `document.getElementById()` | получить элемент |
| `textContent` | изменить текст |
| `style` | изменить CSS |
| `onclick` | выполнить код после нажатия |
| `function` | создать функцию |
| `return` | вернуть значение |
| `for` | цикл |
| `array[i]` | получить элемент массива |

