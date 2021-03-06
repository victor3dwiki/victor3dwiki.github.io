---
layout: page
title: LocalTalk
---

### Определения

* **AppleTalk** - протоколы, которые позволяют Macintosh'ам взаимодействовать с принтерами, файловыми серверами и другими устройствами.
* **LocalTalk** - Спецификация кабелей для 230.4 kbps AppleTalk.
* **Apple LocalTalk кабель** - витая пара, заключённая в экран из аллюминиевой фольги. Может быть заменён на отечественный микрофонный кабель KMM2х0.25 или даже на любой телефонный провод. 

### Как LocalTalk реализована на уровне разьемов/кабелей?

Первоначальный - "родной" - вариант сети LocalTalk использовал экранированную витую пару с MiniDIN-разъемами. Впоследствии наиболее популярной стал более дешевый Farallon PhoneNet. Коннектор PhoneNet --- это такая маленькая коробочка с хвостом (Din8), который вставляется в принтерный порт. На коробке две телефонных розетки. Для соединения используются телефонные 4-х жильные провода обжатые в RJ11 (для приема/передачи используются крайние контакты). Сеть представляет собой шину и не имеет разветвлений. В крайние (по топологии) коннекторы в свободные розетки вставляются согласующие резисторы. (я встречал коннекторы с переключателем вместо резистора). Сеть не может быть разбита на логические зоны. Количество нод 32 и, кажется, не более 4 принтеров. Коннекторы поставляются с 2-х метровым проводом и нагрузочным резистором. Дополнительное программное обеспечение не требуется.

В коробке импульсный трансформатор, пара керамических конденсаторов, 3 или 4 резистора (в TurboNet воткнуты еще светодиоды, моргающие во время работы) и два телефонных гнезда. Номинал резистора в терминаторе - 100 или 120 Ом. Максимальная длина шины - 300 метров (для Apple LocalTalk).

Если нужно соединить только два компа - можно безо всяких лишних коробок связать их принтерным кабелем.

### О топологии сети

Сеть может быть выполнена и на основе бэкбона (мы применили обыкновенную российскую телефонную "лапшу", кабель ТРП-0.25, как помнится) с ответвлениями к машинам. Эта топология в соответствии со стандартом Farallon.

При грамотной терминации соединённых между собой бэкбонов можно работать и на звездо-деревообразной топологии (это уже отход от стандарта). 

Нами успешно эксплуатировалась с 92 г. звездообразная сеть из 3-х бэкбонов с суммарной длиной более 300 м. Сеть была раскинута на 3 этажах офиса и имела несколько десятков Macintosh и штук 5 принтеров, подключаемых по желанию в любую из расположенных на стенах помещений розеток RJ-11. 

### Чем заменить PhoneNet-коннектор

Недавно в сети мне попалось сообщение (1990-го года ;-) ), в котором описывалась замена LocalTalk'овым адаптерам.

```
PIN NUMBERS ARE FOR MINI DIN 8
  
          CapNet Connector  (last update 8/21/90)
  
 J1                                                  J2
       5                                   C1 .1 uF
RCV(-) ----------------------------O----------][------O
                                   !
       8                           !       C2 .1 uF
RCV(+) --------------------------------O------][------O
                                   !   !            ^
                                   !   !           TO
       3                    10 ohm !   !         "PHONE"
TX(-)  -----------O-----------R3----   !          LINES
                  !                    !
       6          !         10 ohm     !
TX(+)  -----------------O-----R4--------
                  !     !
             1K   R     R  1K
                  1     2
                  !     !
       4          !     !
GND    -----------O------
```

**Parts list:**

Qty | Description | Item
--- | ----------- | ----
2 | R1,2 | 1K 1/8W RESISTORS
2 | R3,4 | 10 OHM 1/8W RESISTORS
2 | C1,2 | 0.1 uF THREE LAYER CERAMIC CAPS
1 | J1 | MINI-DIN 8 MALE CONNECTOR
1 | J2 | RJ-11 PHONE CONNECTOR
5 | WIRE | (NOT SHOWN) 22 GAUGE STRANDED WIRE 6"
