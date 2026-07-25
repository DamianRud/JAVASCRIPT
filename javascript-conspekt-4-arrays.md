# JavaScript — Конспект №4

## Массивы: все основные команды (методы)

### Что такое массив?

Массив — это список значений, хранящихся в одной переменной.

```javascript
let fruits = ["яблоко", "банан", "груша"];
```

Элементы нумеруются с 0.

```text
fruits[0] → "яблоко"
fruits[1] → "банан"
fruits[2] → "груша"
```

---

### `length` — узнать количество элементов

```javascript
let fruits = ["яблоко", "банан", "груша"];
console.log(fruits.length);
```

Результат:

```text
3
```

---

## Добавление и удаление элементов

### `push()` — добавить элемент в конец

```javascript
let fruits = ["яблоко", "банан"];
fruits.push("груша");

console.log(fruits);
```

Результат:

```text
["яблоко", "банан", "груша"]
```

### `pop()` — удалить последний элемент

```javascript
let fruits = ["яблоко", "банан", "груша"];
fruits.pop();

console.log(fruits);
```

Результат:

```text
["яблоко", "банан"]
```

### `unshift()` — добавить элемент в начало

```javascript
let fruits = ["банан", "груша"];
fruits.unshift("яблоко");

console.log(fruits);
```

Результат:

```text
["яблоко", "банан", "груша"]
```

### `shift()` — удалить первый элемент

```javascript
let fruits = ["яблоко", "банан", "груша"];
fruits.shift();

console.log(fruits);
```

Результат:

```text
["банан", "груша"]
```

---

## Поиск в массиве

### `indexOf()` — найти индекс элемента

```javascript
let fruits = ["яблоко", "банан", "груша"];
console.log(fruits.indexOf("банан"));
```

Результат:

```text
1
```

Если элемента нет — вернёт `-1`.

### `includes()` — проверить, есть ли элемент

```javascript
let fruits = ["яблоко", "банан", "груша"];
console.log(fruits.includes("банан"));
console.log(fruits.includes("апельсин"));
```

Результат:

```text
true
false
```

### `find()` — найти первый элемент по условию

```javascript
let numbers = [4, 9, 15, 22, 30];
let result = numbers.find(n => n > 10);

console.log(result);
```

Результат:

```text
15
```

### `findIndex()` — найти индекс по условию

```javascript
let numbers = [4, 9, 15, 22, 30];
let result = numbers.findIndex(n => n > 10);

console.log(result);
```

Результат:

```text
2
```

---

## Перебор массива

### `forEach()` — выполнить код для каждого элемента

```javascript
let fruits = ["яблоко", "банан", "груша"];

fruits.forEach(function(fruit) {
    console.log(fruit);
});
```

Результат:

```text
яблоко
банан
груша
```

### `map()` — создать новый массив с изменёнными значениями

```javascript
let numbers = [1, 2, 3];
let doubled = numbers.map(n => n * 2);

console.log(doubled);
```

Результат:

```text
[2, 4, 6]
```

### `filter()` — создать новый массив, отобрав элементы по условию

```javascript
let numbers = [1, 2, 3, 4, 5, 6];
let even = numbers.filter(n => n % 2 === 0);

console.log(even);
```

Результат:

```text
[2, 4, 6]
```

### `reduce()` — свернуть массив в одно значение

```javascript
let numbers = [1, 2, 3, 4];
let sum = numbers.reduce((total, n) => total + n, 0);

console.log(sum);
```

Результат:

```text
10
```

---

## Изменение и преобразование массива

### `slice()` — вырезать часть массива (не изменяет исходный)

```javascript
let fruits = ["яблоко", "банан", "груша", "манго"];
let part = fruits.slice(1, 3);

console.log(part);
console.log(fruits);
```

Результат:

```text
["банан", "груша"]
["яблоко", "банан", "груша", "манго"]
```

### `splice()` — удалить/добавить элементы (изменяет исходный массив)

