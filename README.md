# MODULE 2

## Загальна суть задачі

Тобі потрібно створити простий додаток, який дозволяє користувачу створювати картки з інформацією про людей. Кожна картка повинна містити ім'я та вік людини. Користувач заповнює форму, натискає кнопку "Додати", і нова картка з'являється на екрані.

## Структура компонентів

### 1. `App`

**Опис:** Головний компонент додатку.
**Призначення:** Містить форму для створення картки та відображає список карток.

### 2. `Form`

**Опис:** Компонент форми для створення картки.
**Призначення:** Містить поля введення для імені та віку, а також кнопку для додавання картки.
**Пропси:**

- `onAddCard` (функція) – функція, яка буде викликана при натисканні кнопки "Додати".

### 3. `CardList`

**Опис:** Компонент для відображення списку карток.
**Призначення:** Відображає всі картки, створені користувачем.
**Пропси:**

- `cards` (масив) – масив об'єктів карток для відображення.

### 4. `Card`

**Опис:** Компонент для відображення однієї картки.
**Призначення:** Відображає ім'я та вік людини.
**Пропси:**

- `name` (рядок) – ім'я людини.
- `age` (число) – вік людини.

## Компонент `App`

### Стан:

- `cards` (масив) – зберігає список карток.

### Призначення:

1. Відображає компонент `Form` для введення нових карток.
2. Відображає компонент `CardList` для відображення створених карток.

### Функції:

- `handleAddCard` (функція) – додає нову картку до списку.

## Компонент `Form`

### Стан:

- `name` (рядок) – зберігає значення поля "Ім'я".
- `age` (число) – зберігає значення поля "Вік".

### Призначення:

1. Відображає поля введення для імені та віку.
2. Відображає кнопку "Додати".

### Пропси:

- `onAddCard` (функція) – функція для додавання нової картки.

### Функції:

- `handleNameChange` (функція) – обробляє зміну значення в полі "Ім'я".
- `handleAgeChange` (функція) – обробляє зміну значення в полі "Вік".
- `handleSubmit` (функція) – обробляє натискання кнопки "Додати", викликає функцію `onAddCard` з даними нової картки.

## Компонент `CardList`

### Призначення:

1. Відображає список карток.

### Пропси:

- `cards` (масив) – масив об'єктів карток.

## Компонент `Card`

### Призначення:

1. Відображає ім'я та вік людини.

### Пропси:

- `name` (рядок) – ім'я людини.
- `age` (число) – вік людини.

## Функціональні вимоги

1. **Введення даних:** Користувач повинен мати можливість вводити ім'я та вік у форму.
2. **Додавання картки:** При натисканні кнопки "Додати" нова картка повинна з'являтися у списку карток.
3. **Валідація:** Перевірка, щоб ім'я не було порожнім, а вік був числом і більше нуля.

## Підказки

1. Використовуй `useState` для зберігання стану форми та списку карток.
2. Використовуй прослуховувачі подій для обробки змін в полях введення та натискання кнопки "Додати".
3. Використовуй функцію для додавання нової картки до стану списку карток у компоненті `App`.
