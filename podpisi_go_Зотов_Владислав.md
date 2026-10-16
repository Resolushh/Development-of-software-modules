# Практикум «Младший разработчик: первая неделя» · ветка Go

МДК.01.01 · подписи функций Go и модуль проекта

- Студент: Зотов Владислав
- Группа: РПО 9/25/3
- Сдано: 16.10.2026, 23:30:35

## Рецензия

| Письмо | Результат | Баллы |
|---|---|---|
| Письмо 1 · рабочее место | 17 из 18 | 2 / 2 |
| Письмо 2 · подписи по заявкам | 8 из 10 | 3 / 4 |
| Письмо 3 · строки и подпись | 40 из 40 | 2 / 2 |
| Письмо 4 · подпись вручную | 4 из 4 | 2 / 2 |
| **Итого** | | **9 / 10 · отлично** |

- Рабочее место: повторите что попадает в Git: go.mod, go.sum и правила .gitignore (глава 2.6, ветка Go).
- Подписи по заявкам: не решены заявки 1, 2. Повторите: срезы []тип и словари map[ключ]значение. Справка по записи — на странице описания практикума, §3.
- Строки и подпись: все строки разложены верно.
- Подпись вручную: все подписи верны.

## Письмо 1. Рабочее место

### Порядок команд — верно

1. `Распаковать архив и открыть папку проекта в VS Code: File → Open Folder, затем Terminal → New Terminal`
2. `go mod init example.com/zerno-kassa`
3. `go mod tidy`
4. `go run .`

### Первый коммит — верно 9 из 10

| Файл | Ваш ответ | Верно |
|---|---|---|
| `main.go` | в репозиторий | ✓ |
| `internal/services/calculator.go` | в репозиторий | ✓ |
| `internal/services/calculator_test.go` | в репозиторий | ✓ |
| `go.mod` | в репозиторий | ✓ |
| `README.md` | в репозиторий | ✓ |
| `.gitignore` | в репозиторий | ✓ |
| `go.sum` | в репозиторий | ✓ |
| `zerno-kassa` | в репозиторий | ✗ |
| `zerno-kassa.exe` | на компьютере | ✓ |
| `.env` | на компьютере | ✓ |

### Вопросы из чата — верно 7 из 7

| Вопрос | Ваша причина | Верно |
|---|---|---|
| 1. Денис | Терминал открыт не в папке модуля | ✓ |
| 2. Лиза | Библиотека импортирована в коде, но не записана в go.mod | ✓ |
| 3. Ксюша | Запущен один файл, а не пакет целиком | ✓ |
| 4. Глеб | Нет правил .gitignore для собранного файла и настроек | ✓ |
| 5. Марат | Имя функции начинается с маленькой буквы и не видно из другого пакета | ✓ |
| 6. Оля | В VS Code открыта папка уровнем выше, а не папка с go.mod | ✓ |
| 7. Тимур | В одной папке лежат файлы с разными именами пакета | ✓ |

## Письмо 2. Подписи по заявкам

### 1. Колледж «Северный» · электронный журнал — неверно

```go
func AverageGrade(grades []int) []float64
```

### 2. Колледж «Северный» · посещаемость — неверно

```go
func CountAbsences(marks []string) []int
```

### 3. Кофейня «Зерно» · касса — верно

```go
func OrderTotal(items map[string]int, discount int) int
```

### 4. Кофейня «Зерно» · постоянные гости — верно

```go
func FindGuestPhone(name string, guests map[string]string) (string, bool)
```

### 5. Фитнес-клуб «Пульс» · абонементы — верно

```go
func IsMembershipActive(endDate time.Time, today time.Time) bool
```

### 6. Книжный магазин «Переплёт» · склад — верно

```go
func ParseQuantity(text string) (int, error)
```

### 7. Курьерская служба «Квартал» · отчёт за день — верно

```go
func DistanceBounds(distances []float64) (float64, float64)
```

### 8. Кофейня «Зерно» · печать чека — верно

```go
func PrintReceipt(lines []string, width int)
```

### 9. Колледж «Северный» · ведомость группы — верно

```go
func AverageByStudent(journal map[string][]int) map[string]float64
```

### 10. Книжный магазин «Переплёт» · выгрузка каталога — верно

```go
func ExportCatalog(path string, titles []string) (int, error)
```

## Письмо 3. Строки и подпись

| Подпись | Верно |
|---|---|
| `func AverageGrade(grades []int) float64` | 8 из 8 |
| `func FindGuestPhone(guests map[string]string, name string) (string, bool)` | 8 из 8 |
| `func ParseQuantity(text string) (int, error)` | 8 из 8 |
| `func DistanceBounds(distances []float64) (float64, float64)` | 8 из 8 |
| `func PrintReceipt(lines []string, width int)` | 8 из 8 |

## Письмо 4. Подпись вручную

### 1. Колледж «Северный» · лучший студент — верно

```go
func BestStudent(averages map[string]float64) (string,bool)
```

### 2. Фитнес-клуб «Пульс» · бонусы — верно

```go
func AddBonus(balance int, visits int, isVIP bool) int
```

### 3. Курьерская служба «Квартал» · адреса — верно

```go
func SplitAddress(address string) (string, string)
```

### 4. Книжный магазин «Переплёт» · цены — верно

```go
func LoadPrices(path string) (map[string]int,error)
```
