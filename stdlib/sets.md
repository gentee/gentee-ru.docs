---
nav: tocru
---

# Множества

Здесь описаны операторы и функции для работы с массивом логических значений \(тип **set**\).

* [arr\( set s \) arr.int](sets.md#arrset-s-arrint)
* [set\( arr.int a \) set](sets.md#setarrint-a-set)
* [set\( str s \) set](sets.md#setstr-s-set)
* [str\( set s \) str](sets.md#strset-s-str)
* [Set\( set s, int index \) set](sets.md#setset-s-int-index-set)
* [Toggle\( set s, int index \) bool](sets.md#toggleset-s-int-index-bool)
* [UnSet\( set s, int index \) set](sets.md#unsetset-s-int-index-set)

## Операторы

| Оператор | Результат | Описание |
| :--- | :--- | :--- |
| **\*** set | int | Возвращает размер массива. |
| **^** set | set | Возвращает новое множество, которое обратно указанному. _!s\[i\]_ для каждого элемента. |
| set **=** set | set | Оператор присваивания. |
| set **&=** set | set | Создает клон множества. Новая переменная будет работать с тем же набором данных. |
| set **+=** set | set | Добавить значение одного множества к другому. |
| set **&** set | set | Возвращает множество, которое является пересечением двух множеств. _left\[i\] && right\[i\]_ для каждого элемента. |
| set **\|** set | set | Возвращает множество, которое является объединением двух множеств. _left\[i\] \|\| right\[i\]_ для каждого элемента. |
| set **\[** int **\]** | bool | Установить/получить элемент множества. |

## Функции

### arr\(set s\) arr.int

Функция _arr_ конвертирует множество _set_ в массив целых чисел, который содержит индексы элементов множества.

### set\(str s\) set

Функция _set_ конвертирует строку в множество _set_ и возвращает его. Строка должна содержать только символы 1 и 0.

### set\(arr.int a\) set

Функция _set_ конвертирует массив целых чисел в множество _set_ и возвращает его. Результирующее множество будет иметь элементы с соответствующими индексами.

```text
run arr.int {
  set s &= {780, 99, 128, 105, 136}
  arr.int as = arr(s)
  as += 330
  s &= set(as)
  return arr(s) // [99 105 128 136 330 780]
}
```

### str\(set s\) str

Функция _str_ конвертирует множество в строку и возвращает её. Результирующая строка содержит только символы 1 и 0.

### Set\(set s, int index\) set

Функция _Set_ добавляет элемент к множеству. Эквивалентно _s\[index\] = true_. Функция возвращает _s_.

### Toggle\(set s, int index\) bool

Функция _Toggle_ добавляет элемент множеству, если его не существует, в противном случае, элемент удаляется. Эквивалентно _s\[index\] = !s\[index\]_. Функция возвращает предыдущее состояние - _true_, если элемент существовал и _false_ в противном случае.

### UnSet\(set s, int index\) set

Функция _UnSet_ удаляет элемент из множества. Эквивалентно _s\[index\] = false_. Функция возвращает _s_.
