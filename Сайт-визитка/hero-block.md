🚀 Урок: Создание Hero-block
🎤 Вступление для преподавателя

Сегодня ребята создадут hero-block 🌟 — самую заметную часть сайта, ту самую «визитку», которую посетитель видит первой.
Можно объяснить детям так: «Представьте, что вы заходите в кафе. Сначала вы видите красивую вывеску и витрину. Точно так же и на сайте — hero-block должен зацепить внимание и показать, о чём сайт».

Совет: превратите задание в игру «Продай идею». Пусть ученики придумают, какой главный текст и кнопку они хотят поставить на свой сайт-визитку, чтобы сразу заинтересовать пользователя.

📖 Исходный текст (сохранён полностью)

Hero-block
На этом занятии мы реализуем hero-block. Вспомним для чего нужна эта часть, а также вспомним несколько тегов и свойств, которые мы изучали.
Классы использовать такие же, как и в методичке. Чтобы в дальнейшем не было проблем с назначением свойств и при переводе к другому преподавателю.

1)Открываем макет, рассуждаем по поводу hero-block (для чего он нужен и что там располагается)
2)Переходим в Sublime Text, а именно в index.html и после тега header добавляем тег main и сразу задаём ему класс main. Вспоминаем, для чего нужен этот тег.
```html
	<main class="main">
		
	</main>
```
3)В тег main добавляем тег section и задаём ему класс hero-block. Вспоминаем для чего нужен этот тег.
```html
	<main class="main">
		<section class="hero-block">
			
		</section>
	</main>
```
4)В тег section добавляем тег div, задаём ему класс container и container_hero-block. Спрашиваем, для чего нужен второй класс.
```html
	<main class="main">
		<section class="hero-block">
			<div class="container container_hero-block">

			</div>
		</section>
	</main>
```
5)Смотрим на макет и спрашиваем что добавляем следующее. Это изображение. В тег div добавляем тег img с классом hero-block__img и в атрибут src вводим путь до нужного изображения.
```html
	<main class="main">
		<section class="hero-block">
			<div class="container container_hero-block">
				<img src="img/img.png" class="hero-block__img">
	    </div>
		</section>
	</main>
```
6)Смотрим на макет и рассуждаем(объясняем), как реализовать расположение заголовка и ссылки(кнопки) таким образом. Добавляем тег div с классом hero-block__content.

<img src="images/Picture (52).png" alt="Картинка">

```html
	<main class="main">
		<section class="hero-block">
			<div class="container container_hero-block">
				<img src="img/img.png" class="hero-block__img">
				<div class="hero-block__content">
				</div>
			</div>
		</section>
	</main>
```
7)Добавляем заголовок. Если в логотипе нет h1 или использовался другой тег, то используем h1, в другом случае h2. И задаём класс hero-block__title.
```html
	<main class="main">
		<section class="hero-block">
			<div class="container container_hero-block">
				<img src="img/img.png" class="hero-block__img">
				<div class="hero-block__content">
					<h1 class="hero-block__title">Человек-паук</h1>
				</div>
			</div>
		</section>
	</main>
```
8)Переходим к «кнопке». Объясняем, что некоторые ссылки похожи на кнопки. Рассказываем разницу между этими элементами. А также в каких случаях использовать эти элементы (ссылку – если нужно по нажатию перейти на другую страницу или другой сайт; кнопку – если по нажатию должно что-то появиться или реализуется другой функционал). После добавляем тег a, назначаем класс hero-block__link и в атрибут href вводим #.
```html
	<main class="main">
		<section class="hero-block">
			<div class="container container_hero-block">
				<img src="img/img.png" class="hero-block__img">
				<div class="hero-block__content">
					<h1 class="hero-block__title">Человек-паук</h1>
					<a href="#" class="hero-block__link">СМОТРЕТЬ</a>
				</div>
			</div>
		</section>
	</main>
```
9)Смотрим на результат и видим, что уже работает класс container. После этого переходим к стилям.

