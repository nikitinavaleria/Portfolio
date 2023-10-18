# Исследование объявлений о продаже квартир

Получены данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет.

**Цель**: научиться определять рыночную стоимость объектов недвижимости.

**Задача**: установить параметры для построения автоматизированной системы: она отследит аномалии и мошенническую деятельность.

**Описание данных**

По каждой квартире на продажу доступны два вида данных. Первые вписаны пользователем, вторые — получены автоматически на основе картографических данных. Например, расстояние до центра, аэропорта, ближайшего парка и водоёма.

**airports_nearest** — расстояние до ближайшего аэропорта в метрах (м)

**balcony** — число балконов

**ceiling_height** — высота потолков (м)

**cityCenters_nearest** — расстояние до центра города (м)

**days_exposition** — сколько дней было размещено объявление (от публикации до снятия)

**first_day_exposition** — дата публикации

**floor** — этаж

**floors_total** — всего этажей в доме

**is_apartment** — апартаменты (булев тип)

**kitchen_area** — площадь кухни в квадратных метрах (м²)

**last_price** — цена на момент снятия с публикации

**living_area** — жилая площадь в квадратных метрах (м²)

**locality_name** — название населённого пункта

**open_plan** — свободная планировка (булев тип)

**parks_around3000** — число парков в радиусе 3 км

**parks_nearest** — расстояние до ближайшего парка (м)

**ponds_around3000** — число водоёмов в радиусе 3 км

**ponds_nearest** — расстояние до ближайшего водоёма (м)

**rooms** — число комнат

**studio** — квартира-студия (булев тип)

**total_area** — общая площадь квартиры в квадратных метрах (м²)

**total_images** — число фотографий квартиры в объявлении

## Выводы

Было проведено исследование объявлений о продаже квартир

Изучены и проанализированы данные сервиса Яндекс.Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктов за несколько лет.

Определены  параметры, по которым можно построить автоматизированную систему, чтобы оценить рыночную стоимость объектов недвижимости

На **этапе предобработки** были определены и заполнены возможные пропуски в данных, устранены аномалии, дубликаты, выделены особенности полученных данных. Также добавлены новые данные, полученные на основе исходных данных. Проведена категоризация некоторых данных для более удобной оценки параметров.

На **этапе исследовательского анализа данных** были выделены необходимые закономерности и проведены следующие действия:

*1) Построение гистограмм для выявления параметров квартир, которые встречаются чаще всего. Таким образом, чаще всего встречаются квартиры:*

- с площадью до 100кв.м.;
- с кухней до 15 кв.м.;
- с ценой 3-5млн; с 1-4 комнатами;
- с высотой потолков 2,5 метра;
- на 1-6 этажах;
- с расстоянием до центра до 20км;
- с расстоянием до аэропорта от 10 до 40км;
- с расстоянием до парка 400-800м;
- выявлено, что большинство квартир выставляется на продажу в в феврале, марте, апреле и ноябре;
- на 1-ое и 10-ое число месяца также приходится большинство объявлений;
- объявления выставляются в основном будни.

*2) Изучение времени продажи квартир.*

- Есть отдельные пики продаваемости на примерно 45, 60 и 90 дни продажи.
- Среднее время продажи до 95 дней.
- Необычайно долгими можно считать продажи квартир более 600 дней.

*3) Изучение факторов, которые влияют на стоимость. Ниже представлены факторы в порядке убывания влияния на стоимость и коэффициент корреляции:*

- общая площадь 0.7
- жилая площадь 0.6
- площадь кухни 0.5
- количество комнат 0.4
- квартиры с первыми и последними этажами дешевле, чем с другими. При этом квартиры на первом этаже самые дешевые.
- стоимость квартиры больше, если объявление публикуется в начале недели. По графику видно отрицательный коэффициент, если не брать первый день недели. То есть при приближении к концу недели стоимость становится меньше.
- меньше всего квартиры стоят в мае-июне, а больше всего в апреле.
- невозможно оценить дальнейшую тенденцию роста цен по годам. В 2014 году был пик стоимости квартир. Дальше стоимость падала экспоненциально до 2017 года. Далее пошел медленный рост.

*4) Изучение средней цены одного квадратного метра в 10 населённых пунктах с наибольшим числом объявлений.*

Ниже представлена таблица с ценами за один квадратный метр в 10 населённых пунктах с наибольшим числом объявлений в порядке убывания цены:

 - санкт-петербург     104761.9
 - пушкин              100000.0
 - деревня кудрово     91860.4
 - поселок парголово   91642.8
 - поселок мурино      85878.4
 - поселок шушары      76876.2
 - колпино             74723.7
 - гатчина             67796.6
 - всеволожск          65789.4
 - выборг              58158.3

*5) Изучение средней цены каждого км для квартир в Санкт-Петербурге.*

В целом видна тенденция к падению стоимости с увеличением расстояния от центра. Однако есть отдельные “дорогие” километры. Однако эта особенность может быть связана с другими параметрами квартир.