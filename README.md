# template-builder

Локальное фронтенд-приложение (без бэкенда) для заполнения HTML-шаблонов и выгрузки в PDF.

## Как запустить

1. Откройте `index.html` в браузере (или поднимите простой static-server).
2. Загрузите HTML-файл с плейсхолдерами.
3. Заполните поля в предпросмотре.
4. Нажмите кнопку **«Рендер и скачать PDF»**.

## Формат плейсхолдеров в шаблоне

Любой тег с атрибутом `data-tb-field` заменяется на контрол:

```html
<span data-tb-field="fullName" data-tb-type="text" data-tb-placeholder="ФИО"></span>
<span data-tb-field="age" data-tb-type="number"></span>
<span data-tb-field="birthDate" data-tb-type="date"></span>
<span data-tb-field="city" data-tb-type="select" data-tb-options="Москва,Казань,Екатеринбург"></span>
```

### Поддерживаемые атрибуты

- `data-tb-field` — имя поля (обязательно).
- `data-tb-type` — `text | number | date | select`.
- `data-tb-options` — список значений через запятую (для `select`).
- `data-tb-placeholder` — подсказка для пустого поля.
- `data-tb-width` — минимальная ширина поля (например, `220px`).
