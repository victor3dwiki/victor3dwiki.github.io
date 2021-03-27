---
layout: page
title: RUSKEY for QNX. Описание и руководство пользователя
---

#### ОСНОВНЫЕ ТРУДНОСТИ ПРИ РАБОТЕ С НАЦИОНАЛЬНЫМИ ШРИФТАМИ

Для того чтобы вы могли работать с национальным языком  в OS QNX на своем компьютере, вам необходимо выполнить следующие действия:

* Иметь фонты, включающие символы национального алфавита в определенной кодировке для того режима, который необходим, например: текстовый, Qwindows, Photon, X.
* Иметь файлы конфигурации клавиатуры (для OS QNX и отдельно для Photon или X).
* Программную поддержку для переключения между основной (например, Английской) и дополнительной (национальной) раскладкой клавиатуры, для обеспечения правильного ввода символов.
* Изменить конфигурацию системы для правильной работы с национальными шрифтами (например, для текстового режима необходимо дополнительно обеспечить их правильную загрузку).

### Функциональные возможности RUSKEY

Данный пакет предназначен для поддержки национальных алфавитов (по умолчанию русская кодировка КОИ-8) в операционной системе QNX (Текстовый режим, Qwindows, Photon).

Основные возможности:

* Переключение клавиатуры между основной и дополнительной раскладкой.
* Гибкая настройка комбинации клавиш для переключения.
* Индикация переключения звуком и цветом бордюра.
* Создание .kbd файла, с поддержкой национального языка, для photon.
* Создание конфигурационного файла для ruskey.
* Модификация конфигурационного файла .etc/config/sysinit.node в соответствии с настройками.
* Комплект фонтов для работы (текстовый режим, Qwindows и Photon).
* Дополнительная программа для модификации фонтов текстового режима.

### Комплект поставки
 
В комплект поставки входит инсталляционная дискета Ruskey, на которой находятся следующие файлы и директории:
 
ruskey/bin/be | программа редактирования текстовых фонтов
ruskey/bin/ruskey | программа переключения клавиатуры
ruskey/bin/ruset | программа настройки ruskey
ruskey/kbd/RUS | файл русской кодировки  клавиатуры
ruskey/cfont/ | директория с файлами текстовых фонтов
ruskey/fonts/ | директория с файлами фонтов для Qwindows
ruskey/phfont/ | директория с файлами фонтов для Photon

### Инсталляция
 
Для установки Ruskey на ваш компьютер необходимо дискету, поставленную вместе с этим руководством, вставить в дисковод флоппи дисков и выполнить команду:
 
```
# install [ /dev/fdn ]
```

где:  /dev/fdn - указывает дисковод, в который вставлен диск.
 
При выполнении установки будет отображена информация об установке (копируемые файлы, каталоги и т.д.). После загрузки, будет запущена программа ruset для выполнения конфигурации.

### Описание программ входящих в состав RUSKEY

#### Программа редактирования фонтов текстового режима

Для запуска программы необходимо набрать следующую программу:
 
```
#be name
```

где, name - имя файла содержащего текстовый фонт.
 
После запуска программы на экране появится следующее окно:

![1](/qnx/ruskey/1.png)

*PgUp, PgDown, Up, Down* - Движение по файлу,
 
*Enter* - Выбор байта для изменения (новое значение вводится в шестнадцатеричном виде),
 
*Space* - изменение отображение битов (цифровой или символьный),
 
*Esc* - выход из программы.

#### Программа переключения кодировок клавиатуры ruskey

Для обеспечения переключения на национальную клавиатуру необходимо запустить следующую программу:

``` 
#ruskey [options] &
```

где options:

-n number | установка цвета бордюра для дополнительной раскладки клавиатуры, где "number" значение цвета 0 до 15 (по умолчанию number = 9),
-bi | управление бордюром через int10,
-br | управление бордюром через регистры видео карты,
-u frequency | частота(Hz) тона для основной кодировки,
-r frequency | частота(Hz) тона для дополнительной кодировки,
-d duration | длительность(ms) тона,
-k key1[,key2] | комбинация одной или двух клавиш для переключения на основную(key1) и дополнительную(key2) кодировку, где "key": a-LeftAlt, A-RightAlt, s-LeftShift, S-RightShift, c-LeftCtrl, C-RightCtrl (по умолчанию RightShift+RightCtrl для обеих кодировок),
-o kbfile | полный путь и имя файла основной раскладки клавиатуры, обычно имя страны (по умолчанию /etc/config/kbd/USA),
-t kbfile | полный путь и имя файла дополнительной раскладки клавиатуры, обычно имя страны (по умолчанию /etc/config/kbd/RUS),
-v | вывод номера версии при запуске.
 
