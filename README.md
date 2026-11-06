# JoomGallery Extensions

🇬🇧 English | 🇷🇺 Русский

---

## 🇬🇧 English

A collection of extensions for [JoomGallery](https://www.joomgallery.net/) 4.x (Joomla 5/6).

### Available extensions

| Type | Name | Description |
|------|------|-------------|
| Package | **JoomGallery Stats** | Module, component, and plugin for gallery statistics and analytics |
| Module | **mod_joomgallery_img_grid** | Modern image grid (analog of JoomImages) |
| Plugin | **plg_task_joomgallery_postscheduler** | Scheduled image publication via Joomla Task Scheduler |
| Plugin | **plg_joomgallery_navigationprevnext** | Convenient navigation and mini-gallery for detailed view |

<details>
<summary><b>More about JoomGallery Stats package (click to expand)</b></summary>

**JoomGallery Stats** is a package of three extensions for JoomGallery 4.x and Joomla 5/6. Unzip the archive and install what you need:
* **Module only:** If you just need general statistics on the frontend.
* **Module + Component + Plugin:** For detailed view analytics per image in the admin panel.

**1. Module (`mod_joomgallery_stats`)**
* **What it does:** Displays general gallery statistics on the site (images, categories, views, comments, votes, tags). Supports JComments. 
* **Modes:** Direct DB queries (works standalone) or reading from a small cache table (for high loads and large galleries, updated via Cron). The cache mode requires the component and plugin.

**2. Component (`com_joomgallery_stats`)**
* **What it does:** Adds a "JoomGallery - Analytics" item to the admin panel. Shows a table of views per image for a selected period with clickable IDs for quick editing.
* **Setup:** Go to "Components → JoomGallery Analytics". Use date filters and sort by columns.

**3. Plugin (`plg_system_joomgallery_stats`)**
* **What it does:** Collects views and votes per image into the `#__joomgallery_stats` table. This data is displayed in the component.
* **Setup:** Enable it in "System → Plugins → System - JoomGallery Stats" and configure the schedule via the Joomla Task Scheduler.

Includes standard Joomla update notifications.

**Links:**
* [Download & Documentation](https://vodkomotornik.ru/runduk/download/12-poleznoe/992-mod-joomgallery-stats.html)

</details>

<details>
<summary><b>More about JoomGallery Image Grid module (click to expand)</b></summary>

**JoomGallery Image Grid** – a modern, lightweight module for displaying an image grid from JoomGallery 4.x on Joomla 5/6. Analog of JoomImages.

**Features:**
* Fully compatible with Joomla 5/6 and JoomGallery 4.3+
* Uses native Bootstrap 5 grid (no extra scripts and CSS)
* Responsive output: 1 to 6 columns, auto-wrap
* Flexible settings: category selection, image limit, sorting (date, ID, views, rating, random)
* Info display: title, category, views, date, rating (hidden when 0 votes)
* SEF-links support for image pages
* Visual category tree in settings
* Caching enabled by default
* Multilingual: ru-RU / en-GB / de-DE
* Update notification in Joomla panel
* License: free distribution, non-commercial use.

**Perfect for:** displaying latest photos, galleries in custom positions, portfolio with category filtering.

**Performance:** No extra JS/CSS loaded, uses Joomla caching and optimized SQL queries. *(+4 unique queries and ±0ms time within margin of error!)*

**Links:**
* [Download & Documentation](https://vodkomotornik.ru/runduk/download/12-poleznoe/65-joomgallery-image-grid-modul-joomla.html)

</details>

<details>
<summary><b>More about JoomGallery Post Scheduler plugin (click to expand)</b></summary>

An extension for automatically changing the status of JoomGallery images from **Unpublished** to **Published** at a specified date and time. Uses the built-in Joomla 5/6 Task Scheduler (`com_scheduler`), requires no third-party services, and works at the system core level.

**Key Features:**
* **Auto-publish:** Changes image status to Published when the date in the "Date" field arrives.
* **Native integration:** Works with Joomla Task Scheduler (supports Web Cron and CLI).
* **Configurable limits:** Set how many images to publish per task run.
* **Filtering:** Excludes images waiting for publication longer than a specified number of days.
* **Hidden images ignored:** Images with `hidden = 1` are completely skipped.
* **Debug mode:** Writes detailed selection and execution logs to the system log.
* **Timezone support:** Correctly compares dates based on site settings, not database server time.
* **Modern architecture:** PSR-4, DI container, `TaskPluginTrait`, protection against SQL injections.

**How it works:**
1. Upload a photo and set status to **Unpublished**.
2. In the user panel, set a future date.
3. When the scheduled task runs, the plugin finds unpublished images with a date ≤ current site time, ignores hidden ones, and publishes them. Results are logged.

**Requirements:**
* Joomla 5.0.x – 6.x
* JoomGallery 4.x
* PHP 8.1+

**Links:**
* [Download & Documentation](https://vodkomotornik.ru/runduk/download/12-poleznoe/127-joomgallery-post-scheduler-plagin-otlozhennoj-publikatsii.html)

</details>

<details>
<summary><b>More about JoomGallery Navigation Prev/Next plugin (click to expand)</b></summary>

The plugin adds convenient navigation between images in the JoomGallery 4 detailed view.

**Features:**
* **Previous / Next** image buttons
* Mini-gallery with thumbnails (configurable quantity)
* Thumbnail size setting (from 50 to 200px)
* Counter display (current position / total)
* Show/hide image titles
* Support for anchors `#image-title` for smooth navigation
* Option to display arrows in the mini-gallery
* DEBUG mode for troubleshooting
* Full compatibility with Joomla 5/6 and JoomGallery 4.x
* Update notification

**Requirements:**
You need to create a template override — copy the file from the archive folder `/plugins/joomgallery/navigationprevnext/template-override/default.php` to your template here: `/templates/YOUR_TEMPLATE/html/com_joomgallery/image/default.php`

**Links:**
* [Download & Documentation](https://vodkomotornik.ru/runduk/download/12-poleznoe/87-joomla-joomgallery-navigation-prev-next.html)

</details>

### Installation

1. Download the desired ZIP file
2. In Joomla admin: **System → Extensions Panel → Install**
3. Upload and install

### Documentation

Detailed documentation for each extension is available in separate `README.md` files inside subfolders (coming soon).

### License

GNU General Public License v3.0 or later

---

## 🇷🇺 Русский

Коллекция расширений для [JoomGallery](https://www.joomgallery.net/) 4.x (Joomla 5/6).

### Доступные расширения

| Тип | Название | Описание |
|-----|----------|----------|
| Пакет | **JoomGallery Stats** | Модуль, компонент и плагин для статистики и аналитики галереи |
| Модуль | **mod_joomgallery_img_grid** | Модуль image grid вывод превью (аналог JoomImages) |
| Плагин | **plg_task_joomgallery_postscheduler** | Отложенная публикация фото через планировщик Joomla |
| Плагин | **plg_joomgallery_navigationprevnext** | Удобная навигация и мини-галерея для детального просмотра |

<details>
<summary><b>Подробнее о пакете JoomGallery Stats (нажмите, чтобы развернуть)</b></summary>

**JoomGallery Stats** — пакет из трёх расширений для JoomGallery 4.x и Joomla 5/6. Распакуйте ZIP-архив и установите нужное:
* **Только модуль:** Если нужна только статистика на сайте.
* **Модуль + компонент + плагин:** Для статистики просмотров в админке за период по каждому фото.

**1. Модуль (`mod_joomgallery_stats`)**
* **Что делает:** Выводит на сайте общую статистику галереи (изображения, категории, просмотры, комментарии, голоса, теги). Поддерживает JComments.
* **Режимы:** Прямые запросы к БД (работает сам) или чтение из кэш-таблицы (для высоких нагрузок, обновление через Cron). Для режима кэша нужен компонент и плагин.

**2. Компонент (`com_joomgallery_stats`)**
* **Что делает:** Добавляет в админку пункт «JoomGallery - Аналитика». Показывает таблицу просмотров по каждому фото за выбранный период с кликабельными ID для быстрого перехода к редактированию.
* **Настройка:** Откройте «Компоненты → Аналитика JoomGallery». Используйте фильтры по датам и сортировку по столбцам.

**3. Плагин (`plg_system_joomgallery_stats`)**
* **Что делает:** Собирает просмотры и голоса по каждому изображению в таблицу `#__joomgallery_stats`. Эти данные показываются в компоненте.
* **Настройка:** Включите в «Система → Плагины → Система — JoomGallery Stats» и настройте расписание сбора через планировщик Joomla.

Включено информирование о новых версиях через стандартный механизм обновлений Joomla.

**Полезные ссылки:**
* [Скачать и документация](https://vodkomotornik.ru/runduk/download/12-poleznoe/992-mod-joomgallery-stats.html)

</details>

<details>
<summary><b>Подробнее о модуле JoomGallery Image Grid (нажмите, чтобы развернуть)</b></summary>

**JoomGallery Image Grid** – современный, лёгкий модуль для отображения сетки изображений из JoomGallery 4.x на Joomla 5/6. Аналог JoomImages.

**Особенности:**
* Полностью совместим с Joomla 5/6 и JoomGallery 4.3+
* Использует нативную сетку Bootstrap 5 (без лишних скриптов и CSS)
* Адаптивный вывод: от 1 до 6 колонок, авто-перенос строк
* Гибкие настройки: выбор категорий, лимит изображений, сортировка (дата, ID, просмотры, рейтинг, случайно)
* Отображение информации: заголовок, категория, просмотры, дата, рейтинг (скрывается при 0 голосов)
* Поддержка SEF-ссылок на страницы изображений
* Визуальное дерево категорий в настройках (удобный выбор вложенных разделов)
* Кэширование включено по умолчанию
* Мультиязычность: ru-RU / en-GB / de-DE
* Уведомление о выходе новой версии в панели Joomla
* Лицензия: свободное распространение, некоммерческое использование.

**Идеально подходит для:** вывода последних фото, галерей в нужной позиции, портфолио с фильтрацией по категориям.

**Производительность:** Модуль не загружает дополнительные JS/CSS, использует кэширование Joomla и оптимизированные SQL-запросы. *(+4 уникальных запроса и ±0ms времени на уровне погрешности!)*

**Полезные ссылки:**
* [Скачать и документация](https://vodkomotornik.ru/runduk/download/12-poleznoe/65-joomgallery-image-grid-modul-joomla.html)

</details>

<details>
<summary><b>Подробнее о плагине JoomGallery Post Scheduler (нажмите, чтобы развернуть)</b></summary>

Расширение для автоматической смены статуса изображений JoomGallery с «Не опубликовано» на «Опубликовано» по заданной дате и времени. Использует встроенный планировщик задач Joomla 5/6 (`com_scheduler`), не требует сторонних сервисов и работает на уровне ядра системы.

**Основные возможности:**
* **Автопубликация:** Смена статуса при наступлении даты, указанной в поле «Дата».
* **Нативная интеграция:** Поддержка веб-крон и CLI-режима в планировщике Joomla.
* **Настраиваемый лимит:** Количество публикаций за одно выполнение задачи.
* **Фильтрация:** Исключение записей, ожидающих публикации дольше заданного количества дней.
* **Скрытые фото:** Изображения с `hidden = 1` полностью игнорируются.
* **Режим отладки:** Запись подробных логов в журнал администратора.
* **Часовые пояса:** Сравнение дат по настройкам сайта, а не по времени сервера БД.
* **Архитектура:** PSR-4, DI-контейнер, `TaskPluginTrait`, защита от SQL-инъекций.

**Принцип работы:**
1. Загружаете фото со статусом **«Не опубликовано»**.
2. В панели пользователя ставите будущую дату.
3. При запуске задачи плагин находит неопубликованные фото с датой ≤ текущего времени сайта, игнорирует скрытые и переводит их в статус «Опубликовано». Результат фиксируется в журнале.

**Требования:**
* Joomla 5.0.x – 6.x
* JoomGallery 4.x
* PHP 8.1+

**Полезные ссылки:**
* [Скачать и посмотреть документацию](https://vodkomotornik.ru/runduk/download/12-poleznoe/127-joomgallery-post-scheduler-plagin-otlozhennoj-publikatsii.html)

</details>

<details>
<summary><b>Подробнее о плагине навигации (нажмите, чтобы развернуть)</b></summary>

Плагин добавляет удобную навигацию между изображениями в детальном просмотре JoomGallery 4.

**Возможности:**
* Кнопки **Предыдущее / Следующее** изображение
* Мини-галерея с превью (настраиваемое количество)
* Настройка размера превью (от 50 до 200px)
* Отображение счетчика (текущая позиция / всего)
* Показывать/скрывать названия изображений
* Поддержка якорей `#image-title` для плавной навигации
* Опция отображения стрелок в мини-галерее
* DEBUG-режим для отладки
* Полная совместимость с Joomla 5/6 и JoomGallery 4.x
* Информирование о выходе новой версии

**Требования:**
Необходимо создать переопределение шаблона — скопируйте файл из папки архива `/plugins/joomgallery/navigationprevnext/template-override/default.php` в ваш шаблон сюда: `/templates/ВАШ_ШАБЛОН/html/com_joomgallery/image/default.php`

**Полезные ссылки:**
* [Скачать и посмотреть документацию](https://vodkomotornik.ru/runduk/download/12-poleznoe/87-joomla-joomgallery-navigation-prev-next.html)

</details>

### Установка

1. Скачайте нужный ZIP-файл
2. В админке Joomla: **Система → Панель расширений → Установить**
3. Загрузите и установите

### Документация

Подробная документация для каждого расширения будет в отдельных файлах `README.md` внутри соответствующих папок.

### Лицензия

GNU General Public License v3.0 или новее
