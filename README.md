# ПОСТРОЕНИЕ НЕИЗБЫТОЧНОГО ПОКРЫТИЯ

Пусть D<sub>1</sub>, D<sub>2</sub>, ..., D<sub>n</sub> – конечный набор непустых не обязательно различных множеств, называемых областями значений, которым присвоены имена A<sub>1</sub>, A<sub>2</sub>, ..., A<sub>n</sub>. Пара (A<sub>i</sub>, D<sub>i</sub>) называется атрибутом с именем A<sub>i</sub> и областью значений D<sub>i</sub>. Обозначим через R = {A<sub>1</sub>, A<sub>2</sub>, ..., A<sub>n</sub>} конечное непустое множество имен атрибутов, а через r(R) отношение r(R) &#8838; D1 &#215; D2 &#215; ... &#215; Dn.
Элементы отношения r(R) принято называть кортежами.

В теории реляционных баз данных рассматривают только конечные отношения, которые представимы реляционными таблицами. Каждая строка такой таблицы – кортеж, а каждый столбец соответствует атрибуту отношения, при этом порядок столбцов и строк не имеет значения. Ввиду того, что перестановка столбцов не изменяет информационного содержания таблицы,
делается предположение, что декартово произведение D1 &#215; D2&#215; ... &#215; Dn коммутативно

Схемой отношения r(R) называется конечное множество имен атрибутов R = {A<sub>1</sub>, A<sub>2</sub>, ..., A<sub>n</sub>}. При записи схем отношений принято опускать фигурные скобки и запятые, отделяющие имена атрибутов друг от друга. Например, вместо R = {A, B, C} записывают R = ABC

Одним из видов связей между атрибутами являются функциональные зависимости (ФЗ). Пусть X, Y – произвольные подмножества множества R и dom X – домен атрибутов из X. Говорят, что отношение r(R), удовлетворяет функциональной зависимости X → Y, если для всякого его состояния и любого x &#8712; dom X отношение &#960;<sub>Y</sub> (&#963;<sub>X = x (r)</sub>) имеет не более одного кортежа. Здесь  &#960;, &#963; - реляционные операции проекции и селекции соответственно 

К функциональным зависимостям применим набор правил вывода, с помощью которых из некоторой исходной совокупности ФЗ можно вывести другие ФЗ. Пусть X, Y, Z, W &#8838; R. Тогда для любого r(R) верны правила вывода:

F1 (рефлексивность). Всегда X → X;
F2 (пополнение). Если X → Y, то XZ → Y;
F3 (аддитивность). Если X → Y и X → Z, то X → YZ;
F4 (проективность). Если X → YZ, то X → Y;
F5 (транзитивность). Если X → Y и Y → Z, то X → Z;
F6 (псевдотранзитивность). Если X → Y и YZ → W, то XZ → W

Пусть F – множество ФЗ, описывающих связи между атрибутами из R.
Функциональная зависимость X → Y логически следует из F, если каждое допустимое состояние отношения r(R) удовлетворяет также X → Y. Логическая выводимость зависимости X → Y из F обозначается так: F╞ X → Y. Множество всех ФЗ, логически следующих из множества F, называется замыканием F и обозначается F+. Доказано, что система правил вывода F1 – F6
полна. Поэтому X → Y &isin; F<sup>+</sup> тогда и только тогда, когда F╞ X → Y
