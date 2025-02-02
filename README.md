# editDocs 
PHP >= 7.2 <br>
Evolution CMS 1.4, 2.0, 3.0<br>
<br>
Модуль для Evolution CMS. Для работы необходим DocLister. В работе модуля используется библиотека phpSpreadSheet https://github.com/PHPOffice/phpspreadsheet/
<br/><br/>
<b>модуль доступен для установки из extras</b> <br/>

Документация с примерами https://editdocs.grishin.net/

Модуль умеет:<br/>

- Редактировать основные поля и TV группы документов разной вложенности, а также изменять ID категорий для плагина <a href="https://github.com/Pathologic/MultiCategories">MultiCategories</a><br/>
- Импортировать/обновлять таблицы из Excel или Calc и CSV и производить сравнение по выбранному полю( или ТВ). Также можно включить интеграцию с таблицей значений для категорий плагина <a href="https://github.com/Pathologic/MultiCategories">MultiCategories</a><br/>
- Экспортировать в XLSX и CSV с выбранным уровнем вложенности.<br/>
- Массово переносить документы от одного родителя к другому.

Видео-урок по использованию модуля
https://youtu.be/6c_Tg9eGc2g

<b>ВАЖНО!</b>
- При импорте обязательно должен быть столбец со стандартным полем <b>pagetitle</b>!
- Список полей и ТВ можно регулировать в настройках модуля.
- Внимательно проверяйте названия полей или TV-параметров при импорте.
- при импорте сразу в несколько родительских документов указываем для каждого документа поле <b>parent</b>, тогда основной родитель при импорте можно ставить любой, отличный от 0. Он роли играть не будет.
- для EVO 3 нужно будет установить ModxAPI для evo 3 через composer, будет сообщение при запуске модуля.

11.12.2022<br>
<b>Обновление до версии 2.0</b> <br>
- добавлены конфиги
- переработан интерфейс
- исправлены мелкие баги

03.12.2022<br>
<b>Обновление до версии 1.4.0</b> <br>
- добавлен импорт MultiTV
- исправлен рендер ТВ для значений 1||2||3

29.08.2022<br>
<b>Обновление до версии 1.3.14</b> <br>
- добавлен английский язык для Evo 3 <br>

18.08.2022<br>
<b>Обновление до версии 1.3.13</b> <br>
- Добавлена возможность снимать с публикации документы с выбранными шаблонами перед импортом. В таком случае все найденные совпадения будут принудительно публиковаться. Функция востребована в случае если надо публиковать, например, только все товары которые есть на складе.

28.07.2022<br>
<b>Обновление до версии 1.3.11</b> <br>
<b>рекомендуется удалить модуль и установить заново!</b><br>
- добавлена опция в настройках модуля для сопоставления полей из базы и из экселя по умолчанию<br>
- добавлена опция в настройках модуля вывода количества строк в браузер загружаемой таблицы.
- добавлены поиск и замена по выбираемому параметру при импорте.

23.07.2022<br>
<b>Обновление до версии 1.3.10</b><br>
- добавлены MultiCategories при экспорте<br>

22.06.2022<br>
<b>Обновление до версии 1.3.9</b><br>
- исправление ошибок с рендером ТВ-полей<br>

03.05.2022<br>
<b>Обновление до версии 1.3.7</b><br>
- Исправлена проблема с заполнением пустых TB через пробел
- добавлена опция "выбрать все" при редактировании и экспорте.

23.03.2020<br>
<b>Обновление до версии 1.3.5</b><br>
- При редактировании добавлен рендеринг ТВ-полей (dropdown,radio,checkbox,select,multiselect)
- При импорте добавлено поле соответствия для XLS-таблицы
- При экспорте устранена ошибка memory limit если в БД большое количество документов для экспорта.

15.11.2021<br>
<b>Обновление до версии 1.2.3</b><br>
фикс работы экспорта<br>

08.11.2021<br>
<b>Обновление до версии 1.2.2</b><br>
фикс для сайтов вида site.ru/site/<br>

04.11.2021<br>
<b>Обновление до версии 1.2.1</b><br>
добавлен экспорт в формате .xlsx<br>
файл экспорта скачивается по ссылке (нет бага в сафари)<br>
добавлена кнопка очистки кэша во вкладке экспорта (при очистке кэша удаляются все файлы из папки upload)<br>

06.08.2021<br>
<b>Обновление до версии 1.1.4</b><br>
багфикс нули в pagetitle

27.07.2021<br>
<b>Обновление до версии 1.1.3</b><br>
импорт/апдейт значений равных нулю или пустому значению.

13.07.2021<br>
<b>Обновление до версии 1.1.2</b><br>
добавление prepare функции для изменения полей по которым идет сравнение.

11.05.2021<br>
<b>Обновление до версии 1.1.1</b><br>
Мелкие исправления

15.04.2021<br>
<b>Обновление до версии 1.1.0</b><br>
Скорость импорта увеличена в десятки раз!


