# Film distribution
# Исследование данных о российском кинопрокате

**Цель:** выявление текущих трендов рынка российского кинопроката.

**Задача:** изучить рынок российского кинопроката, найти взаимосвязи, посмотреть, насколько фильмы с государственной поддержкой интересны зрителю.

Данные были взяты с портала открытых данных Министерства культуры. Набор данных содержит информацию о прокатных удостоверениях, сборах и государственной поддержке фильмов, а также информацию с сайта КиноПоиск.

## Описание данных

**Таблица mkrf_movies** содержит информацию из реестра прокатных удостоверений. У одного фильма может быть несколько прокатных удостоверений.

 - title — название фильма;
 - puNumber — номер прокатного удостоверения;
 - show_start_date — дата премьеры фильма;
 - type — тип фильма;
 - film_studio — студия-производитель;
 - production_country — страна-производитель;
 - director — режиссёр;
 - producer — продюсер;
 - age_restriction — возрастная категория;
 - refundable_support — объём возвратных средств государственной поддержки;
 - nonrefundable_support — объём невозвратных средств государственной поддержки;
 - financing_source — источник государственного финансирования;
 - budget — общий бюджет фильма;
 - ratings — рейтинг фильма на КиноПоиске;
 - genres — жанр фильма.

Cтолбец budget уже включает в себя полный объём государственной поддержки. Данные в этом столбце указаны только для тех фильмов, которые получили государственную поддержку.

**Таблица mkrf_shows** содержит сведения о показах фильмов в российских кинотеатрах.

 - puNumber — номер прокатного удостоверения;
 - box_office — сборы в рублях.

## Выводы

В работу были получены открытые данные министерства культуры Российской Федерации. Данные были предобработаны и проверены на наличие пропусков, возможные их замены, дубликаты, неявные дубликаты, изменены типы данных и заменены лишние категориальные данные. Также проверены выбросы данных и добавлены новые столбцы для дальнейшей работы и наглядности.

**В основном этапе - в исследовательском анализе данных - были проделаны следующие этапы:**

1) Проверено, сколько фильмов выходило в прокат каждый год
2) Проверено, как менялась динамика проката по годам
3) Посчитана средняя и медианная сумма сборов для каждого года
4) Определено, влияет ли возрастное ограничение аудитории на сборы фильма в прокате в период с 2015 по 2019 год
5) Проверены фильмы, которые получили государственную поддержку

**Были получены следующие выводы:**

1) Меньше всего фильмов представлено в 2012 году. Больше всего представлено в 2010 и 2019. Если говорить о фильмах в российском прокате, то видна тенденция к увеличению доли фильмов с прокатом с годами. Большая доля приходится на 2015-2017 годы. В целом количество фильмов с российским прокатом резко увеличивается в 2015 году.

2) Cумма сборов в 2010 году была минимальной, а в 2018 году максимальной. Виден сильный рост в сборах, начавшийся в 2013 году, и который вышел на плато после 2016 года.

3) Необходимо учитывать медианное значение сборов, а не среднее, потому что медиана более устойчива к выбросам больших и маленьких значений, показывает наиболее частое значение сборов. Так, например, можно увидеть, что средние сборы в 2014 году были около 27 млн, а медианное значение около 0.02млн, что говорит о том, что в 2014 году был какой-то фильм с очень большим кассовым сбором, который как раз повышает среднее значение.

4) В 2010-2013 годах общие сборы по всем категориям были на одном уровне, в 2010 году категория 6+ отсутствовала вовсе. Начиная с 2013 года пошел рост и в 2014 году наибольшие сборы собрала категория 6+ с небольшим отрывом от 18+. Категории 16+ и 0+ собрали меньше всего. В 2015-2016 годах больше всего собрали категории 12+ и 6+, хуже всего собрали категории 18+ и 0+. В 2017 году с большим отрывом большую часть сборов собрала категория 6+, потом 12+, 16+. Наименьшую часть собрали категории 0+ и 18+. В 2018 году больше всего собрали категории 12+,6+, потом 16+. Меньше всего - 18+ и 0+.
Скорее всего увеличение графика после 2013 года связано с увеличением количества выборки, то есть с увеличением количества анализируемых фильмов. Самые собирающие категории - 6+, 12+, а также 16+ связаны с тем, что они захватывают большую аудиторию, способную и имеющую время ходить в кинотеатры. Также скорее всего таких фильмов большинство, потому что в таких фильмах не слишком много жестоких или наоборот детских моментов, поэтому они могут захватывать большую часть зрителей. Категории 0+ и 18+ либо слишком детские, либо с жестокостью или другими специфическими моментами, что интересно не всем зрителям.

5) В среднем объём государственной поддержки фильма - 60 млн.

У фильмов, финансируемых министерством культуры и фондом кино 14/14 = 100% провальных фильмов

У фильмов, финансируемых фондом кино 52% провальных фильмов и 48% успешных фильмов.

Гос поддержка началась с 2014 года.

В 2014 году было 33% провальных и 66% успешных фильмов

В 2015 году было 58% провальных и 42% успешных фильмов

В 2016 году было 76% провальных и 24% успешных фильмов

В 2017 году было 52% провальных и 48% успешных фильмов

В 2018 году было 39% провальных и 61% успешных фильмов

В 2019 году было 61%провальных и 28% успешных фильмов

Больший процент провальных фильмов был в 2016 году. Их процент составил 76%.

Больший процент успешных фильмов был в 2014 году. Их процент составил 66%.

Самые окупившиеся фильмы у Д.Дьяченко(4 фильма) и С.Подгаевского(2 фильма)

Больше всего окупившихся фильмов было снято в следующих студиях:

 - ООО "ЛИЦЕНЗИОННЫЕ БРЕНДЫ" 3
 - ООО "ТаББаК" 3
 - ООО "Студия анимационного кино "Мельница" 3
 - ООО "Ол Медиа Компани" 2
 - АО "ВайТ Медиа", ООО "Арт Пикчерс Студия" 2

Средний рейтинг самых финансируемых фильмов - 5.95. Минимальный - 2.8, Максимальный - 8.5

К 2018-2019 году гос поддержка стала сильно больше, но рейтинги фильмов остались примерно на той же позиции. Это может быть связано с общим подорожанием и экономическими тенденциями.

В основном самые финансируемые фильмы сняли следющие режиссеры:
 - Д.Дьяченко 4
 - С.Андреасян 2
 - А.Матисон 2
 - А.Цицилин 2
 - Н.Хомерики 2
 - С.Подгаевский 2
 - Р.Давлетьяров 2
 - П.Руминов 2

В основном самые финансируемые фильмы сняли следющие студии:
 - ООО "ВИЗАРТ ФИЛЬМ" 4
 - ООО "ТаББаК" 3
 - ООО "Студия анимационного кино "Мельница" 3
 - ООО "ЛИЦЕНЗИОННЫЕ БРЕНДЫ" 3
 - ООО "ТПО "РОК" 2
 - ООО "Ол Медиа Компани" 2
 - ООО "Продюсерская фирма Игоря Толстунова" 2
 - ООО "Кинокомпания "Небо" 2
 - ООО "Кинодом" 2
 - АО "ВайТ Медиа", ООО "Арт Пикчерс Студия" 2
 - ООО "ВВП Альянс" 2

Зависимости между господдержкой и рейтингом нет для самых успешных фильмов с рейтингом от 6.7