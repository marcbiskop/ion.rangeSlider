# Ion Range Slider 1.0
Удобный легкий слайдер диапазонов <a href="http://ionden.com/a/plugins/ion.rangeSlider/">Страница проекта</a>

***

## Описание
ion.rangeSlider — красивый, удобный и легко настраиваемый слайдер диапазонов, поддерживающий скины. Слайдер поддерживает события, имеет гибкие настройки, может быть полностью видоизменен через CSS.
Слайдер свободно распространяется на условиях <a href="http://ionden.com/a/licence.html" target="_blank">лицензии MIT</a>.

## Зависимости
* <a href="http://jquery.com/" target="_blank">jQuery 1.9+</a>


## Подключение

Подключаем библиотеки:
* jQuery
* ion.rangeSlider.min.js

И CSS:
* normalize.min.css - желательно, если он у вас еще не подключен
* ion.rangeSlider.css

Не забываем про скин:
* sprite-skin-simple.png - простецкий скин
* sprite-skin-other.png - еще какой-то скин
* Либо воспользуйтесь вложенным в архив PSD файлом, и нарисуйте собственный скин (не забудьте модифицировать размеры элементов в CSS файле)

Создаем базовое поле инпут:
```html
<input type="range" id="someID" name="rangeName" value="10;100" />
```

Инициализируем календарь:
```javascript
$("#someID").ionRangeSlider();
```

Или инициализируем календарь с параметрами:
```javascript
$("#someID").ionRangeSlider({
    min: 10,                        // минимальное значение
    max: 100,                       // максимальное значение
    from: 30,                       // предустановленное значение ОТ
    to: 80,                         // предустановленное значение ДО
    type: "single",                 // тип слайдера
    step: 10,                       // шаг слайдера
    postfix: " грамм",              // постфикс значение
    onChange: function(obj){        // callback функция, вызывается при изменении состояния
        console.log(obj);
    },
});
```


## Настройка

<table>
    <thead>
        <tr>
            <th>Атрибут</th>
            <th>По умолчанию</th>
            <th>Описание</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>type</td>
            <td>"single"</td>
            <td>Не обязательный параметр, позволяет выбрать тип слайдера, может принимать значение <code>single</code> - для одиночного слайдера или <code>double</code> - для двойного слайдера</td>
        </tr>
        <tr>
            <td>min</td>
            <td>10</td>
            <td>Не обязательный параметр, автоматически устанавливается из атрибута <code>value</code> базового поля input. Например если value="10;100", то примет значение 10</td>
        </tr>
        <tr>
            <td>max</td>
            <td>100</td>
            <td>Не обязательный параметр, автоматически устанавливается из атрибута <code>value</code> базового поля input. Например если value="10;100", то примет значение 100</td>
        </tr>
        <tr>
            <td>from</td>
            <td>= min</td>
            <td>Не обязательный параметр, по умолчанию равен значению min. Позволяет задать стартовую позицию слайдера "ОТ"</td>
        </tr>
        <tr>
            <td>to</td>
            <td>= max</td>
            <td>Не обязательный параметр, по умолчанию равен значению max. Позволяет задать стартовую позицию слайдера "ДО"</td>
        </tr>
        <tr>
            <td>step</td>
            <td>1</td>
            <td>Не обязательный параметр, задает шаг слайдера</td>
        </tr>
        <tr>
            <td>onChange</td>
            <td>-</td>
            <td>Callback функция, вызывается при смене состояния слайдера, возвращает объект, содержащий параметры слайдера</td>
        </tr>
    </tbody>
</table>