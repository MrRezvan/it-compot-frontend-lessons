# 🚀 Урок: Footer

## 🎤 Вступление для преподавателя
На этом занятии мы реализуем **footer**.  
Важно напомнить детям, зачем нужна эта часть сайта и что обычно там располагается.  
Совет: акцентируй внимание на повторении уже знакомых тегов и свойств — это поможет закрепить материал.  

---

## 📖 Исходный текст

1) Открываем макет, рассуждаем по поводу **footer** (для чего он нужен и что там располагается).  

2) Переходим в Sublime Text, а именно в **index.html** и после тега `main` добавляем тег `footer` и сразу задаём ему класс `footer`.  
```html
	<footer class="footer">
		
	</footer>
```
3) Создаём тег `div` и задаём ему 2 класса – `container` и `container_footer`.  
```html
	<footer class="footer">
		<div class="container container_footer">

		</div>
	</footer>
```
4) Для реализации заголовка и текста в столбик добавим ещё один тег `div` с классом `footer__content`.  
```html
	<footer class="footer">
		<div class="container container_footer">
			<div class="footer__content">
				
			</div>
		</div>
	</footer>
```
5) Теперь добавляем `h3` с классом `footer__title` и заполняем его.  
```html
	<footer class="footer">
		<div class="container container_footer">
			<div class="footer__content">
				<h3 class="footer__title">SPIDER MAN</h3>
			</div>
		</div>
	</footer>
```
6) Добавляем тег `p` с классом `footer__text` и заполняем его.  
```html
			<div class="footer__content">
				<h3 class="footer__title">SPIDER MAN</h3>
				<p class="footer__text">2023. Все права защищены.</p>
			</div>
```
7) Не хватает знака копирайта. Скидываем ученикам ссылку на спецсимволы — https://htmlbook.ru/samhtml/tekst/spetssimvoly и знакомимся с ними.  

8) Ученики находят этот знак и вставляют в тег `p`.  
```html
			<div class="footer__content">
				<h3 class="footer__title">SPIDER MAN</h3>
				<p class="footer__text">&copy; 2023. Все права защищены.</p>
			</div>
```
9) Переходим к реализации списка с соцсетями. Добавляем тег `ul` с классом `footer__list`.  
```html
<div class="container container_footer">
			<div class="footer__content">
				<h3 class="footer__title">SPIDER MAN</h3>
				<p class="footer__text">&copy; 2023. Все права защищены.</p>
			</div>
			<ul class="footer__list">
				
			</ul>
		</div>
```
10) Добавляем элемент списка с помощью тега `li` с классом `footer__item`.  
```html
<div class="container container_footer">
			<div class="footer__content">
				<h3 class="footer__title">SPIDER MAN</h3>
				<p class="footer__text">&copy; 2023. Все права защищены.</p>
			</div>
			<ul class="footer__list">
				<li class="footer__item">

				</li>
			</ul>
		</div>
```
11) Добавляем тег `a` для реализации ссылки. Задаём ему класс `footer__link`. В `href` пишем `#`.  
```html
<div class="container container_footer">
			<div class="footer__content">
				<h3 class="footer__title">SPIDER MAN</h3>
				<p class="footer__text">&copy; 2023. Все права защищены.</p>
			</div>
			<ul class="footer__list">
				<li class="footer__item">
					<a href="#" class="footer__link">
					
					</a>
				</li>
			</ul>
		</div>
```
12) Внутри тега `a` добавляем тег `img` с классом `footer__img`. В `src` задаём путь до нужной картинки.  
```html
<div class="container container_footer">
			<div class="footer__content">
				<h3 class="footer__title">SPIDER MAN</h3>
				<p class="footer__text">&copy; 2023. Все права защищены.</p>
			</div>
			<ul class="footer__list">
				<li class="footer__item">
					<a href="#" class="footer__link">
						<img src="img/telegram.png" class="footer__img">
					</a>
				</li>
			</ul>
		</div>
```
13) Копируем тег `li` со всем содержимым и вставляем столько элементов списка, сколько нужно.  

14) Меняем содержимое атрибута `src` в каждом теге `img`.  

15) Переходим к CSS. Первый класс с которым работаем – `footer`. Для него нужно задать свойство `background`. Значение копируем с **Figma**.  
```css
.footer {
	background: #2C2C2C;
}
```

16) Переходим к классу `container_footer` и задаём ему свойства. Ученики или сами задают эти свойства, или мы помогаем вспомнить им, зачем они нужны.
```css
.container_footer {
	display: flex;
	justify-content: space-between;
	align-items: center;
}

```
17) Этому же классу задаём padding. Значение ученики смотрят в Figma.
```css
.container_footer {
	display: flex;
	justify-content: space-between;
	align-items: center;
	padding: 50px 0 52px;
}  
```
18) Переходим к классу footer__title и ученики копируют текстовые свойства с Figma.
```css
.footer__title {
	color: #E4E4E4;
	font-family: Nico Moji;
	font-size: 30px;
	font-style: normal;
	font-weight: 400;
	line-height: normal;
}
```
19) Этому классу задаём свойство margin-bottom. Значение ученики смотрят в Figma.
```css
.footer__title {
	color: #E4E4E4;
	font-family: Nico Moji;
	font-size: 30px;
	font-style: normal;
	font-weight: 400;
	line-height: normal;
	margin-bottom: 18px;
}
```
20) Переходим к классу footer__text и ученики копируют свойства с Figma.
```css
.footer__text {
	color: #FFF;
	font-family: Nico Moji;
	font-size: 16px;
	font-style: normal;
	font-weight: 400;
	line-height: 164.063%; /* 26.25px */
}
```
21) Переходим к классу footer__list. Списку нужно отключить точки, а его элементы расположить в строку.
Спрашиваем у учеников, как это можно сделать и какие свойства для этого нужны.
```css
.footer__list {
	display: flex;
	list-style: none;
}
```
22) Переходим к классу footer__item и задаём свойство margin-right. Значение ученики смотрят в Figma.
```css
.footer__item {
	margin-right: 40px;
}
```
23) Для того чтобы ссылки были рабочие, нужно вместо # в href вставить ссылку на нужный сайт.

---

## 🔧 Дополнительно
Добавить псевдокласс :not(:last-child) классу footer__item, чтобы не было отступа у крайнего правого элемента.

Добавить кнопку возвращения к началу страницы, используя якорь и position: fixed.

## 🎯 Заключение для преподавателя
К концу урока ученики должны:

уметь создавать структуру футера;

знать, как работать с flexbox;

уметь подключать изображения и ссылки;

повторить спецсимволы и работу с псевдоклассами.

----

Совет: в конце можно задать вопрос ученикам — «Какие ещё элементы вы бы добавили в футер сайта?»
Это стимулирует креативность и закрепляет понимание роли футера в веб-странице.
