# <p align="center"> Хакатон по программированию ботов<br>"Bot Fight 1.0"</p>
![logo3](https://github.com/KaBaN4iK357/BotFight/assets/32903150/68153677-f88c-494f-a5ba-d953b6c54a63)
## Вступление
Всех рад приветствовать на открытом хакатоне по программированию ботов.</br>
<b>Целью</b> хакатона является продвижении программирования среди студентов ВУЗов и развитие навыков программирования поисковых алгоритмов. Надеюсь, что участники найдут здесь друзей, единомышленников, обменяются между собой опытом и получат новые знания в программировании.
## О месте проведения
Проведение хакатона планируется в рамках практики по предмету "Информационные технологии и программирование", проводимого на кафедре "Прикладная математика и информационные технологии" (г. Ижевск, ИжГТУ им. М.Т. Калашникова), также к участию приглашаются все желающие студенты других кафедр. Хакатон планируется проводить по мере готовности студентов начиная с <b>2024 года</b> на кафедре "ПМиИТ", 6 корпус, кабинеты 309 и 310.
## О хакатоне (Об игре)
Хакатон рассчитан на 10-30 команд из 1-2 человек. Участники должны разработать алгоритм, который управляет ботом (говорит куда двигаться и что делать), чтобы победить необходимо набрать больше очков, чем другие игроки. Боты передвигаются по общему игровому полю из 40x40 клеток (могут быть и другие поля). </br>
За основу взята игра "Бомбермен" с некоторыми изменениями. Далее представлено изображение игрового поля.
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/3983c038-85f1-4d98-b45c-da4f340b33f9) </br>
Поле имеет прямоугольный вид, на поле размещены игровые объекты (стены, бонусы, ловушки) и игроки, имена ботов противников подписаны красным шрифтом, имя Вашего бота отмечается зеленым шрифтом, справа отображается таблица игроков.

Игра протекает <b>пошагово</b>. На каждый ход игрокам дается <b>2 секунды</b> на отправку действия на сервер.

## Правила хакатона
<b>Запрещается:</b>
* Управлять ботом "вручную" тем или иным образом.
* Намеренно препятствовать работе сервера.

### Игровые объекты
#### Укрепленная стена
![HeavyWall](https://github.com/KaBaN4iK357/BotFight/assets/32903150/bcdef53b-eb23-4dbb-9925-12f4b7c58a4b)  </br>
<b>Свойства объекта:</b></br>
* Препятствует передвижению. </br>
* Нельзя уничтожить. </br>
* Защищает от взрывов (см. подробности в п. "Мина", "Бомба" и "Суперсила"). </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/24a8d926-8912-4c72-8941-d51c96277850) </br>

#### Обычная стена
![Wall](https://github.com/KaBaN4iK357/BotFight/assets/32903150/8ffa6779-cb72-41d3-b4f7-3f3cb29dcedf) </br>
<b>Свойства объекта:</b></br>
* Препятствует передвижению. </br>
* Можно уничтожить. </br>
* Защищает от взрыва, после чего разрушается (см. подробности в п. "Мина", "Бомба" и "Суперсила"). </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/cb543bec-81e9-4004-a3cd-960eba0ce876) </br>

#### Порох
![Powder](https://github.com/KaBaN4iK357/BotFight/assets/32903150/46363242-0258-4abe-88dd-f1899e653af1) </br>
<b>Свойства объекта:</b></br>
* Можно уничтожить взрывом. </br>
* Может быть подобран игроком. </br>
* При подборе дает 1 очко и увеличивает дальность взрыва бомбы на 1 клетку. </br>

взрыв бомбы при 0 пороха </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/90e0b3b7-456a-448d-8e34-0b666cfc8946) </br>
взрыв бомбы при 1 порохе </br> 
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/3b822477-c44b-4813-8d2c-6156f88f96a4) </br>
взрыв бомбы при 2 порохах</br> 
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/7672ed88-511e-446a-8ce9-cab4b9386826) </br>

