# Стан джерел графіків відключень

Telegram-бот [@grafik_ua_bot](https://t.me/grafik_ua_bot) із сервера в Україні опитує джерела
графіків кожного оператора кожні кілька хвилин і публікує тут, що бачить: щойно стан змінюється і
щонайменше щогодини. Звідси бейджі для [ukraine-energy-monitor](https://github.com/fastiuk/ukraine-energy-monitor).
Стан на **31.10.2026 19:17** (Київ).

**Джерело офіційне:** ✅ — сайт, API чи Telegram-канал самого оператора (на який веде його сайт),
❌ — неофіційне дзеркало. **Джерело:** звідки береться графік, з посиланням, де адреса незмінна;
«резерв» — запасні джерела по черзі. **Стан** стає «не працює», коли жодне джерело не відповідає
~30 хв (тоді ж бот пише адміну); **Відповідь джерел** — що кожне відповіло востаннє, тож там може
бути разова помилка й при «працює».

| Область | Оператор | Стан | Джерело офіційне | Джерело | Відповідь джерел |
|---|---|---|---|---|---|
| м. Київ | ДТЕК Київські електромережі | працює | ✅ · резерв ❌ | [API](https://app.yasno.ua/api/blackout-service/public/shutdowns/regions/25/dsos/902/planned-outages) · резерв: [неофіційне дзеркало](https://github.com/Baskerville42/outage-data-ua) | YASNO 25/902: ok \(31.10\); outage-data-ua kyiv: ok \(30.10\) |
| АР Крим | — | тимчасово окупована — буде після повернення додому | — | — | Тимчасово окупована територія. Буде доступно після повернення додому 🇺🇦 |
| Київська | ДТЕК Київські регіональні електромережі | працює | ❌ | [неофіційне дзеркало](https://github.com/Baskerville42/outage-data-ua) | outage-data-ua kyiv-region: ok \(31.10, 01.11\) |
| Вінницька | Вінницяобленерго | не працює | ✅ | [сторінка сайту](https://www.voe.com.ua/disconnection/detailed) | Vinnytsia: error \(FetchError: GET https\://www\.voe.com.ua/disconnection/detailed/autocomplete/read\_city?…: HTTP 404\) |
| Волинська | Волиньобленерго | працює | ✅ | [картинка з сайту](https://api-voe-poweron.inneti.net/api/options?option_key%5B%5D=pw_gpv_image_today&option_key%5B%5D=pw_gpv_image_tomorrow) | Volyn: ok \(nothing published\) |
| Дніпропетровська · ДТЕК | ДТЕК Дніпровські електромережі | працює | ✅ · резерв ✅ ❌ | [API](https://app.yasno.ua/api/blackout-service/public/shutdowns/regions/3/dsos/301/planned-outages) · резерв: [сторінка сайту](https://www.dtek-dnem.com.ua/ua/shutdowns), [неофіційне дзеркало](https://github.com/Baskerville42/outage-data-ua) | YASNO 3/301: ok \(31.10, 01.11\) |
| Дніпропетровська · ЦЕК | Центральна енергетична компанія \(ЦЕК\) | працює | ✅ · резерв ✅ ❌ | [API](https://app.yasno.ua/api/blackout-service/public/shutdowns/regions/3/dsos/303/planned-outages) · резерв: [сторінка сайту](https://www.dtek-dnem.com.ua/ua/shutdowns), [неофіційне дзеркало](https://github.com/Baskerville42/outage-data-ua) | YASNO 3/303: ok \(31.10, 01.11\) |
| Донецька | ДТЕК Донецькі електромережі | не публікує | — | — | Оператор не публікує графіків погодинних відключень. |
| Житомирська | Житомиробленерго | працює | ✅ | [сторінка сайту](https://www.ztoe.com.ua/unhooking-search.php) | Zhytomyr: ok \(31.10, 01.11\) |
| Закарпатська | Закарпаттяобленерго | працює | ✅ | [картинка з сайту](https://api-outage-zakarpat-energy.inneti.net/api/options?option_key%5B%5D=pw_gpv_image_today&option_key%5B%5D=pw_gpv_image_tomorrow) | Zakarpattia: ok \(nothing published\) |
| Запорізька | Запоріжжяобленерго | працює | ✅ | [сторінка сайту](https://www.zoe.com.ua/outage/) | Zaporizhzhia: ok \(nothing published\) |
| Івано-Франківська | Прикарпаттяобленерго | працює | ✅ | API | Prykarpattia: ok \(nothing published\) |
| Кіровоградська | Кіровоградобленерго | працює | ✅ · резерв ✅ | [Telegram-канал](https://t.me/s/SvitloKropyvnytskyiMisto) · резерв: [Telegram-канал](https://t.me/s/SvitloOleksandriyskohoRaionu) | Telegram SvitloKropyvnytskyiMisto: ok \(nothing published\) |
| Луганська | Луганське енергетичне об'єднання | не публікує | — | — | Оператор не публікує графіків погодинних відключень. |
| Львівська | Львівобленерго | працює | ✅ | [API](https://api.loe.lviv.ua/api/menus?page=1&type=photo-grafic) | Loe: ok \(nothing published\) |
| Миколаївська | Миколаївобленерго | працює | ✅ | [API](https://off.energy.mk.ua/api/v2/schedule/active) | Mykolaiv: ok \(nothing published\) |
| Одеська | ДТЕК Одеські електромережі | працює | ✅ · резерв ❌ | [сторінка сайту](https://www.dtek-oem.com.ua/ua/shutdowns) · резерв: [неофіційне дзеркало](https://github.com/Baskerville42/outage-data-ua) | DTEK OEM: ok \(nothing published\); outage-data-ua odesa: ok \(nothing published\) |
| Полтавська | Полтаваобленерго | працює | ✅ | [сторінка сайту](https://www.poe.pl.ua/disconnection/power-outages/) | Poltava: ok \(31.10, 01.11\) |
| Рівненська | Рівнеобленерго | працює | ✅ | [сторінка сайту](https://www.roe.vsei.ua/disconnections) | Rivne: ok \(nothing published\) |
| Сумська | Сумиобленерго | працює | ✅ | [картинка з сайту](https://www.soe.com.ua/press-service/news) | SumyNews: ok \(nothing published\) |
| Тернопільська | Тернопільобленерго | працює | ✅ | API | Тернопільобленерго показує графік лише для конкретної адреси, тож бот підписує за адресою: знайдіть свій будинок, і бот стежитиме за чергою цієї адреси. |
| Харківська | Харківобленерго | працює | ✅ | [сторінка сайту](https://oblenergo.kharkiv.ua/uk/rss.xml) | Kharkiv: ok \(nothing published\) |
| Херсонська | Херсонобленерго | недоступно | — | — | Херсонобленерго не публікує графіків відкрито — лише в особистому кабінеті. |
| Хмельницька | Хмельницькобленерго | працює | ✅ | [картинка з сайту](https://hoe.com.ua/post/novini-kompaniji) | Khmelnytskyi: ok \(nothing published\) |
| Черкаська | Черкасиобленерго | працює | ✅ | [API](https://www.cherkasyoblenergo.com/api/v1/posts/main?lang=uk&limit=200) | Cherkasy: ok \(31.10, 01.11\) |
| Чернівецька | Чернівціобленерго | працює | ✅ | [сторінка сайту](https://oblenergo.cv.ua/shutdowns/) | Chernivtsi: ok \(nothing published\) |
| Чернігівська | Чернігівобленерго | працює | ✅ | [Telegram-канал](https://t.me/s/chernigivoblenergo) | Chernihiv: ok \(31.10\) |
| м. Севастополь | — | тимчасово окупована — буде після повернення додому | — | — | Тимчасово окупована територія. Буде доступно після повернення додому 🇺🇦 |

Машиночитно: [`summary.json`](summary.json). Бейдж кожного оператора — `<оператор>.svg`, а також
`<оператор>.json` у форматі [shields.io endpoint](https://shields.io/badges/endpoint-badge).