10)Стили задаём по порядку. Первым идёт тег section с классом hero-block. Рассуждаем, какие стили нужно задать этому классу. Идём в Figma и ищем свойство background, после копируем и вставляем в style.css.
```css
.hero-block {
	background: #201E1F;
}
```
11)Дальше идёт container_hero-block. Смотрим на макет и рассуждаем какие стили нужно задать. Это display:flex; justify-content:space-between; и align-items:center; (по возможности вспоминаем для чего нужны эти стили). А также показываем, как посмотреть внутренние отступы у секции и задаём их.

<img src="images/Picture (53).png" alt="Картинка">

```css
.container_hero-block {
	display: flex;
	justify-content: space-between;
	align-items: center;
	padding: 99px 0 91px;
}
```
12)Дальше hero-block__title. Ищём в Figma нужные свойства, копируем и вставляем в style.css.

<img src="images/Picture (54).png" alt="Картинка">

<img src="images/Picture (55).png" alt="Картинка">

```css
.hero-block__title {
	color: #E4E4E4;
	font-family: Nico Moji;
	font-size: 96px;
	font-style: normal;
	font-weight: 400;
	line-height: normal;
}
```
13)Из-за того, что увеличили размер текста – пропал отступ. Поэтому зададим max-width для hero-block__content. Сначала посмотрим в Figma нужное значение. Обращаем внимание, что задавать свойство этому классу нужно перед классом hero-block__title (как минимум, что нужно соблюдать очерёдность классов и будет проще ориентироваться в коде).

<img src="images/Picture (56).png" alt="Картинка">

```css
.hero-block__content {
	max-width: 475px;
}
```
14)Теперь переходим к hero-block__link. Сначала реализуем вид кнопки, а потом перейдём к свойствам текста. Начнём с border-radius и background.

<img src="images/Picture (57).png" alt="Картинка">

<img src="images/Picture (58).png" alt="Картинка">

```css
.hero-block__link {
	border-radius: 6px;
	background: #CC960A;
}
```
15)Нужно добавить внутренние отступы. Сначала смотрим значения в Figma, после задаём их классу hero-block__link.

<img src="images/Picture (59).png" alt="Картинка">

```css
.hero-block__link {
	border-radius: 6px;
	background: #CC960A;
	padding: 29px 136px;
}
```
16)Из-за padding ссылка залазит на заголовок. Поэтому добавляем для класса hero-block__title свойство margin-bottom. Заходим в Figma и находим нужное значение.

<img src="images/Picture (60).png" alt="Картинка">

```css
.hero-block__title {
	color: #E4E4E4;
	font-family: Nico Moji;
	font-size: 96px;
	font-style: normal;
	font-weight: 400;
	line-height: normal;
	margin-bottom: 30px;
}
```
17)А теперь переходим к свойствам текста. Копируем с Figma и задаём их классу hero-block__link.

<img src="images/Picture (61).png" alt="Картинка">

<img src="images/Picture (62).png" alt="Картинка">

```css
.hero-block__link {
	border-radius: 6px;
	background: #CC960A;
	padding: 29px 136px;
	color: #000;
	font-family: Nico Moji;
	font-size: 40px;
	font-style: normal;
	font-weight: 400;
	line-height: normal;
	text-decoration: none;
}
```
Дополнительно:
1)Добавить ссылку в href
2)Добавить тег p между h1 и a.

<img src="images/Picture (63).png" alt="Картинка">

3)Реализовать свечение ссылке и разобрать свойства

<img src="images/Picture (64).png" alt="Картинка">

🎯 Заключение для преподавателя

В конце урока у учеников будет готов hero-block с:

картинкой, заголовком и кнопкой;

правильным позиционированием элементов через flex;

стилями, похожими на макет из Figma.

Совет:

Попросите ребят показать свои hero-блоки друг другу

С хард-группой можно поиграть в «доработку макета» — пусть попробуют сделать эффект свечения кнопки при наведении.

С изиками главное — добиться, чтобы картинка, заголовок и кнопка красиво располагались и не наползали друг на друга.
