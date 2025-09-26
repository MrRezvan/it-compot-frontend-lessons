## 🚀 Урок: Секция Video  

# 🎤 Вступление для преподавателя  

Сегодня ребята создадут секцию **video** 🎬 — элемент сайта, в котором можно встроить YouTube-видео.  
Это хорошая возможность познакомить их с новым тегом `<iframe>` и свойством `box-sizing`.  
Можно объяснить детям так: «Представьте, что у вас есть телевизор, который можно вставить прямо в сайт. Вот для этого и нужен iframe — он показывает уже готовый контент внутри вашей страницы».  

Совет: дайте ребятам самим выбрать видео для вставки. Это сделает задание интереснее и персональнее.  

---

# 📖 Исходный текст  

Video  
На этом занятии мы реализуем секцию video. Вспомним для чего нужна эта часть, познакомимся с тегом iframe и свойством box-sizing, научимся встраивать видео с ютуба на свою страницу, а также вспомним несколько тегов и свойств, которые мы изучали.  
Классы использовать такие же, как и в методичке. Чтобы в дальнейшем не было проблем с назначением свойств и при переводе к другому преподавателю.  

——————————————————————————————————————————  

1) Открываем макет, рассуждаем по поводу секции video (для чего он нужен и что там располагается).  
2) Переходим в Sublime Text, а именно в index.html и после тега section добавляем тег section и сразу задаём ему класс video.  

```html
		<section class="video">
			
		</section>
```

3) Внутрь добавляем тег div с классом container и container_video.  
```html
		<section class="video">
			<div class="container container_video">

			</div>
		</section>
```
4) Теперь переходим в Figma и смотрим, какие элементы находятся в этой секции. Первым идёт заголовок. Для реализации этого заголовка используем тег h2 с классом video__title.  
```html
		<section class="video">
			<div class="container container_video">
				<h2 class="video__title">Видео</h2>
			</div>
		</section>
```
5) Дальше идёт видео. Для того, чтобы добавить видео с ютуба, нужно перейти на этот сайт и найти нужное видео.  
6) Под видео нажимаем на кнопку поделиться.  

<img src="images/Picture (70).png" alt="kartinka">

7) Встроить.  

<img src="images/Picture (71).png" alt="kartinka">

8) Копировать.  

<img src="images/Picture (72).png" alt="kartinka">

9) И вставляем в html.  
```html
		<section class="video">
			<div class="container container_video">
				<h2 class="video__title">Видео</h2>
				<iframe class="video__video" src="https://www.youtube.com/embed/AQHBkqelmUc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
			</div>
		</section>
```
10) Рассказываем подробнее про тег iframe (как минимум то, что этот тег нужен для встраивания уже готового html).  

11) Переходим к стилям. Начинаем с класса video. Этому классу нужно задать только свойство background. Значение ученики ищут сами в Figma.  
```css
.video {
	background: #1A1A1A;
}
```
12) Теперь класс container_video. Ему задаём padding. Значения ученики ищут сами в Figma.  
```css
.container_video {
	padding: 70px 0 98px;
}
```
13) Переходим к классу video__title. Ученики сами копируют стили, которые есть в Figma.  
```css
.video__title {
	color: #E4E4E4;
	font-family: Nico Moji;
	font-size: 48px;
	font-style: normal;
	font-weight: 400;
	line-height: normal;
}
```
14) Осталось выровнять этот заголовок по центру и добавить внешний отступ снизу. Ученики пробуют реализовать это сами.  
```css
.video__title {
	color: #E4E4E4;
	font-family: Nico Moji;
	font-size: 48px;
	font-style: normal;
	font-weight: 400;
	line-height: normal;
	text-align: center;
	margin-bottom: 38px;
}
```
15) Переходим к классу video__video. Но перед этим удалим у тега iframe атрибут width и height, объясняем для чего мы это сделали (чтобы не было в дальнейшем проблем с работой стилей).  
16) Задаём ширину 100%, т.к. видео занимает весь контейнер. Объясняем почему это работает.  
```css
.video__video {
	width: 100%;
}
```
17) Задаём высоту. Значения ученики смотрят сами в Figma. Значение высоты нужно без бордера.  

<img src="images/Picture (73).png" alt="kartinka">

```css
.video__video {
	width: 100%;
	height: 568px;
}
```
18) Теперь реализуем border. Обращаем внимание на то, что не всегда Figma показывает нужные стили и нужно их знать самому. Figma не заменяет знания, а упрощает и ускоряет работу. Пусть ребята сами пробуют реализовать это. Если ребята не помнят, как задавать бордер – напоминаем, говорим что есть 3 значения, напоминаем очерёдность и ребята пусть сами пробуют найти нужные значения.  
```css
.video__video {
	width: 100%;
	height: 568px;
	border: 50px solid #D1233E;
}
```
19) И для округления углов добавляем свойство border-radius. Значение ученики находят сами в Figma.  
```css
.video__video {
	width: 100%;
	height: 568px;
	border: 50px solid #D1233E;
	border-radius: 29px;
}
```
20) Но можно заметить, что теперь iframe вылазит из контейнера. Рассуждаем с учениками почему это произошло (к 100% ширины элемента добавилось 100px от border).  

<img src="images/Picture (74).png" alt="kartinka">

21) Рассуждаем с учениками как можно это починить. После знакомим со свойством box-sizing и задаём его со значением border-box классу video__video.  
```css
.video__video {
	width: 100%;
	height: 568px;
	border: 50px solid #D1233E;
	border-radius: 29px;
	box-sizing: border-box;
}
```
22) Так как мы задали свойство box-sizing со значением border-box, высота теперь задана не совсем правильно – исправляем.  
```css
.video__video {
	width: 100%;
	height: 668px;
	border: 50px solid #D1233E;
	border-radius: 29px;
	box-sizing: border-box;
}
```
---

Дополнительно:  
1) Добавить секцию с встроенной картой. Инструкция — https://disk.yandex.ru/i/2c3irtmvMimzTA  

---

## 🎯 Заключение для преподавателя  

В конце урока у учеников будет готова секция **video** с:  

- заголовком;  
- встроенным YouTube-видео;  
- корректным стилевым оформлением;  
- пониманием, зачем нужен `<iframe>` и как работает `box-sizing`.  

Совет:  
- Можно предложить ребятам поэкспериментировать с разными видео и рамками.  
- Для более сильной группы — дать задание встроить **Google Maps** по инструкции.  
- Для начинающих — главное, чтобы видео корректно отображалось и не «вылезало» за пределы контейнера.  