При запуске ruskey устанавливает свою настройку в следующем порядке: опции командной строки, файл конфигурации, значения по умолчанию.

#### Программа конфигурирования ruset

Для изменения конфигурации наберите команду:

``` 
#ruset
```

После запуска программы на экране появится следующее окно:

![2](/qnx/ruskey/2.png)

Для изменения параметров ruskey необходимо нажать клавишу (Alt+key или просто key) соответствующую изменяемому параметру, где:
 
*Speaker* | Вкл/Выкл звуковой сигнализации переключения кодировок,
*Duration(ms)* | Длительность звукового сигнала,
*Text Font* | Вызов окна настройки текстовых фонтов,
*Primary* | Вызов меню настройки параметров основной раскладки клавиатуры,
*Secondary* | Вызов меню настройки параметров дополнительной раскладки клавиатуры,
*Photon* | Вкл/Выкл конфигурации для Photon,
*Layout* | Изменение конфигурации клавиатуры для Photon,
*Save & Exit* | Сохранение конфигурации и выход из программы,
*Restore* | Восстановить настройки из файла конфигурации,
*Default* | Восстановить настройки по умолчанию,
*Cancel* | Выход из программы без сохранения.

##### Список фонтов текстового режима

![3](/qnx/ruskey/3.png)

При выборе в основном окне Text Font на экране появится следующее окно настройки фонтов, где:

*Num* - номер фонта,
 
*Font* - полный путь и имя файла фонта,
 
*Rows* - число строк на экране,
 
*Line* - высота фонта в пикселях.

*Add* - добавление в список  текстового фонта,
 
*Delete* - удаление фонта из списка,
 
*Done* - возврат в основное окно с сохранением изменений,
 
*Cancel* - возврат в основное окно без сохранения изменений.

Для изменения настроек фонта из списка необходимо выбрать изменяемый фонт, нажать на клавишу соответствующую изменяемому параметру и ввести новое значение.
 
При изменении имени файла или добавлении нового фонта на экране появляется следующее меню списка файлов.

![4](/qnx/ruskey/4.png)

Перемещение по списку с помощью курсорных клавиш, *Enter* - выбор фонта, *Esc* - отказ от выбора.

Для того чтобы изменить параметры переключения клавиатуры необходимо выбрать настройку Primary или Secondary, для изменения основной или дополнительной раскладки. 

![5](/qnx/ruskey/5.png)

![5a](/qnx/ruskey/5a.png)

После чего появится одно из следующих меню, где:

*Switch* - комбинация клавиш для переключения,
 
*Layout* - путь и имя файла описывающего раскладку клавиатуры для текстового режима,
 
*Edit* - редактирование файла раскладки клавиатуры,
 
*Sound* - частота звуковой сигнализации клавиатуры,
 
*Border* - индикация включения дополнительной раскладки цветом бордюра,
 
*Use INT10* - использование для изменения цвета бордюра int10, если не включено то используется аппаратное переключение,
 
*Color* - цвет бордюра.

#####  Настройки для Photon

![6](/qnx/ruskey/6.png)

Для включения поддержки Photon необходимо включить соответствующий режим в основном окне. При включенном режиме, выбор Layout (появится соответствующее меню) позволяет изменить настройки клавиатуры, где:

*New* - ввод нового пути и имени файла для сохранения конфигурации,
 
*File* - выбор пути и имени файла с настройкой,
 
*Edit* - настройка клавиатуры.

После выбора опции меню Edit на экране появится следующее окно, где:

*курсорные клавиши* - перемещение по кодам клавиш,
 
*Modifier (Tab)* - раскладка клавиатуры (primary, primary+shift, secondary, secondary+ shift),
 
*Value* - код символа клавиши,
 
*Done* - возврат в основное окно,
 
*Restore* - восстановление старых значений из файла,
 
*Default* - восстановление значений по умолчанию,
 
*Cancel* - выход из окна без сохранения.

![7](/qnx/ruskey/7.png)

##### Завершение работы

После окончания работы, при нажатии клавиш Alt+X или X (опция основного окна Save & Exit), будут внесены изменения в файлы /etc/config/sysinit.node, /etc/config/ruscfg.node, а также будет сгенерирован файл .kbd для Photon (если включена опция). После чего будет предложено перезагрузить компьютер для вступления всех изменений в силу.

![8](/qnx/ruskey/8.png)

*&copy; Николай Злобин*