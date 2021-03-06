## Структурна лінгвістика

#### 1. Перевірте роботу [SnowballStem](http://snowballstem.org/) для спільнокореневих слів. Напишіть ваші спостереження.

1. truth, truthful, truthfulness, countertruth, untruthful, truthology

| **Original** | **Stemmed**  |
|--------------|--------------|
| truth        | truth        |
| truthful     | truth        |
| truthfulness | truth        |
| countertruth | countertruth |
| untruthful   | untruth      |
| truthology   | trutholog    |

Не розпізнае префікси.
працює лише з суфіксами, відрізає закінчення слова ( ```-ful```, ```- fulness```, ```-y```, ```-ness``` )

2. flaw, flaws, flawed, flawless, flawlessness, flawlessly

| **Original** | **Stemmed** |
|--------------|-------------|
| flaw         | flaw        |
| flaws        | flaw        |
| flawed       | flaw        |
| flawless     | flawless    |
| flawlessness | flawless    |
| flawlessly   | flawless    |

Не відрізае суфікс ```-less```

Відрізав закінчення слова ( ```-s```, ```- ed``` )

в цілому досить непогано справляється з англійською мовою та звів більшість до більш простих словоформ
 
3. лес, лесной, лесник, лесничий, лесничество, пролесье

| **Original** | **Stemmed** |
|--------------|-------------|
| лес          | лес         |
| лесной       | лесн        |
| лесник       | лесник      |
| лесничий     | леснич      |
| лесничество  | лесничеств  |
| пролесье     | пролес      |

Відрізав закінчення слова ( ```-ой```, ```- ий```, ```-о```,```-ье``` )

4. окно, окошко, подоконник, оконный, окнище

| **Original** | **Stemmed** |
|--------------|-------------|
| окно         | окн         |
| окошко       | окошк       |
| подоконник   | подоконник  |
| оконный      | окон        |
| окнище       | окнищ       |

Тут взагалы выдрызав від кореневогго слова ```-о```

Відрізав закінчення слова ( ```-е```, ```- ый```)

Для російскоі працює так собі, відрізає від кореневого слова його частину, та в результаті стемінгу все одно залишилось стільки ж словоформ скільки й було. 
#### 2. Визначте частину мови виділеного слова і слово, яке є його батьком (за зразком):

```
{I} like turtles.: pronoun, like  
I {like} turtles.: verb, ROOT  
I like {turtles}.: noun, like
```

я использую тут UD anotation https://universaldependencies.org/u/dep/index.html

1. We can {but} hope that everything will be fine. : cc, can
2. It's sad {but} true. : cc, sad
3. Jack brings nothing {but} trouble. : case, trouble
4. Let's do it this {way}! : xcomp, do
5. This is {way} too much! : advmod, much
6. The prices are going {down}. :compound, going
7. Someone pushed him and he fell {down} the stairs. : compound, fell
8. I’ve been feeling rather {down} lately. : advmod, feeling
9. It's not easy to {down} a cup of coffee in one gulp. : advmod, gulp
10. Bring a {down} jacket and a pair of gloves, and you'll be fine. : amod, jacket

#### 3. Визначте частину мови виділеного слова і слово, яке є його батьком (за зразком):

```
{Я} люблю черепашок.: займенник, люблю  
Я {люблю} черепашок.: дієслово, ROOT  
Я люблю {черепашок}.: іменник, люблю  
```

1. Рада міністрів Європейського союзу затвердила угоду про спрощений порядок видачі {віз} для України. : Іменник, видачі 
2. Батько Себастьяна {віз} на санях їх театральний гурт до Львова. : Дієслово, ROOT
3. А ще дивний елемент інтер’єру – {віз} із продукцією одного з херсонських виробників. : іменник, елемент
4. У цю мить {повз} Євгена пролетів останній вагон товарняка. : прислівник, пролетів
5. Кліпнув очима і побачив малого песика, який саме пробігав {повз} у бік села. : прислівник, пробігав
6. Степанко перестав кричати, тільки ламкий стогін {повз} йому із грудей. : дієслово, перестав
7. Ось присіла на {край} ліжка. : прийменник, ліжка
8. Поставив ту кузню не {край} дороги, як було заведено, а на Красній горі, біля Прадуба. : прийменник, дороги
9. Розповідаючи про передній {край} лінґвістики, фон Лібіх, як завжди, мислив широко і глобально. : прийменник, лінгвістики
10. Не {край} мені серце. : дієслово, ROOT

#### 4. Виберіть одне речення зі списку та побудуйте для нього дерево залежностей:

(Дерево можна намалювати в графічному редакторі або на папері і докріпити картинку до домашнього завдання. Назви частин мови та залежностей можна не писати. Головне - це структура.)

1. Пригадую, уже згодом, коли я відбував свій термін у таборі № 36 у Кучино Пермської області, я отримав від Михасі листівку з жартівливим описом того, як Київ готується до святкування свого 1500-ліття.
2. 6C приземляється на плече, перекочуючись, пролітає метрів п’ятдесят і витягується на снігу за кілька кроків від забризканої палаючими уламками посадкової смуги.
3. Дівчина стояла там, де й була, і намагалася привести до ладу скуйовджене волосся, вкрай розлючена тим, що це побачили водії, які чекали на переїзді.

#### 5. Виберіть одне cлово зі списку та побудуйте лексико-семантичні зв'язки до трьох різних значень цього слова. Фактично, потрібно побудувати WordNet-подібні вузли, тобто для кожного з трьох значень підібрати синоніми, антоніми, мероніми, голоніми, гіпоніми та гіпероніми, якщо такі є. Значення слів можна перевірити у [СУМі](http://sum.in.ua/) чи [Словниках України](http://lcorp.ulif.org.ua/dictua/).

Слова на вибір: вік, стіна, добро, серце, центр, **{куля}**, міст, ланцюг, бік, дух.

куля.01 - Геометричне тіло, утворене обертанням кола навколо свого діаметра. Радіус кулі; Поверхня кулі. {синонім: сфера, кулька } {меронім: радіус, коло} {голонім: фігура}

куля.02 - Маленький свинцевий або стальний снаряд для стрільби із ручної вогнепальної зброї і кулеметів, що являє собою передню частину бойового патрона. {синонім: дев'ять грам,  набій  } {меронім: порох, набій, } {голонім: зброя}

куля.03 - (діал)допоміжний засіб для ходіння, що переносить вагу тіла з ніг до його верхньої частини. Використовується особами, які не можуть спиратися на одну чи обидві ноги, внаслідок травми чи інвалідності. {синонім: милиця, костур, костуряка } {меронім: палиці } {голонім: інструмент}