# Практикум «Младший разработчик: первая неделя»

**МДК.01.01 · Go · подписи функций и модуль проекта**

Практическая работа по основам модулей Go, организации проекта и чтению сигнатур функций. Задания охватывают настройку `go.mod`, зависимости, структуру пакетов, правила первого коммита, типы параметров и результатов функций.

## Что изучено

- Создание Go-модуля командой `go mod init` и управление зависимостями через `go mod tidy`.
- Запуск всего пакета командой `go run .`.
- Размещение исходного кода, тестов, `go.mod`, `go.sum` и `.gitignore` в репозитории; исключение локальных секретов и собранных исполняемых файлов.
- Экспорт идентификаторов из пакета и единое имя пакета для файлов одной папки.
- Сигнатуры функций: простые типы, срезы, карты, несколько результатов, `error` и `time.Time`.

## Исправленные сигнатуры

```go
func AverageGrade(grades []int) float64
func CountAbsences(marks []string) int
func OrderTotal(items map[string]int, discount int) int
func FindGuestPhone(name string, guests map[string]string) (string, bool)
func IsMembershipActive(endDate time.Time, today time.Time) bool
func ParseQuantity(text string) (int, error)
func DistanceBounds(distances []float64) (float64, float64)
func PrintReceipt(lines []string, width int)
func AverageByStudent(journal map[string][]int) map[string]float64
func ExportCatalog(path string, titles []string) (int, error)
```

Для `time.Time` требуется импорт:

```go
import "time"
```

## Результат

По итогам практикума получено **9 из 10 баллов («отлично»)**. Все задания по строкам и ручному составлению сигнатур выполнены верно. В заявках 1 и 2 исправлены типы результатов: средний балл возвращается как `float64`, а число пропусков — как `int`.

Подробный отчёт с ответами и рецензией находится в файле [`podpisi_go_Зотов_Владислав.md`](podpisi_go_Зотов_Владислав.md).

## Материалы практикума

[Описание задания](https://algorthimization-course-vvodnoe.vercel.app/mdk0101-razrabotka-modulei/lessons/05-praktikum-podpisi/go/index.html)
