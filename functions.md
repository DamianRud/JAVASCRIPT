# JavaScript — Функции (Functions)

## Что такое функция?

Функция — это кусок кода, который можно вызвать в любой момент.

---

## Создание функции

```javascript
function hello() {
    console.log("Привет");
}
```

---

## Вызов функции

```javascript
hello();
```

Ответ:

```text
Привет
```

---

## Функция с параметром

```javascript
function hello(name) {
    console.log(name);
}

hello("Damian");
```

Ответ:

```text
Damian
```

---

## Несколько параметров

```javascript
function person(name, age) {
    console.log(name);
    console.log(age);
}

person("Damian", 16);
```

Ответ:

```text
Damian
16
```

---

## return

### Что делает?

Возвращает результат из функции.

### Пример

```javascript
function add(a, b) {
    return a + b;
}

console.log(add(5, 3));
```

Ответ:

```text
8
```

---

### Ещё пример

```javascript
function square(number) {
    return number * number;
}

console.log(square(5));
```

Ответ:

```text
25
```

---

## Разница между console.log() и return

### console.log()

Только выводит информацию.

```javascript
console.log("Привет");
```

---

### return

Возвращает значение, которое можно сохранить.

```javascript
function add(a, b) {
    return a + b;
}

let result = add(5, 3);

console.log(result);
```

Ответ:

```text
8
```

---

## Шпаргалка

```text
function    → создать функцию

параметр    → данные внутри функции

return      → вернуть результат
```