#### Мина
![mine](https://github.com/KaBaN4iK357/BotFight/assets/32903150/8390e934-c646-49c9-82fb-2d9514def9ab) </br>
<b>Свойства объекта:</b></br>
* Взрывается если игрок наступил. </br>
* Радиус взрыва равен 2 клетки </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/40287c6a-cfc6-42b8-9fba-00d9c8d3dc4c)
* Взрыв может быть остановлен стенами </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/623f3c26-f8f4-4a76-87fc-cfffa65df6bc)
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/c329f3eb-0aed-446a-b97d-5db4cbce7dc5)
* Возможны цепные реакции взрывов </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/06e4eeb3-11c1-4b80-ac1d-7579b56280cb)
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/04be7905-8823-4826-a436-794367e22225)
* Игрок, который инициировал взрыв мины (наступив или взорвав) считается инициатором взрыва. </br>
* Если мина подорвала игрока, то очки начисляются инициатору взрыва. </br>
* Нельзя получить очки за подрыв самого себя. </br>

#### Алмаз
![Diamond](https://github.com/KaBaN4iK357/BotFight/assets/32903150/006d05da-f673-4560-82fd-64c95b7d7410) </br>
<b>Свойства объекта:</b></br>
* При подборе дает 10 очков</br>
* Нельзя уничтожить взрывом </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/feaab590-1843-4617-9f7f-92d5b64ec396)
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/24d7394d-0be1-4dd8-957d-43507fa6c7ef)
* Не защищает от взрыва. </br>

#### Бонус "Постройка"
![build](https://github.com/KaBaN4iK357/BotFight/assets/32903150/8bf2df35-2a86-44f6-a4d4-1732edb0d196) </br>
<b>Свойства объекта:</b></br>
* Может быть подобран игроком. </br>
* При подборе возводит стены вокруг игрока. </br>
* Стены возводятся только в пустых ячейках. </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/5912db2d-df94-4914-a10f-21527f519743)
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/74063a42-946a-44f3-9408-ab090bcdf13b)

#### Суперсила
![SuperPower](https://github.com/KaBaN4iK357/BotFight/assets/32903150/013bbf55-dddb-4263-be72-9135ef3c86f1) </br>
<b>Свойства объекта:</b></br>
* Может быть подобран игроком. </br>
* При подборе у игрока меняется модель </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/a0a7aa3f-04cc-46a6-9032-f977a300cd86) </br>
* При подборе дает игроку суперсилы на следующие 10 ходов. </br>
* Во время действия суперсилы игрок неуязвим </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/73221756-bc23-442b-b43a-726ab1a78a84) </br>
* Установка бомбы заменяется на выстрел в заданном направлении. </br>
* Выстрел пробивает насквозь 1 простую стену </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/c607923a-1158-4832-994f-c973ca3ed355) </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/3704bd0b-29b3-4531-8c2a-32f37121494a) </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/427d700d-4b4b-4286-854d-21ada7278ecb) </br>
* Дальность выстрела равна удвоенной дальности взрыва бомбы. </br>

