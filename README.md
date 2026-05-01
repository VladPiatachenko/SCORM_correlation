# SCORM-тренажер: залежності між змінними

Інтерактивний SCORM 1.2 тренажер для практичної роботи з теми аналізу залежностей між змінними. Студент завантажує CSV-файл, аналізує кореляцію між числовими змінними, будує діаграму розсіювання та матрицю кореляцій, а результат може бути збережений у LMS через SCORM API.

## Структура

- `index.html` — головна сторінка тренажера, UI і вся JavaScript-логіка
- `style.css` — окремий файл стилів у репозиторії
- `imsmanifest.xml` — SCORM-маніфест
- `skulpt.min.js`, `skulpt-stdlib.js` — сторонні бібліотеки в складі пакета

## Збірка SCORM ZIP

```bash
mkdir -p dist
zip -r dist/data_correlation_scorm.zip \
  index.html \
  imsmanifest.xml \
  style.css \
  skulpt.min.js \
  skulpt-stdlib.js
```

## Примітка

`Chart.js` підключається в `index.html` через CDN, тому для повністю офлайн-роботи в LMS бібліотеку варто додати в пакет локально.
