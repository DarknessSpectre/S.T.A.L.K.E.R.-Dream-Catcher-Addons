# Аддоны для «Ловца снов Remastered»

Четыре независимых аддона для Dream Catcher Remastered RC3 на IX-Ray 1.3.4. В сборнике есть правки интерфейса, моделей и торговли, очистка старых прицелов и облегчённая погода Мёртвого города.

## Что делает каждый аддон

- **Del_OldAddons** убирает устаревшие прицелы из размещения предметов на локациях, отдельных ящиков, тайников, ассортимента двух торговцев и меню ручного спавна.
- **Eazy_Economy** позволяет торговцам и обычным сталкерам выкупать даже полностью изношенные предметы из их списков скупки. У Косаря в обеих ступенях обычной торговли выплаты игроку повышены на 25%, а цены покупки у него снижены на 25%.
- **FixPack** возвращает исходный HUD и меняет карты в ПДА, заменяет модель Шеппарда, вертолёты и модели двух прицелов, обновляет текстуры ряда мутантов и меняет расход выносливости. В меню **Настройки → Игра** добавляет переключатель **Эффект линзы шлема**. В боевом скрипте зомбированных добавляет проверки на случай, когда пропадает цель или событие опасности.
- **Optimization_DeadCity** задаёт Мёртвому городу два пасмурных погодных цикла с дымкой и базовой дальностью отрисовки 120 м. В обоих циклах отключены прямой солнечный свет и солнечные теневые каскады R4. Для дневного и ночного неба используются отдельные кубические текстуры и карты отражений.

## Установка

Скопируйте нужные папки из `ixr_addons/` репозитория в `ixr_addons/` в корне игры. Файл `addon.init` должен лежать в корне каждого аддона. Для полного применения изменений спавна и экономики начните новую игру.

## Карта файлов

Пути указаны относительно папки соответствующего аддона. В каждом аддоне `addon.init` служит манифестом IX-Ray, а `info.txt` содержит описание. Звёздочки объединяют связанные файлы, двойная звёздочка обозначает содержимое папки с подпапками.

### Del_OldAddons

| Файл | За что отвечает |
| --- | --- |
| `spawns/all.spawn` | Размещение предметов на локациях и содержимое отдельных ящиков. |
| `configs/misc/secret_jupiter.ltx`, `configs/misc/secret_zaton.ltx` | Списки предметов в тайниках. |
| `configs/misc/trade/trade_jup_b202_stalker_barmen.ltx`, `configs/misc/trade/trade_zat_b30_stalker_trader.ltx` | Ассортимент двух торговцев. |
| `scripts/spawn_items.script`, `scripts/ui_si.script` | Списки ручного спавна предметов. |

### Eazy_Economy

Все файлы ниже находятся в `configs/misc/trade/` и накладывают изменения через DLTX.

| Файл | Торговый профиль |
| --- | --- |
| `mod_dec_a3_musicboy_trade_economy_update.ltx` | Косарь. Порог состояния и множители цен в двух ступенях. |
| `mod_dec_a3_lixoi_trade_economy_update.ltx` | Лихой. |
| `mod_dec_a3_medic_trade_economy_update.ltx` | Профессор Сорокин. |
| `mod_dec_a3_small_barmen_trade_economy_update.ltx` | Кощей. |
| `mod_lim_stalker_medic_trade_economy_update.ltx` | Айболит. |
| `mod_lim_stalker_trader_trade_economy_update.ltx` | Мажор. |
| `mod_rad_t3_haron_trade_economy_update.ltx` | Харон. |
| `mod_rad_t3_hromoi_trade_economy_update.ltx` | Хромой. |
| `mod_rad_vlasov_medic_trade_economy_update.ltx` | Доктор Власов. |
| `mod_yan_6_4_slepoi_trade_economy_update.ltx` | Слепой. |
| `mod_yan_6_4_sokolov_trade_economy_update.ltx` | Соколов. |
| `mod_yan_elisei_trade_economy_update.ltx` | Елисей. |
| `mod_yan_ronin_trade_economy_update.ltx` | Ронин. |
| `mod_trade_barmen_all_economy_update.ltx` | Общий профиль барменов. |
| `mod_trade_generic_economy_update.ltx` | Обычный обмен со сталкерами. |

### FixPack

| Файл или группа | За что отвечает |
| --- | --- |
| `configs/creatures/actor.ltx` | Расход и восстановление выносливости при движении и беге. |
| `configs/ui/maingame.xml`, `configs/ui/maingame_16.xml`, `textures/ui/ui_actor_hint_wnd.dds` | Игровой HUD и оформление подсказок. |
| `configs/ui/zone_map.xml`, `configs/ui/zone_map_16.xml`, `textures/ui/ui_global_map.dds`, `textures/map/map_*.dds` | Интерфейс карты, глобальная карта и текстуры отдельных локаций. |
| `scripts/dc_helmet_lens.script`, `configs/ui/dc_helmet_lens.xml`, `configs/text/rus/ui_st_dc_helmet_lens.xml` | Переключатель визора, его раскладка и русский текст. Точка входа указана в `addon.init`. |
| `scripts/xr_combat_zombied.script` | Проверки цели, последней известной позиции врага и события опасности в боевом поведении зомбированных. |
| `meshes/actors/mod_npc/shepard_life.ogf`, `textures/act/newmilitary/**` | Модель Шеппарда, текстуры экипировки и лиц, служебные `.thm` и исходник `eyeball_bump.tga`. |
| `meshes/dynamics/vehicles/mi24/veh_mi24_u_01*.ogf` | Модели вертолёта Ми-24. |
| `meshes/dynamics/weapons/wpn_upgrade/wpn_scope*.ogf` | Модели обычного прицела и SUSAT, включая варианты LOD. |
| `textures/act/act_*_bump.dds`, `textures/act/act_*_fur*.dds` | Карты нормалей и текстуры шерсти ряда мутантов. |
| `textures/act/act_rus_legs_spec.dds` | Карта отражающей способности текстуры экипировки `rus_legs`. |

### Optimization_DeadCity

| Файл | За что отвечает |
| --- | --- |
| `configs/mod_game_dc_distance.ltx` | Назначает погодные циклы локации `dead_city`. |
| `configs/environment/mod_dynamic_weather_graphs_dc_distance.ltx` | Задаёт выбор между двумя погодными циклами. |
| `configs/environment/weathers/dc_dynamic_dc_distance_clear_alt_clean.ltx` | Более светлый пасмурный цикл. |
| `configs/environment/weathers/dc_dynamic_dc_distance_cloudy_black_clean.ltx` | Более тёмный цикл с плотной дымкой. |
| `textures/sky/deadcity_opt_cloudy.dds`, `textures/sky/deadcity_opt_cloudy#small.dds` | Дневное небо и куб отражений. |
| `textures/sky/deadcity_opt_night.dds`, `textures/sky/deadcity_opt_night#small.dds` | Ночное небо и куб отражений. |
| `textures/intro/intro_dead_city_1.dds` | Изображение экрана загрузки Мёртвого города. |
