# <p align="center">PersonGenerator 👤</p>
Generator of non-existent personalities - 2017

## Установка
Используйте клонирование репозитория для размещения библиотеки у себя в проекте:
```
git clone https://github.com/kikemaru/PersonGenerator.git
``` 
Или установите библиотеку из конечного релиза по прямой <a href="https://github.com/kikemaru/PersonGenerator/archive/refs/tags/php.zip">ссылке-></a><br>

<br>

## Использование
Создайте экземпляр класса генератора и укажите кол-во генерируемых персон<br>
Класс расположен в пространстве имен <b>generate</b>
```php
//подключение библиотеки
include_once './lib/Generate.php';
//Экземпляр класса
$foo = new \generate\Generate(n);
``` 
*Где n - количество запрашиваемых персон*<br>

<br>Используйте метод Get() для генерации персональных данных<br>
Передавайте в метод 4 параметра:<br>
(<b>пол</b>, <b>требование фамилии</b>, <b>требование имени</b>, <b>требование отчества</b>)<br>
Требование определяется с помощью: 0 - (не требовать), 1 - (требовать).<br>
Пол определяется с помощью: m - (мужской), w - (женский).
```php
//Экземпляр класса
$foo = new \generate\Generate(1);
//Использование метода Get
$result = $foo->Get('m', 1, 1, 1);
print_r($result);
``` 
По умолчанию установлены параметры ('m', 1, 1, 1). По этому обязательно указывайте <b>необходимые</b> параметры.<br>
Возвращаемый результат:
```php
//Результат
Array
(
    [0] => Array
        (
            [0] => Романов
            [1] => Протасий
            [2] => Вавилович
        )
)

``` 
<br>

<br>Используйте метод GeneratePhone() для генерации номера телефона<br>
```php
//Экземпляр класса
$foo = new \generate\Generate(3);
//Использование метода GeneratePhone
$result = $foo->GeneratePhone();
print_r($result);
``` 
Возвращаемый результат:
```php
//Результат
Array
(
    [0] => +79971749459
    [1] => +79931235862
    [2] => +79291362418
)
``` 
<br>

<br>

## Источники
Фамилии - <a href="https://ru.wikipedia.org/wiki/%D0%A1%D0%BF%D0%B8%D1%81%D0%BE%D0%BA_%D0%BE%D0%B1%D1%89%D0%B5%D1%80%D1%83%D1%81%D1%81%D0%BA%D0%B8%D1%85_%D1%84%D0%B0%D0%BC%D0%B8%D0%BB%D0%B8%D0%B9">ru.wikipedia.org/wiki/Список_общерусских_фамилий</a><br>
Имена мужские - <a href="https://ru.wikipedia.org/wiki/%D0%9A%D0%B0%D1%82%D0%B5%D0%B3%D0%BE%D1%80%D0%B8%D1%8F:%D0%A0%D1%83%D1%81%D1%81%D0%BA%D0%B8%D0%B5_%D0%BC%D1%83%D0%B6%D1%81%D0%BA%D0%B8%D0%B5_%D0%B8%D0%BC%D0%B5%D0%BD%D0%B0">ru.wikipedia.org/wiki/Категория:Русские_мужские_имена</a><br>
Имена женские - <a href="https://ru.wikipedia.org/w/index.php?title=%D0%9A%D0%B0%D1%82%D0%B5%D0%B3%D0%BE%D1%80%D0%B8%D1%8F:%D0%96%D0%B5%D0%BD%D1%81%D0%BA%D0%B8%D0%B5_%D0%B8%D0%BC%D0%B5%D0%BD%D0%B0">ru.wikipedia.org/w/index.php?title=Категория:Женские_имена</a>
