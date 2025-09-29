# 🚀 Урок: Создание header
## 🎤 Вступление для преподавателя

Сегодня мы делаем первый настоящий шаг к нашему сайту — создаём header!
Это отличное занятие, чтобы обсудить: зачем нужна шапка сайта, какие элементы там всегда находятся, и познакомить ребят с новыми тегами (header, nav) и новыми свойствами (justify-content, align-items).

Совет: превратите это в игру «Архитекторы сайта» 🏗️. Пусть дети представят, что они строят дом, а header — это крыша и вывеска. Спросите: «Что бы вы поместили на фасад здания, чтобы сразу было понятно, кто вы и куда попали?». Так плавно подведём к структуре.

## 📖 Исходный текст (сохранён полностью)

На этом занятии мы сделаем первую часть странички, а именно header. Вспомним для чего нужна эта часть, а также вспомним несколько тегов и свойств, которые мы изучали и изучим новые (тег header и nav; свойства justify-content и align-items).
Классы использовать такие же, как и в методичке. Чтобы в дальнейшем не было проблем с назначением свойств и при переводе к другому преподавателю.

1)Открываем макет, рассуждаем по поводу header (для чего он нужен и что там располагается)
2)Переходим в Sublime Text, а именно в index.html и после комментария добавляем тег header и сразу задаём ему класс header (так в дальнейшем будет удобнее, т.к. не нужно будет на это отвлекаться и сразу будем писать название класса).

```html
	<header class="header">
		
	</header>
```

3)Добавляем внутри тега header тег div с классом container и объясняем для чего он нужен.
```html
	<header class="header">
		<div class="container">
			
		</div>
	</header>
```
4)Добавляем внутри тега div тег img для картинки, задаём ему класс logo и путь до нужной картинки
```html
<header class="header">
		<div class="container">
			<img src="img/image.png" class="logo">
```
5)Добавляем тег nav с классом nav
```html
	<header class="header">
		<div class="container">
			<img src="img/image.png" class="logo">
			<nav class="nav">
				
			</nav>
		</div>
	</header>
```
6)В него добавляем список с классом nav__list
```html
	<header class="header">
		<div class="container">
			<img src="img/image.png" class="logo">
			<nav class="nav">
				<ul class="nav_list"></ul>

			</nav>
		</div>
	</header>
```
7)Заходим в Figma, смотрим сколько элементов у нас в навигации и добавляем такое же количество тегов li с классом nav__item.

<img src="images/Picture (45).png" alt="Картинка)">

```html
<ul class="nav__list">
  <li class="nav__item">Главная</li>
  <li class="nav__item">Об авторе</li>
  <li class="nav__item">Видео</li>
  <li class="nav__item">Галерея</li>
</ul>
```
8)С html мы закончили и получилось вот так.
```html
	<header class="header">
		<div class="container container_header">
			<img src="img/image.png" class="logo">
			<nav class="nav">
				<ul class="nav__list">
					<li class="nav__item">Главная</li>
					<li class="nav__item">Об авторе</li>
					<li class="nav__item">Видео</li>
					<li class="nav__item">Галерея</li>
				</ul>
			</nav>
		</div>
	</header>
```
9)Переходим в css. Объясняем, что задаём свойства классам по порядку.

Переходим в Figma и показываем Dev Mode

<img src="images/Picture (46).png" alt="Картинка)">

11)Копируем свойство background для header и задаём в style.css

<img src="images/Picture (47).png" alt="Картинка)">

```css
.header {
	background: #D1233E;
}
```

12)Переходим к классу container, рассказываем, что его часто используют и для чего он нужен и задаём свойства. Объясняем почему используем max-width

```css
.container {
	max-width: 1110px;
	margin: 0 auto;
}
```

13)Обращаем внимание на то, что этот класс будем использовать почти во всех секциях. Но нужно задать свойства, которые не понадобятся в других. Поэтому добавим ещё один класс и задаём свойства (объяснем для чего нужны).
```html
<div class="container container_header">
```
```css
.container_header {
	display: flex;
	justify-content: space-between;
	align-items: center;
}
```

14)Также этому классу нужно задать padding. Показываем как можно посмотреть значение отступа в Figma и задаём.

<img src="images/Picture (48).png" alt="Картинка)">

```css
.container_header {
	display: flex;
	padding: 27px 0;
	justify-content: space-between;
	align-items: center;
}
```

15)Переходим к классу nav__list. Распологаем элементы списка в строку и убираем точки.

```css
.nav__list {
	display: flex;
	list-style: none;
}
```

16)Переходим к классу nav__item и задаём отступы. (показываем где можно узнать значение)

<img src="images/Picture (49).png" alt="Картинка)">

```css
.nav__item {
	margin-right: 63px;
}
```

17)Добавляем стили, которые изменяют текст (если времени не много то просто копируем всё с Figma)

<img src="images/Picture (50).png" alt="Картинка)">

```css
.nav__item {
	margin-right: 63px;
	color: #FFF;
	font-family: Nico Moji;
	font-size: 18px;
	font-style: normal;
	font-weight: 400;
	line-height: normal;
}
```

Готово!

Дополнительно:
1)Разобрать все свойства, которые задали nav__item

2)Добавить внутри тега li тег a с классом nav__link и задать ему нужные стили, для изменения текста. В атрибут href добавить # для заглушки.

3)У хардов на макете в логотипе есть текст – добавляем

4)Изучить 2 псевдокласса :not и :last-child и использовать их вместе для nav__item

5)Также у хардов есть иконка – можно её добавить

<img src="images/Picture (51).png" alt="Картинка)">

## 🎯 Заключение для преподавателя

К концу урока у учеников должно быть:

- готовая структура header с логотипом и навигацией;

- подключённые стили для контейнера и списка;

- понимание, зачем нужны justify-content и align-items.

Совет:

- Вопрос «А зачем нужен контейнер?» задайте обязательно — это закрепит понимание.

- Можно устроить мини-турнир: кто быстрее сделает список навигации и уберёт точки.

- Хард-группе покажите псевдоклассы (:not, :last-child), а изикам — просто дайте радость от красивого аккуратного header.
