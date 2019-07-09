---
nav: tocru
---

# Ассоциативные массивы

Здесь описаны операторы и функции для работы с ассоциативными массивами **map**. Запись **map.typename** означает, что вы можете указать любой тип, но в случае бинарного оператора, этот тип должен быть одинаковым у обоих массивов.

## Операторы

| Оператор | Результат | Описание |
| :--- | :--- | :--- |
| **\*** map.typename | int | Возвращает количество элементов в массиве. |
| map.typename **=** map.typename | map.typename | Присваивание. |
| map.typename **&=** map.typename | map.typename | Создать клон ассоциативного массива. Новая переменная будет работать с тем же набором данных. |
| map.typename **\[** str **\]** | typename | Присвоить/получить значение ассоциативного массива по ключу. |
