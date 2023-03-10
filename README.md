## Event Phases (difference between them). Event propagination cycle

### 3 фази подій в JavaScript

- Фаза перехоплення. Перехоплення події - це передача події від документа до
  активованого елемента.
- Цільова фаза (спрацьовує двічі; як у фазі захоплення, так і у фазі спливання;
  подія досягає цільового елемента).
- Фаза спливання. Спливання подій — це поширення події від активованого елемента
  догори до документа.

## Carrying and partial functions (difference between them)

Carrying — це коли ми трансформуємо функцію, яка приймає декілька аргументів, на
ряд функцій, кожна з яких приймає один аргумент. Наприклад:
`function add (a, b) { return a + b; }` трансформує в
`function add (a) { return function (b) { return a + b; } }`

Partial - це функція, яка повертає іншу функцію, яка може повертати іншу
функцію, але кожна функція, яка була повернута, може приймати декілька
аргументів.

Відмінність: carrying приймає тільки один аргумент, на відміну від partial, яка
може приймати більше одного.

В чому схожі: обидві функції не співпадають з початковими, це нові функції, які
приймають менше параметрів.

## How to catch async errors events

В асинхронних функціях ми можемо відловити помилки за допомогою `try..catch`.
Наприклад: `try { function(); } catch (error) { console.error(error); }`. Якщо у
нас немає `try..catch`, тоді згенерований викликом асинхронної функції `f()`
проміс, завершиться з помилкою. Ми можемо додати .catch для її обробки.
