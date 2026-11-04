# JoomGallery Extensions

🇬🇧 English | 🇷🇺 Русский

---

## 🇬🇧 English

A collection of extensions for [JoomGallery](https://www.joomgallery.net/) 4.x (Joomla 5/6).

### Available extensions

| Type | Name | Description |
|------|------|-------------|
| Module | **mod_joomgallery_stats** | Gallery statistics module |
| Module | **mod_joomgallery_img_grid** | Modern image grid (analog of JoomImages) |
| Plugin | **jg_post_scheduler** | Scheduled publication for images |
| Plugin | **plg_joomgallery_navigationprevnext** | Convenient navigation and mini-gallery for detailed view |
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
</details>

### Installation

1. Download the desired ZIP file
2. In Joomla admin: **System → Extensions Panel → Install**
3. Upload and install

### Documentation

Detailed documentation for each extension is available in separate `README.md` files inside subfolders (coming soon).

### License

GNU General Public License v3.0 or later

### Author

[vodkomotornik](https://github.com/vodkomotornik)

---

## 🇷🇺 Русский

Коллекция расширений для [JoomGallery](https://www.joomgallery.net/) 4.x (Joomla 5/6).

### Доступные расширения

| Тип | Название | Описание |
|-----|----------|----------|
| Модуль | **mod_joomgallery_stats** | Модуль статистики галереи |
| Модуль | **mod_joomgallery_img_grid** | Модуль image grid вывод превью (аналог JoomImages) |
| Плагин | **jg_post_scheduler** | Отложенная публикация изображений |
| Плагин | **plg_joomgallery_navigationprevnext** | Удобная навигация и мини-галерея для детального просмотра |

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
</details>

### Установка

1. Скачайте нужный ZIP-файл
2. В админке Joomla: **Система → Панель расширений → Установить**
3. Загрузите и установите

### Документация

Подробная документация для каждого расширения будет в отдельных файлах `README.md` внутри соответствующих папок.

### Лицензия

GNU General Public License v3.0 или новее

### Автор

[vodkomotornik](https://github.com/vodkomotornik)
