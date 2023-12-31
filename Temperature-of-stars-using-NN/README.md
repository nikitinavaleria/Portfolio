# Temperature of stars using NN

# Прогнозирование температуры звезды
Пришла задача от обсерватории «Небо на ладони»: придумать, как с помощью нейросети определять температуру на поверхности обнаруженных звёзд. Обычно для расчёта температуры учёные пользуются следующими методами:
 - Закон смещения Вина.
 - Закон Стефана-Больцмана.
 - Спектральный анализ.

Каждый из них имеет плюсы и минусы. Обсерватория хочет внедрить технологии машинного обучения для предсказания температуры звёзд, надеясь, что этот метод будет наиболее точным и удобным.

В базе обсерватории есть характеристики уже изученных 240 звёзд.

**Характеристики**
 - Относительная светимость L/Lo — светимость звезды относительно Солнца.
 - Относительный радиус R/Ro — радиус звезды относительно радиуса Солнца.
 - Абсолютная звёздная величина Mv — физическая величина, характеризующая блеск звезды.
 - Звёздный цвет (white, red, blue, yellow, yellow-orange и др.) — цвет звезды, который определяют на основе спектрального анализа.
 - Тип звезды: Коричневый карлик 0, Красный карлик 1, Белый карлик 2, Звёзды главной последовательности 3, Сверхгигант 4, Гипергигант 5
 - Абсолютная температура T(K) — температура на поверхности звезды в Кельвинах.

💡 Справочная информация: Светимость Солнца (англ. Average Luminosity of Sun) L0 = 3.828 ⋅ (10)^26 Вт

Радиус Солнца (англ. Average Radius of Sun) R0 = 6.9551 ⋅ (10)^8 м


## Выводы
В данной работе были изучены данные обсерватории. Данные были практически идеальны и потребовали лишь небольшой коррекции признака "цвет". Далее данные были подготовлены к загрузке в нейронную сеть: были стандартизированы и закодированы. Далее было построено несколько вариантов нейронной сети с разными параметрами, после чего к этим вариантам были добавлены улучшения в виде BatchNorm и dropout. Лучших показателей достигнуто не было, поэтому стоит остановиться на более простых baseline моделях. Также ниже указаны улучшения проекта, благодаря которым вероятно выйдет достичь необходимых показателей выбранной метрики rmse

## Улучшения проекта

1) Использовать другие методы стандартизации и нормализации

2) Улучшить baseline: использовать больше слоёв, взять большее количество нейронов в слое, также более грамотно подобрать инициализацию весов, а также параметры улучшения нс
