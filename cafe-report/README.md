# Cafe Report

Программа читает заказы кофейни из файла `data/orders.csv` и печатает отчёт: количество заказов, выручку, средний чек и суммы по официантам.

Внешних библиотек нет, нужен только Python 3.10 или новее.

## Структура проекта

```text
cafe-report/
├── .env
├── .gitignore
├── README.md
├── requirements.txt
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── services/
│   │   ├── __init__.py
│   │   ├── orders.py
│   │   └── report.py
│   └── utils/
│       ├── __init__.py
│       ├── money.py
│       └── text.py
├── data/
│   └── orders.csv
├── docs/
│   └── project.md
└── tests/
    ├── __init__.py
    ├── test_orders.py
    └── test_report.py
```

### Назначение папок

- `app/` — основной пакет с исходным кодом приложения.
- `app/services/` — модули бизнес-логики: расчёт агрегированных показателей и формирование итогового отчёта.
- `app/utils/` — вспомогательные утилиты для форматирования текста и работы с денежными суммами.
- `data/` — каталог с входными данными приложения (`orders.csv`).
- `docs/` — сопроводительная документация и справочные материалы по проекту.
- `tests/` — модульные тесты для проверки корректности бизнес-логики и вспомогательных функций.

---

## Запуск

Команды выполняются из корня проекта — каталога `cafe-report`.

### Создание и активация виртуального окружения (опционально)

В macOS / Linux:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

В Windows (PowerShell):
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### Запуск программы

```bash
python -m app.main
```

### Запуск тестов

```bash
python -m unittest discover -s tests -v
```

---

## Ожидаемый результат

При запуске приложения (`python -m app.main`):

```text
ОТЧЁТ ПО ЗАКАЗАМ
----------------------------------
Заказов: 6
Выручка: 3 702,00 ₽
Средний чек: 617,00 ₽
----------------------------------
Анна Петрова      770,00 ₽
Игорь Смирнов     1 793,00 ₽
Мария Ким         1 139,00 ₽
```

При запуске тестов (`python -m unittest discover -s tests -v`):

```text
test_average (test_orders.TestOrders.test_average) ... ok
test_average_empty (test_orders.TestOrders.test_average_empty) ... ok
test_by_waiter (test_orders.TestOrders.test_by_waiter) ... ok
test_total (test_orders.TestOrders.test_total) ... ok
test_format_rubles (test_report.TestHelpers.test_format_rubles) ... ok
test_normalize_name (test_report.TestHelpers.test_normalize_name) ... ok
test_pad (test_report.TestHelpers.test_pad) ... ok
test_to_rubles (test_report.TestHelpers.test_to_rubles) ... ok
test_lines (test_report.TestReport.test_lines) ... ok

----------------------------------------------------------------------
Ran 9 tests in 0.001s

OK
```