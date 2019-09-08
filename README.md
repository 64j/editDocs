# editDocs 
Модуль для Modx Evolution. Для работы необходим DocLister. В работе модуля используется библиотека PHPExcel https://github.com/PHPOffice/PHPExcel
<br/><br/>
<b>модуль доступен для установки из extras</b> <br/><br/>
Модуль умеет:<br/>

- Редактировать основные поля и TV группы документов разной вложенности, а также изменять ID категорий для плагина <a href="https://github.com/Pathologic/MultiCategories">MultiCategories</a><br/>
- Импортировать/обновлять таблицы из Excel или Calc и CSV и производить сравнение по выбранному полю( или ТВ). Также можно включить интеграцию с таблицей значений для категорий плагина <a href="https://github.com/Pathologic/MultiCategories">MultiCategories</a><br/>
- Экспортировать в CSV с выбранным уровнем вложенности.<br/>
- Массово переносить документы от одного родителя к другому.

Видео-урок по использованию модуля
https://youtu.be/6c_Tg9eGc2g

<b>ВАЖНО!</b>
- При импорте обязательно должен быть столбец со стандартным полем <b>pagetitle</b>!
- Список полей и ТВ можно регулировать в настройках модуля.
- Внимательно проверяйте названия полей или TV-параметров при импорте.
- при импорте сразу в несколько родительских документов указываем для каждого документа поле <b>parent</b>, тогда основной родитель при импорте можно ставить любой, отличный от 0. Он роли играть не будет.

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



<b>Если понравился модуль, можете задонатить мне на пиво :)</b>

Webmoney<br/>
R948295169787<br/>
Z350511691467

