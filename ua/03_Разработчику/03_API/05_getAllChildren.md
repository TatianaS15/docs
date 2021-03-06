###Повертає інформацію про всі дочірні документи, включаючи також неопубліковані та видалені

*Примітка: getAllChildren() повертає інформацію про дочірні документи тільки першого рівня.*

array getAllChildren(mixed $id[, string $sort[, string $dir[, string $fields]]]);

**$id** - індентифікатор батьківського документа

**$sort** - поле, по якому буде здійснюватись сортування
- за замовчуванням: menuindex

**$dir** - варіант сортування:
- ASC - за зростанням, DESC - за спаданням
- за змовчуванням: ASC

**$fields** - список необхідних полів
за змовчуванням: id, pagetitle, description, parent, alias, menutitle

***

####Формат даних результату:
````php
Array (
    [0] => Array (
        [id] => 50
        [pagetitle] => Документ 1
        [description] =>
        [parent] => 16
        [alias] =>
        [menutitle] =>
    )
    [1] => Array (
        [id] => 48
        [pagetitle] => Документ 2
        [description] =>
        [parent] => 16
        [alias] =>
        [menutitle] =>
    )
)
````

***

####Приклад

````php
/**Структура документів:

-Статті (1)
--Нерухомість (11)
---Економ(111)
---Елітна(112)
--Авто (12)

**/

$modx->getActiveChildren(1); //поверне інформацію про документи 11 и 12

````

*Дивіться також: getActiveChildren*