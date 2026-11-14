# MobiCar data

[↩ Project](../README.md) · [Русский](README.ru.md)

`funnel-daily.csv` and `funnel-data.xlsx` contain identical data: 56 days from 6 January to 2 March 2025 and eight columns.

The table was restored from the supplied Python block `data = {...}`. The original Excel file was not available. All 48 weekly averages of daily conversion rates match the saved output of the original notebook to six decimal places.

The supplied numbers and dates were preserved. Checks found no missing values, duplicate dates or violations of the order of funnel stages.

| Original column | Meaning |
| :--- | :--- |
| `Дата` | Observation date |
| `Неделя` | Week 1-8 |
| `Установки` | App installations |
| `Регистрации` | Registrations |
| `Открыли поиск` | Users who opened car search |
| `Просмотрели авто` | Users who viewed a car |
| `Забронировали` | Users who booked a car |
| `Первая поездка` | Users who completed their first ride |

The English notebook renames these columns after loading the shared source data. Installation growth, retention, search changes and reviews are context supplied in the [case brief](../materials/task.en.md).