#### Бомба
![bomb](https://github.com/KaBaN4iK357/BotFight/assets/32903150/952e6218-2d99-4820-b00c-c70161a7b844) </br>
<b>Свойства объекта:</b></br>
* Устанавливается игроком. </br>
* Взрывается на 5-й ход после размещения. </br>
* Радиус взрыва по умолчанию равен 2 клетки </br>
![image](https://github.com/KaBaN4iK357/BotFight/assets/32903150/448b7211-7c61-429a-8bd9-d07a510e3533)

#### Игрок
![player](https://github.com/KaBaN4iK357/BotFight/assets/32903150/7d5a8e9b-bf36-4b01-be9d-2fbd723a4183) </br>
<b>Свойства объекта:</b></br>
* Погибает от взрыва. </br>
* Воскрешается на 3-й ход после смерти. </br>

### Возможные действия игрока
Возможные действия представлены в программе в виде enum [PlayerAction](https://github.com/KaBaN4iK357/BotFight/blob/main/BomberMans/BomberMansTCPFormsLibrary/PlayerAction.cs). За 1 ход игрок может сделать 1 из действий:
* Ничего (None)
* Шаг влево (Left)
* Шаг вправо (Right)
* Шаг вверх (Top)
* Шаг вниз (Bottom)
* Установить бомбу слева от игрока (BombLeft)
* Установить бомбу справа от игрока (BombRight)
* Установить бомбу сверху от игрока (BombTop)
* Установить бомбу снизу от игрока (BombBottom)

```
public enum PlayerAction
{
  None, Left, Right, Top, Bottom, BombLeft, BombRight, BombTop, BombBottom
}
```

### Как устроена игра
Проект представляет собой клиент-серверное приложение. Все операции обрабатываются на сервере, доступ к серверу обеспечивается по локальной сети. В начале каждого хода на компьютеры игроков по TCP в виде строки формата json отправляется текущее игровое поле, далее через 2 секунды происходит обработка ответов игроков и обновление поля. <br>

В репозитории расположена серверная часть проекта в папке [BomberMans](https://github.com/DaniilKlyukin/BotFight/tree/main/BomberMans/BomberMans) и пример клиентской части [BomberManClient](https://github.com/DaniilKlyukin/BotFight/tree/main/BomberMans/BomberManClient), которую должны запускать игроки для общения с сервером и отправки действий ботов. Серверная часть дана для ознакомления с программой и её логикой. Проект целиком написан на языке C#, однако участники при желании могут написть свою клиентскую часть на любом языке программирования. <br>
#### Последовательность обработки ответов игроков:
Запросы обрабатываются в порядке их получения сервером. Это значит, что в случае спорной ситуации, например, когда 2 игрока хотят занять одну и ту же клетку, предпочтение будет отдаваться тому, кто быстрее отправил ответ на сервер.
#### Последовательность операций при обновлении поля:
1. Уменьшение таймера действия суперсилы и её отключение в случае, если истек таймер;
2. Уменьшение таймера бомб;
3. Подрыв бомб, у которых истек таймер;
4. Выполнение действий игроков;
5. Уменьшение таймера воскрешения;
6. Воскрешение игроков, у которых таймер воскрешения истек.

## Как начать программировать своего бота
0. Для начала работы необходимо установить .Net 7.0 SDK если он не установлен;
1. Клонировать (скачать) данный репозиторий на свой компьютер;
2. Запустить клиентскую часть (далее клиент) [BomberManClient.sln](https://github.com/KaBaN4iK357/BotFight/tree/main/BomberMans/BomberManClient);
3. В файле [ClientForm.cs](https://github.com/KaBaN4iK357/BotFight/blob/main/BomberMans/BomberManClient/BomberManClient/ClientForm.cs) задать имя игрока ```const string PlayerName = "Имя игрока";```
4. Для пробного запуска необходимо запустить сервер [BomberMans.sln](https://github.com/KaBaN4iK357/BotFight/tree/main/BomberMans);
5. Далее узнать IP адрес компьютера где запущен сервер, если вы запускаете сервер на своем компьютере, то нужно запустить командную строку и ввести ipconfig, скопировать адрес IPv4;
6. В клиенте перейти в файл [ClientForm.cs](https://github.com/KaBaN4iK357/BotFight/blob/main/BomberMans/BomberManClient/BomberManClient/ClientForm.cs) и ввести IP-адрес сервера </br> ``` c.Connect("192.168.0.194:9000", PlayerName); ```
7. Действие игрока определяется в методе DoWork
 ```
public PlayerAction DoWork(GameObject?[,] map)
{
  return (PlayerAction)rnd.Next(Enum.GetValues<PlayerAction>().Length);
}
```

## Советы и алгоритмы
Далее представлены субъективные общие советы по разработке алгоритма действий бота.
1. Задачу управления ботом стоит разбить на отдельные блоки, отвечающие за:
  + предсказание следующего хода (определение безопасных зон и т.п)
  + поиск бонусов;
  + поиск противников;
  + анализ окружающей области и принятие оптимального действия.
3. Для поиска объектов вокруг игрока целесообразно использовать алгоритм поиска в ширину с ограничением на дальность поиска и с сохранением дальности пути.
4. Рекомендуется использовать ограничение на дальность поиска, т.к. на большой карте не хватит времени на сканирование всего игрового поля. Наиболее простым образом он реализуется с помощью структуры данных Queue.
5. Для поиска кратчайшего пути можно модифицировать поиск в ширину и сохранять путь, либо использовать алгоритмы поиска кратчайшего пути: алгоритм Дейкстры, A* (A-star) и др.
6. При расчете длины пути стоит руководствоваться не только расстоянием, но и тем, через что проходит данный путь. Например, путь, лежащий через бонусы лучше, чем путь аналогичной длины через пустые клетки. Для решения этой задачи необходимо добавить вес (стоимость) клеток и оценивать путь по его стоимости (алгоритм Дейкстры и A* могут искать путь по взвешенному графу).

## Контактная информация
Разработчиком соревнования является инженер-программист 1-й кат., преподаватель курса "ИТиП" Клюкин Даниил Анатольевич (https://vk.com/id194921992).
