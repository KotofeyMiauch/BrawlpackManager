# Brawlpack Manager

**Помощник по размещению предметов в Backpack Brawl для Windows и Android.**  
**An inventory layout planner for Backpack Brawl, available for Windows and Android.**

## Скачать актуальную версию

- 💻 [Скачать для Windows](https://github.com/KotofeyMiauch/BrawlpackManager/releases/latest/download/BrawlpackManager-Windows.exe)
- 📱 [Скачать для Android](https://github.com/KotofeyMiauch/BrawlpackManager/releases/latest/download/BrawlpackManager-Android.apk)

[Что нового в последней версии](https://github.com/KotofeyMiauch/BrawlpackManager/releases/latest)

[Русский](#русский) · [English](#english)

## Русский

### Предыстория разработки

Привет, игроки Backpack Brawl! Я **KotofeyMiauch**.

Некоторое время назад я подсел на эту игру. Мне понравился её геймплей, но довольно быстро обнаружилась знакомая многим проблема: в поздней игре рюкзак полон предметов, и всё это нужно разместить так, чтобы звёзды активировались, крафты происходили, поглощения поглощались и оставалось место для будущих покупок.

Не раз, не два и не десять я тратил на расстановку по 10–15 минут, а иногда — полчаса и больше. И после всего одного боя приходилось переставлять всё заново.

Тогда я вспомнил, что вообще-то умею разрабатывать приложения. Почему бы не решить эту проблему самому? Так появился **Brawlpack Manager**, или просто **BM**: программа, которая ищет эффективную раскладку для выбранных предметов и заданных условий.

Вместе с ChatGPT мы взялись за разработку, и примерно за две недели работы в свободное время получилась версия, которой уже можно пользоваться. Тестируя BM в собственных забегах, я получал раскладки со всеми возможными активными звёздами и несколькими готовыми крафтами одновременно. Программа уже помогла мне подняться по рейтингу и пройти игровые события.

Передаю привет соклановцам из гильдии **«Удача»**! Спасибо всем, кто помогал собирать и уточнять информацию о предметах, чтобы представить их в программе как можно полнее :)

### Текущая версия и возможности

База BM подготовлена для **Backpack Brawl 7.1.0** и включает предметы всех **18 героев**, общие предметы и сумки.

Программа учитывает форму и повороты предметов, звёздные связи, бонусы сумок, крафты, поглощения и превращения. Можно задавать условия и менять их приоритет. Интерфейс поддерживает **русский и английский** языки; выбранный язык, герой, списки предметов и сумок, уровни и условия сохраняются локально.

BM оптимизирует размещение по заданным правилам. **Полноценного симулятора боя в нём пока нет**: больше активных звёзд не всегда означает более сильный боевой билд. Время поиска и возможность доказать оптимальность зависят от набора предметов, условий и устройства.

### Установка

Готовые сборки находятся в разделе **Releases** этого репозитория. Откройте нужный выпуск и скачайте файл для своей платформы из списка **Assets**.

| Платформа | Что скачать | Как запустить |
| --- | --- | --- |
| Windows x64 | Архив Windows-сборки или отдельный EXE, если он приложен к выпуску | Распаковать архив целиком и запустить `BrawlpackManager.Desktop.exe`. Установка не требуется. |
| Android | Подписанный файл `.apk` | Скачать APK на смартфон, открыть его и подтвердить установку. |

На Android может понадобиться разрешить установку приложений из выбранного браузера или файлового менеджера. Название настройки зависит от устройства.

Windows может показать предупреждение SmartScreen о неизвестном приложении: у новой сборки ещё может не быть репутации. Проверяйте источник загрузки; предупреждение о конкретно обнаруженной угрозе стоит разбирать отдельно. Отключать защиту системы для работы BM не требуется.

Архивы **Source code**, которые GitHub добавляет автоматически, содержат файлы репозитория. Для обычного запуска выбирайте готовую сборку своей платформы.

### Быстрый старт

1. Выберите героя.
2. Добавьте свои сумки — это рекомендуется для учёта их бонусов и доступного места.
3. Добавьте предметы текущего рюкзака.
4. Укажите нужные условия и расставьте их по важности.
5. Нажмите **Solve** и наблюдайте за улучшением раскладки.
6. Дождитесь завершения поиска или нажмите **Остановить**, чтобы оставить лучший найденный вариант.
7. При необходимости нажмите **Craft**, чтобы применить доступные преобразования и перейти к следующему состоянию предметов.

### Интерфейс Windows

В центре окна находятся две схемы: **верхняя показывает сумки**, нижняя — **предметы**. Без выбранных сумок используется стандартное поле **9 × 6**, то есть 54 клетки. Если сумки заданы, доступное место определяется ими.

В левой панели можно выбрать героя, переключиться между списками предметов и сумок, найти нужный предмет и добавить его нажатием на иконку. Общие предметы и предметы выбранного героя показываются выше остальных.

Следите за числом занятых клеток: если предметы превышают вместимость, разместить их все невозможно. По умолчанию предметам задан **5-й уровень**; для текущего набора уровень можно уточнить вручную.

Для каждого из списков предметов, сумок и условий предусмотрена кнопка очистки. Перед удалением всего списка BM запросит подтверждение.

### Почему стоит указывать сумки

Сумки влияют не только на свободное место. BM учитывает полезные связи с **Critical Sack**, **Fanny Pack**, **Bolstering Bag** и сумками героев.

Для **Cast Net**, **Drift Net** и **Bottom Trawl** программа также старается сохранять пустые клетки для рыбалки, с учётом более важных условий. Если сумки не указаны, их бонусы не участвуют в оптимизации.

### Условия и их приоритет

В правой панели задаются требования к раскладке. Среди них:

- подготовить крафт, поглощение или превращение;
- максимизировать звёзды выбранного предмета;
- поместить конкретный предмет в звезду другого;
- поместить предмет в сумку с подходящим бонусом;
- выполнить другие доступные для выбранного предмета действия.

**Укажите все условия, которых хотите добиться, и расположите их от наиболее важных к наименее важным.** Для изменения порядка перетаскивайте условие за **⋮⋮** или используйте **↑ / ↓**. Преобразования находятся в отдельной приоритетной группе выше остальных условий.

Переключатель **«Приоритет размещению всех предметов»** определяет начало порядка целей:

| Состояние переключателя | Первые цели |
| --- | --- |
| Включён — по умолчанию | Сначала разместить больше предметов, затем выполнить преобразования. |
| Выключен | Сначала выполнить преобразования, затем разместить больше предметов. |

Далее идут остальные условия, свободные клетки сетей, активные звёзды и бонусы сумок. Текущий порядок также показан в самой панели.

Если условий нет, BM стремится разместить предметы и улучшить общие показатели раскладки. **Преобразования, которые вы хотите применить через Craft, задавайте явно.**

### Solve: поиск раскладки

**Solve** запускает поиск и показывает лучший найденный вариант по мере работы. Под полем отображаются время, счётчики вычислений, число размещённых предметов, активных звёзд и полезных связей сумок.

Простые наборы могут решаться за секунды; для сложных заполненных рюкзаков поиск может занять несколько минут и дольше. Можно отойти попить воды или посмотреть в окно — BM продолжит улучшать результат. На Android время и качество поиска могут отличаться от ПК.

**Найденная раскладка и доказанный оптимум — разные состояния.** Пока поиск продолжается, программа может найти более подходящий вариант. Остановка сохраняет лучший найденный результат, но сама по себе не подтверждает его оптимальность.

Во время Solve BM использует несколько рабочих потоков. Нагрузка на процессор и нагрев устройства могут увеличиваться. Остановить поиск можно в любой момент кнопкой **«Остановить»**.

### Craft: следующий магазин

После завершения или остановки Solve кнопка **Craft** применяет подготовленные преобразования, заданные условиями, а также поддерживаемые гарантированные изменения при входе в магазин.

Исчезнувшие предметы удаляются, гарантированно появившиеся — добавляются. Если результат случаен или его вид неизвестен, BM не выбирает его за игру: **добавьте фактически полученный предмет вручную**.

После Craft проверьте обновлённый набор и условия. Для следующего перехода снова выполните Solve.

### Интерфейс Android

На смартфоне используются те же предметы, условия и правила приоритета. Список предметов и сумок, а также условия открываются кнопками на **левой панели**. Закрыть панель можно кнопкой **×** или системным действием «Назад».

Поиск предметов открывает отдельную область с результатами: вводите часть названия и нажимайте нужную иконку. Переключатель **RU / ENG** позволяет выбрать язык интерфейса.

### Обратная связь

Если нашли ошибку, создайте **Issue** в этом репозитории. Полезно приложить версию BM, платформу, список предметов и сумок, условия в порядке приоритета и снимок результата. Для вылета Android также пригодится журнал ошибки.

BM — неофициальный фанатский инструмент. Backpack Brawl, игровые изображения и названия принадлежат их правообладателям.

**Приятной игры и побед!**

---

## English

### How the project started

Hello, Backpack Brawl players! I'm **KotofeyMiauch**.

I got hooked on the game a while ago. I enjoyed its puzzle-like gameplay, but soon ran into a familiar problem: late in a run, your backpack is full, and everything needs to fit while activating stars, preparing crafts, setting up absorptions, and leaving room for future purchases.

I repeatedly spent 10–15 minutes arranging items, sometimes half an hour or more. After just one fight, I would have to rearrange everything again.

Then I remembered that I can actually develop applications. Why not solve this problem myself? That became **Brawlpack Manager**, or **BM**: a tool that searches for an effective layout based on your items and the conditions you specify.

With ChatGPT's help, about two weeks of development in my spare time produced a version ready to use. While testing it in my own runs, I found layouts with every possible star active and several crafts ready at once. BM has already helped me climb the rankings and progress through events.

Thanks to everyone who helped gather and clarify item information so it could be represented as fully as possible :)

### Current version and features

BM's item database targets **Backpack Brawl 7.1.0** and includes items for all **18 heroes**, shared items, and bags.

The planner accounts for item shapes and rotations, star links, bag bonuses, crafts, absorptions, and transformations. You can specify conditions and adjust their priority. The interface supports **Russian and English**; your language, hero, item and bag lists, levels, and conditions are saved locally.

BM optimizes placement according to its rules. **It does not yet include a full combat simulator**: more active stars do not always mean a stronger combat build. Search time and the ability to prove optimality depend on your items, conditions, and device.

### Installation

Ready-to-run builds are available under **Releases** in this repository. Open a release and download your platform's build from **Assets**.

| Platform | Download | How to run |
| --- | --- | --- |
| Windows x64 | The Windows build archive, or a standalone EXE if provided | Extract the entire archive and run `BrawlpackManager.Desktop.exe`. No installation required. |
| Android | The signed `.apk` file | Download the APK to your phone, open it, and confirm installation. |

On Android, you may need to allow app installation from your chosen browser or file manager. Setting names vary by device.

Windows SmartScreen may warn that the application is unrecognized because a new build may not have an established reputation. Verify the download source; a warning about a specifically detected threat should be investigated separately. BM does not require you to disable system protection.

The **Source code** archives automatically added by GitHub contain the repository files. To run the application, choose your platform's ready-to-run build.

### Quick start

1. Select your hero.
2. Add your bags — recommended for accurate capacity and bag bonus handling.
3. Add the items in your current backpack.
4. Add your conditions and arrange them by priority.
5. Press **Solve** and watch the layout improve.
6. Wait for the search to finish, or press **Stop** to keep the best layout found so far.
7. If needed, press **Craft** to apply available transformations and advance your items to their next state.

### Windows interface

Two boards occupy the center of the window: **bags above**, **items below**. Without selected bags, BM uses a default **9 × 6** board with 54 cells. When bags are specified, they determine the available space.

The left panel lets you select a hero, switch between item and bag lists, search, and add an item by clicking its icon. Shared items and your selected hero's items appear before other heroes' items.

Watch the occupied cell count: if your items exceed the available space, they cannot all be placed. Items default to **level 5**; you can adjust levels for the items on your current board.

The item, bag, and condition lists each have a clear-all button. BM asks for confirmation before clearing an entire list.

### Why you should specify bags

Bags affect more than capacity. BM accounts for useful links with **Critical Sack**, **Fanny Pack**, **Bolstering Bag**, and hero-specific bags.

For **Cast Net**, **Drift Net**, and **Bottom Trawl**, the planner also tries to preserve empty cells for fishing, subject to higher-priority objectives. Bag bonuses cannot be optimized when the corresponding bags are not specified.

### Conditions and priorities

The right panel defines layout requirements, including:

- prepare a craft, absorption, or transformation;
- maximize a selected item's stars;
- place a specific item in another item's star;
- place an item inside a bag with a relevant bonus;
- perform other supported actions for the selected item.

**Specify every condition you want and order them from most to least important.** Drag the **⋮⋮** handle or use **↑ / ↓** to reorder conditions. Transformations have their own priority group above other conditions.

The **Prioritize placing all items** switch controls the first objectives:

| Switch | First objectives |
| --- | --- |
| On — default | Place more items first, then satisfy transformations. |
| Off | Satisfy transformations first, then place more items. |

Other conditions follow, then empty net cells, active stars, and bag bonuses. The panel also shows the current priority order.

Without conditions, BM tries to place items and improve the layout's overall metrics. **Explicitly add the transformations you want Craft to apply.**

### Solve: searching for a layout

**Solve** starts the search and displays the best layout found as work progresses. Below the board, you can see elapsed time, search counters, placed items, active stars, and useful bag links.

Simple inventories may take seconds; complex full backpacks can take several minutes or longer. Get some water or look out of the window — BM will keep working. Search time and results on Android may differ from those on a PC.

**Finding a layout and proving it optimal are different states.** While the search continues, BM may find a better solution. Stopping keeps the best result found so far, but does not establish its optimality.

During Solve, BM uses multiple worker threads. CPU usage and device temperature may increase. You can stop the search at any time with **Stop**.

### Craft: the next shop

After Solve finishes or is stopped, **Craft** applies the prepared transformations you requested through conditions, along with supported guaranteed changes upon entering the shop.

Consumed or disappearing items are removed, and guaranteed new items are added. If a result is random or its identity is unknown, BM does not choose it for the game: **add the item you actually received manually**.

After Craft, review the updated items and conditions. Run Solve again before the next transition.

### Android interface

The mobile version uses the same items, conditions, and priority rules. Buttons on the **left sidebar** open the item/bag and condition panels. Close a panel with **×** or the system Back action.

Item search opens a dedicated results area: type part of a name and tap the desired icon. Use **RU / ENG** to choose the interface language.

### Feedback

Found a bug? Open an **Issue** in this repository. Include your BM version, platform, item and bag lists, conditions in priority order, and a screenshot of the result. For Android crashes, an error log is also useful.

BM is an unofficial fan-made tool. Backpack Brawl, its artwork, and item names belong to their respective rights holders.

**Enjoy the game, and good luck with your runs!**
