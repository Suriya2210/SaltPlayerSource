<img src="src/App GitHub Header.png" width="100%"/>

# Salt Player - музыкальный плеер, выбранный сотнями тысяч пользователей

Переводы：[中文](https://github.com/Moriafly/SaltPlayerSource/blob/main/README.md)，[Indonesia](https://github.com/Moriafly/SaltPlayerSource/tree/main/README-ID.md)

Salt Player - это приложение для воспроизведения музыки на платформе Android. Этот репозиторий используется для публикации обновлений новой версии Salt and Pepper Music, сбора отзывов и отправки уведомлений

## Скачивание

### Android

Salt Player *для Android* требуется система на Android 6.0 и выше, поддерживается архитектура arm-v8a и armeabi-v7a

| Поставщик | Источники | Версия релиза | ⚠️ Внимание |
|:--|:--|:--|:--|
| Moriafly | 1. [Github Release](https://github.com/Moriafly/SaltPlayerSource/releases) <br> 2. [CoolApk](https://www.coolapk.com/apk/284064) | Стандартная версия | Данная версия доступна только на архитектуре arm64-v8a |
| Google Play | [Google Play](https://play.google.com/store/apps/details?id=com.salt.music) | Пакеты Google Play | 1. Поддерживаются архитектуры arm64-v8a, armeabi-v7a <br> 2. Данная версия подписана и издана корпорацией Google и **НЕСОВМЕСТИМА** со стандартной версией <br> 3. Рекомендуется как канал выпуска стабильных версий, в отличие от стандартной версии |

Примечание: Пожалуйста, устанавливайте это приложение с офицального источника

#### Правила именования версий (файлов)

Например, имя apk-файла 10.5.0.2-release-2024091902-moriafly-arm64-v8a означает что...

| Термин | Означает | Имеется ввиду |
|:--|:--|:--|
| 10.5.0.2 | Номер версии | 10 - мажорное，5 минорное，0 - патч，2 - аварийный патч (Если патчей не было то цифра 0 опускается и пишется 10.4.4) |
| release | Тип версии | 1. release - Стабильная версия，beta - общедоступная бета-версия в которой возможны мелкие ошибки，alpha - тестовая версия в которой могут быть серьезные ошибки <br> 2. Иногда надпись release может опускаться, а alpha-версия может быть доступна публично, но это не означает, что в ней нет серьезных ошибок <br> 3. Стабильность сортируется так: release > beta > alpha (По субъективной оценке) |
| 2024091902 | Код версии | В Salt Player *для Android* код версии тоже имеет значение, например, 2024091902 указывает что это версия была выпущена 19 сентября 2024 года, а цифра 2 значит вторую сборку за день |
| moriafly | Код поставщика версии | Смотрите таблицу источников |
| arm64-v8a | Архитектура сборки | Смотрите таблицу источников |

### Windows

<img src="src/spw.png" height="128px"/>

Подробнее: [SPW](https://github.com/Moriafly/SPW)

## Библиотеки с открытым исходным кодом

[Salt UI](https://github.com/Moriafly/SaltUI)

## Локализация

Для получения дополнительной информации обратитесь [переводам](https://github.com/Moriafly/SaltPlayerSource/tree/main/translations)

## Адаптация к устройствам разных производиетелей

| Прошивка | Функции | Состояние | Примечания |
|:--|:--|:--|:--|
| Xiaomi MIUI/Hyper OS | Xiaomi Miaobang | 🟢 Поддерживается | 1. Для вызова функции Xiaomi Miaobang требуется MIUI 12 и выше. Нажмите кнопку в правом верхнем углу интерфейса воспроизведения Salt Player для смены устройства <br> 2. Эта функция основана на системных компонентах экранной проекции от Xiaomi. Если она недоступна, пожалуйста, проверьте, отключены ли соответствующие компоненты |
| | Внешний дисплей (например, Mix Flip) | 🟢 Поддерживается | |
| | MIUI/Hyper OS Виджеты | 🟠 Планируется | Ожидание релиза и доработки |
| Huawei HarmonyOS | Центр управления музыкой | 🔴 Не поддерживается | Документация по портированию под API не найдена |
| vivo OriginOS/Funtouch OS  | Умный автомобиль joviincar | 🟢 Поддерживается | 1. 29 августа 2024 года в версии Vivo Smart Car V4.0.7.3 была добавлена поддержка Salt Player. Благодарим пользователей, оставивших пожелания компании vivo и Vivo за их официальную поддержку <br> 2. Версия experience на данный момент не поддерживает отображение текстов песен doviincar (метод портирования неясен), тексты песен можно пока транслировать через автомобильный Bluetooth |
| | Hi-Fi | 🔵 Активируется вручную | 1. Введите через adb `settings put global game_support_hifi_list com.salt.music` <br> 2. Чтобы добавить Salt Player поддержку Hi-Fi, для этого зайдите в системные настройки > Звук и вибрации > включите Hi-Fi <br> 3. Чтобы узнать, поддерживает ли устройство функцию Hi-Fi, пожалуйста, перейдите на страницу продукта официального сайта Vivo, чтобы узнать подробнее |
| | Atomic Walkman | 🔴 Не поддерживается | Ничего не известно, документация по портированию под API не найдена <br> [#749](https://github.com/Moriafly/SaltPlayerSource/issues/749) |
| OPPO ColorOS | Fluid Cloud | 🟢 Поддерживается | Тестирование в оттенках серого будет постепенно внедряться с 4 ноября 2024 года благодаря официальной поддержке OPPO |
| Meizu Flyme | Текст песни в строке состояния | 🟢 Поддерживается | |
| | 灵动环 | 🔴 Не поддерживается | Ничего не известно, документация по портированию под API не найдена |

## Функции, которые больше не поддерживаются

| Функция | Дата | Подробнее |
|:--|:--|:--|
| DSD аудио（.dsf/.dff）| 2024 год | Рассматриваемый как устаревший формат, рекомендуется заменить его на FLAC <br> Смотрите подробности для получения дополнительной информации [Salt Player завершает работу поддержку формата DSD](https://github.com/Moriafly/SaltPlayerSource/blob/main/articles/240902_Deprecated_DSD.md) [(Перевод)](https://github.com/Moriafly/SaltPlayerSource/blob/main/articles/241123_Deprecated_DSD_russian_translate.md) |

## Контрибуторы

<a href="https://github.com/Moriafly/SaltPlayerSource/graphs/contributors">
    <img src="https://contrib.rocks/image?repo=Moriafly/SaltPlayerSource&columns=12" />
</a>

## Юридическая информация

Торговая марка Android принадлежит компании Google LLC

Логотип Android созданная Google воссоздан или изменен на основе оригинальных и общедоступных результатов интелектуальной собственности при условии соблюдения [Сreative Сommons](https://creativecommons.org/licenses/by/3.0/) и должны применяться условия лицензии версии 3.0

Salt Player является зарегистрированной торговой маркой компании Xunxun Technology (Shanghai) Co., Ltd. в Китайской Народной Республике

Для получения более подробной юридической информации, пожалуйста, ознакомьтесь с политикой программнного обеспечения и связанными с ним ресурсами сети интернет