```javascript
let fruits = ["яблоко", "банан", "груша"];
fruits.splice(1, 1, "апельсин");

console.log(fruits);
```

Результат:

```text
["яблоко", "апельсин", "груша"]
```

`splice(индекс, сколько удалить, что добавить)`

### `concat()` — объединить массивы

```javascript
let a = [1, 2];
let b = [3, 4];
let result = a.concat(b);

console.log(result);
```

Результат:

```text
[1, 2, 3, 4]
```

### `join()` — превратить массив в строку

```javascript
let fruits = ["яблоко", "банан", "груша"];
console.log(fruits.join(", "));
```

Результат:

```text
яблоко, банан, груша
```

### `reverse()` — перевернуть порядок элементов

```javascript
let numbers = [1, 2, 3];
numbers.reverse();

console.log(numbers);
```

Результат:

```text
[3, 2, 1]
```

### `sort()` — отсортировать массив

```javascript
let numbers = [5, 1, 4, 2, 3];
numbers.sort();

console.log(numbers);
```

Результат:

```text
[1, 2, 3, 4, 5]
```

⚠️ Для чисел `sort()` по умолчанию сортирует как строки.
Правильный вариант для чисел:

```javascript
let numbers = [10, 1, 21, 2];
numbers.sort((a, b) => a - b);

console.log(numbers);
```

Результат:

```text
[1, 2, 10, 21]
```

---

## Проверки

### `every()` — проверить, что ВСЕ элементы удовлетворяют условию

```javascript
let numbers = [2, 4, 6, 8];
console.log(numbers.every(n => n % 2 === 0));
```

Результат:

```text
true
```

### `some()` — проверить, что ХОТЯ БЫ ОДИН элемент удовлетворяет условию

```javascript
let numbers = [1, 3, 5, 8];
console.log(numbers.some(n => n % 2 === 0));
```

Результат:

```text
true
```

### `Array.isArray()` — проверить, является ли значение массивом

```javascript
console.log(Array.isArray([1, 2, 3]));
console.log(Array.isArray("привет"));
```

Результат:

```text
true
false
```

---

## Таблица: изменяют ли метод исходный массив?

| Метод | Изменяет исходный массив? |
|---|---|
| `push()` | ✅ Да |
| `pop()` | ✅ Да |
| `shift()` | ✅ Да |
| `unshift()` | ✅ Да |
| `splice()` | ✅ Да |
| `sort()` | ✅ Да |
| `reverse()` | ✅ Да |
| `slice()` | ❌ Нет |
| `map()` | ❌ Нет |
| `filter()` | ❌ Нет |
| `concat()` | ❌ Нет |
| `join()` | ❌ Нет |

---

## Что уже изучено

- ✅ Подключение JavaScript
- ✅ `console.log()`
- ✅ Переменные (`let`)
- ✅ Типы данных
- ✅ Арифметические операторы
- ✅ Операторы сравнения
- ✅ `if`, `else`, `else if`
- ✅ Логические операторы (`&&`, `||`, `!`)
- ✅ Цикл `for`
- ✅ Цикл `while`
- ✅ Массивы и их методы

## Моя шпаргалка

- `push()` / `pop()` → добавить / удалить с конца.
- `unshift()` / `shift()` → добавить / удалить с начала.
- `indexOf()` / `includes()` → поиск элемента.
- `find()` / `findIndex()` → поиск по условию.
- `forEach()` → пройтись по массиву.
- `map()` → создать новый массив с изменениями.
- `filter()` → отобрать элементы по условию.
- `reduce()` → свернуть массив в одно значение.
- `slice()` → вырезать часть (не меняя оригинал).
- `splice()` → удалить/вставить (меняя оригинал).
- `concat()` → объединить массивы.
- `join()` → массив → строка.
- `sort()` / `reverse()` → сортировка и разворот.
- `every()` / `some()` → проверки условий.
