# 📘 JavaScript — Конспект: Создание HTML-элементов

## 📑 Содержание

- [Что такое createElement()?](#-что-такое-createelement)
- [Добавить текст](#-добавить-текст)
- [Добавить элемент на страницу](#-добавить-элемент-на-страницу)
- [Полный пример](#-полный-пример)
- [Создание заголовка](#-создание-заголовка)
- [Создание кнопки](#-создание-кнопки)
- [Изменение стиля](#-изменение-стиля)
- [Создание списка](#-создание-списка)
- [Добавление элемента по нажатию кнопки](#-добавление-элемента-по-нажатию-кнопки)
- [Шпаргалка](#-шпаргалка)
- [Что уже изучено](#-что-уже-изучено)

---

## 🧩 Что такое `createElement()`?

Позволяет JavaScript **создать новый HTML-элемент**.

### Пример

```javascript
let p = document.createElement("p");
```

JavaScript создаёт:

```html
<p></p>
```

> ⚠️ Этот элемент ещё **не отображается на странице**.

---

## ✏️ Добавить текст

Используется свойство:

```javascript
textContent
```

### Пример

```javascript
let p = document.createElement("p");

p.textContent = "Привет!";
```

Получится:

```html
<p>Привет!</p>
```

---

## 📌 Добавить элемент на страницу

Используется метод:

```javascript
appendChild()
```

### Пример

```javascript
document.body.appendChild(p);
```

> Теперь элемент появится на странице.

---

## 🧪 Полный пример

```javascript
let p = document.createElement("p");

p.textContent = "Я изучаю JavaScript!";

document.body.appendChild(p);
```

**Результат:**

```text
Я изучаю JavaScript!
```

---

## 🔠 Создание заголовка

```javascript
let title = document.createElement("h1");

title.textContent = "Damian";

document.body.appendChild(title);
```

---

## 🔘 Создание кнопки

```javascript
let button = document.createElement("button");

button.textContent = "Купить";

document.body.appendChild(button);
```

---

## 🎨 Изменение стиля

```javascript
let p = document.createElement("p");

p.textContent = "JavaScript";

p.style.color = "green";

document.body.appendChild(p);
```

---

## 📃 Создание списка

**HTML:**

```html
<ul id="list"></ul>
```

**JavaScript:**

```javascript
let list = document.getElementById("list");

let li = document.createElement("li");

li.textContent = "iPhone";

list.appendChild(li);
```

**Результат:**

```text
• iPhone
```

---

## 🖱️ Добавление элемента по нажатию кнопки

```javascript
let button = document.getElementById("btn");
let list = document.getElementById("list");

button.addEventListener("click", function () {

    let li = document.createElement("li");

    li.textContent = "iPhone";

    list.appendChild(li);

});
```

> Каждое нажатие создаёт новый элемент.

**Например:**

```text
• iPhone
• iPhone
• iPhone
```

---

## 🧠 Что важно запомнить

```javascript
// Создать элемент
document.createElement("тег");

// Изменить текст
element.textContent = "...";

// Изменить стиль
element.style.color = "...";

// Добавить на страницу
document.body.appendChild(element);
// или
list.appendChild(element);
```

---

## ✅ Что уже изучено

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
- [x] `onclick`
- [x] `addEventListener()`
- [x] `createElement()`
- [x] `appendChild()`

---

## 📋 Шпаргалка

| Метод/свойство | Назначение |
|---|---|
| `document.getElementById()` | найти элемент |
| `textContent` | изменить текст |
| `style` | изменить CSS |
| `onclick` | старый способ обработки события |
| `addEventListener()` | современный способ обработки события |
| `document.createElement()` | создать новый HTML-элемент |
| `appendChild()` | добавить элемент на страницу |

