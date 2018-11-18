# Необходимо больше CSS-селекторов


**Normalize.css/reset.css**

Различные браузеры могут добавлять разные свойства к html-элементам (например margin'ы и padding'и) у списков. Для того, чтобы сбросить все такие дополнения у браузеров к проекту подключают файл [reset.css](http://meyerweb.com/eric/tools/css/reset/)

Более поздняя версия для HTML5 [normalize.css](https://necolas.github.io/normalize.css/)

**Селектор * **

Данный селектор воздействует на все теги в документе

```css
* {
padding:0px;
margin:0px;
}
```

Конечно такой глобальный охват не всегда удобен, поэтому чаще всего данный селектор применяется в каком-то контексте.

```css
.block * {
  border-width:0px ;
}
```
то есть все теги внутри класса block будут без границ.

**:not()**

Применяет оформление ко всем тегам, кроме заданного

https://developer.mozilla.org/en/docs/Web/CSS/:not

https://css-tricks.com/almanac/selectors/n/not/

**Селекторы атрибутов**

https://habrahabr.ru/post/85920/


```css
[src] {
    border:10px solid grey;
}
```

**nth-of-type**

```html
<style> 
div:nth-of-type(2) {
    background: #ff0000;
}
</style>

<h1>Это заголовок</h1>
<div>The first paragraph.</div>
<div>Это второй параграф, к которому применится оформление</div>
<div>The third paragraph.</div>
<div>The fourth paragraph.</div>
```

_nth-child_ похож на nth-of-type, но применяется просто к элементу-ребенку с заданным номером, если его тип совпал с заданным.

То есть p:nth-child(2) применится ко второму ребенку в body, если он оказался параграфом.

https://www.w3schools.com/cssref/sel_nth-child.asp

odd, even, формула an+b

_Примеры:_

https://css-tricks.com/useful-nth-child-recipies/
	
**last-child
first-child**

```css
li:nth-last-child(2) {
    color: green;
}
```

**::selection**

```css
.block::selection {
    color:red;
    background-color:yellow;
}
```

**user-select**

Убираем выделение для текста внутри блока
```css
.block {
    user-select: none;
}
```
**cursor**

```css
.block {
    cursor: pointer;
    cursor: hand;
}
```

**Дополнительные ссылки**

1.
https://medium.com/@adamemdouglas/advanced-css-selectors-you-really-may-not-have-heard-of-and-if-you-have-you-probably-haven-t-a888515e8f2#.p4fh8fndb

2.
http://bitsofco.de/on-not-and-specificity/


**Практика:**

1. Создаем чередующие окрашенные строки (два цвета)
2. Создаем чередующие окрашенные строки (три цвета)
3. Создаем шахматную доску 5*5
4. Двухцветный список, через каждые пять элементов появляется отступ
5. Задаем разное оформление для внутренних и внешних ссылок
6. Все jpeg'и оборачиваем в зеленую каемочку, а gif'ы в красную
7. Делаем буквицу – в первом абзаце страницы, выделяем первую букву