08.04.2021<br/>
<b>Обновление до версии 1.0</b><br>
- переезд на библиотеку PHPSpreadSheet (PHP >= 7.2) тем кто на древних сайтах обновляться не надо.<br/>
- ИМПОРТ - обработка CSV средствами библиотеки (кодировка файла должна быть UTF-8 или windows-1251)<br/>
- РЕДАКТИРОВАНИЕ - добавлена сортировка по любому полю или ТВ.<br/>
- ИМПОРТ - убраны лишние столбцы в таблице template и category если эти параметры не были задействованы пользователем.<br/>
- исправлены некоторые ошибки при импорте (добавлены новые :D)<br/>
- автоматическое создание таблицы в БД для плагина MultiCategories если человек только что установил плагин но еще не добавил вручную доп. категорию для товара и таблица не была при этом создана.
- в футер добавлена форма для доната ^_^ <br/>

28.02.2021<br/>
<b>Обновление до версии 0.4.9</b><br/>
Добавлена совместимость с Evo 3

08.12.2020<br/>
<b>Обновление до версии 0.4.8</b><br/>
Фикс мультиКатегории для EVO 2

30.05.2020<br/>
<b>Обновление до версии 0.4.7</b><br/>
- Добавлена следующая возможность, в сниппет prepare передается переменная для отслеживания тестового режима. Удобно если вы импортируете/обновляете прайс где нужно на лету создавать категории/разделы. Вот чтобы в тестовом режиме они не создавались можно проверять в каком режиме идет обработка.
В сниппете editDocsPrepare который ставится по умолчанию сверху строчка будет висеть напоминание.

25.05.2020<br/>
<b>Обновление до версии 0.4.6</b><br/>
- официально добавлена работа prepare сниппета, который позволяет менять данные при импорте на лету.
- переработан вывод логов при импорте.

26.04.2020<br/>
<b>Обновление до версии 0.4.5</b><br/>
- добавлено отображение картинок при редактировании полей

23.03.2020<br/>
<b>Обновление до версии 0.4.4</b><br/>
- добавлено сравнение по id при импорте(обновлении)
- добавлено пояснение что id всегда включен при экспорте.

01.12.2019<br/>
<b>Обновление до версии 0.4.3</b><br/>
При работе с мультикатегориями можно указывать несколько категорий, а не только одну (через запятую).

10.11.2019<br/>
<b>Обновление до версии 0.4.2</b>
- Добавлены фильтры DocLister для TV и основных полей документов при экспорте.

08.09.2019<br/>
<b>Обновление до версии 0.4.1</b>
- При импорте добавлен чекбокс отменяющий действие добавления документа если нет совпадений в базе. (Используется, если например, нужно только обновить документы которые совпали)
- При импорте поле ID родителя теперь не обязательно для заполнения.
- При импорте добавлен поиск поля для совпадения.

13.08.2019<br/>
<b>Обновление до версии 0.4.0</b>
- Интегрированы улучшения из форка от Webber. Импорт теперь может быть с любым количеством строк в файле таблицы. 
- Добавлена интеграция с плагином  <a href="https://github.com/Pathologic/MultiCategories">MultiCategories</a>, можно редактировать соответствубщий параметр вместе с основными полями или ТВ. Также можно добавлять данный параметр для плагина при импорте.
- добавлен выбор разделителя при экспорте в CSV.
- объеденены разделы импорт и апдейт в один раздел. Если документа нет, то он добавится, если найдено совпадение (по выбранному параметру) то значения обновятся.

10.08.2018<br/>
<b>Обновление до версии 0.3.7</b>
- добавлен массовый перенос документов (в новой вкладке).

26.01.2018<br/>
<b>Обновление до версии 0.3.6</b>
- добавлена фильтрация по ТВ параметрам и основным по полям (по правилам компонента DocLister) при редактировании.
- сообщения о редактировании теперь всегда сверху.
- исправлены мелкие баги
- отредактированы CSS под стиль админки.


09.05.2017<br/>
<b>Обновлено до версии 0.3</b>
- рефакторинг кода
- добавлен флаг переключения обработки неопубликованных и помеченных на удаление документов при редактировании и экспорте.
- исправление ошибок

15.04.2017<br/>
<b>Обновлено до версии 0.2</b>
- добавлен экспорт в CSV
- добавлена возможность сравнения на наличие в базе по выбранному полю TV при апдейте
- мелкие исправления

12.03.2017
- мелкие правки
- удаление чанка пагинации (сама пагинация осталась)

11.02.2017
- добавлен апдейт из Excel или Calc
- добавлен импорт из Excel или Calc
- мелкие фиксы

01.02.2017 
 - перевод модуля на ООП.
 - добавлена опционально ajax-пагинация.

<br/><br/>



<b>Если Вам понравился модуль и он облегчил Вам жизнь, то я с радостью приму донаты :)</b>

Яндекс кошелек<br/>
41001460027073<br/>

Webmoney<br/>
Z350511691467

