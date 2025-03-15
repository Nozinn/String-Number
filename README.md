
# String and Number in JavaScript

## 📌 Introduction
JavaScript предоставляет два фундаментальных типа данных для работы с текстом и числами: **String** (строка) и **Number** (число). Эти типы используются для представления данных в большинстве программ и имеют множество встроенных методов и особенностей. В этом руководстве мы разберем ключевые концепции, методы и операции, связанные с этими типами.

---

## 📜 Strings in JavaScript

### 🔹 Что такое строки?
Строки в JavaScript — это последовательность символов, заключенных в кавычки. Они могут содержать буквы, цифры, пробелы и другие символы.

### 🔹 Способы объявления строк
В JavaScript строки можно задавать тремя способами:
```javascript
let singleQuote = 'Hello';   // одинарные кавычки
let doubleQuote = "World";   // двойные кавычки
let templateLiteral = `Hello, ${doubleQuote}!`; // шаблонные строки (поддерживают интерполяцию)
```

### 🔹 Особенности строк
1. **Строки неизменяемы** – после создания строки её нельзя изменить, можно только создать новую.
2. **Поддержка юникода** – строки могут содержать символы из различных алфавитов и эмодзи.
3. **Индексация** – доступ к символам осуществляется по индексу, начиная с `0`.

```javascript
let text = "JavaScript";
console.log(text[0]);  // "J"
console.log(text.charAt(4)); // "S"
```

### 🔹 Методы строк
Строки обладают множеством полезных методов:
```javascript
let text = "JavaScript";
console.log(text.length);        // 10 (длина строки)
console.log(text.toUpperCase()); // "JAVASCRIPT"
console.log(text.toLowerCase()); // "javascript"
console.log(text.includes("Script")); // true
console.log(text.replace("Java", "ECMA")); // "ECMAScript"
console.log(text.split("a")); // ["J", "v", "Script"]
```

### 🔹 Конкатенация строк
Объединение строк может быть выполнено разными способами:
```javascript
let firstName = "John";
let lastName = "Doe";
console.log(firstName + " " + lastName); // "John Doe"
console.log(`${firstName} ${lastName}`); // "John Doe" (Шаблонные строки)
```

---

## 🔢 Numbers in JavaScript

### 🔹 Что такое числа?
В JavaScript числа представлены единственным типом данных — `Number`. В отличие от многих других языков программирования, в JavaScript нет разделения на целые и дробные числа.

### 🔹 Виды чисел
1. **Целые числа**
```javascript
let integer = 42;
```
2. **Десятичные дроби**
```javascript
let float = 3.14;
```
3. **Экспоненциальная запись**
```javascript
let scientific = 5e3; // 5000
```
4. **Бесконечные значения** (`Infinity`, `-Infinity`)
```javascript
console.log(1 / 0); // Infinity
```
5. **Не-числовые значения (`NaN`)**
```javascript
console.log("abc" * 3); // NaN (Not a Number)
```

### 🔹 Методы работы с числами
```javascript
let num = 123.456;
console.log(num.toFixed(2)); // "123.46" (округление до 2 знаков после запятой)
console.log(num.toPrecision(4)); // "123.5" (общее число значащих цифр)
console.log(Number.isInteger(num)); // false
console.log(Number.parseInt("42px")); // 42
console.log(Number.parseFloat("3.14test")); // 3.14
```

### 🔹 Математические операции
JavaScript поддерживает базовые арифметические операции и работу с библиотекой `Math`:
```javascript
console.log(Math.round(4.6)); // 5 (округление)
console.log(Math.ceil(4.2)); // 5 (округление вверх)
console.log(Math.floor(4.9)); // 4 (округление вниз)
console.log(Math.random()); // Случайное число от 0 до 1
console.log(Math.pow(2, 3)); // 8 (2^3)
console.log(Math.sqrt(25)); // 5 (квадратный корень)
```

---

## 🎯 Type Conversion (Преобразование типов)

### 🔹 Преобразование строки в число
```javascript
let str = "123";
console.log(Number(str)); // 123
console.log(parseInt(str, 10)); // 123
console.log(parseFloat("3.14")); // 3.14
```

### 🔹 Преобразование числа в строку
```javascript
let numValue = 456;
console.log(String(numValue)); // "456"
console.log(numValue.toString()); // "456"
```

### 🔹 Автоматическое преобразование типов
JavaScript часто автоматически преобразует типы данных в зависимости от контекста:
```javascript
console.log("5" + 3); // "53" (конкатенация строк)
console.log("5" - 3); // 2 (преобразование строки в число)
console.log(5 * "2"); // 10 (преобразование строки в число)
```

---

## 🚀 Summary (Итоги)
- **Строки (String)** используются для работы с текстом и обладают множеством методов, таких как `.toUpperCase()`, `.split()`, `.replace()` и др.
- **Числа (Number)** поддерживают математические операции и методы, такие как `.toFixed()`, `Math.round()`, `parseInt()` и др.
- **Преобразование типов** позволяет легко конвертировать строки в числа и наоборот с помощью `Number()`, `String()`, `parseInt()`, `parseFloat()`.
- **JavaScript выполняет автоматическое преобразование типов**, что может приводить к неожиданным результатам.

---

