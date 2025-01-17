# Ассемблер
Как тут уже говорилось, инструкции для Боба представлены в памяти как
наборы последовательно идущих чисел. Бобу крайне легко их понимать и исполнять.
Он, всё-таки, не человек, а кусок кремния, который магическим образом
заставили думать. А вот для неподготовленного человека инструкции будут выглядеть
совершенно бессмысленно. Попробуй посмотреть на последовательность чисел и понять,
что она значит - ничего не получится. Однако инструкции не могут взяться
из воздуха, их должен написать программист, а программист - это человек.

Следовательно, каждому программисту необходимо наизусть выучить все эти инструкции и самому
стать как Боб. Запомнить длину, назначение и структуру каждой инструкции, чтобы
научиться их писать. Стать ходячим биологическим компьютером... Сотни разных инструкций...
Можно с ума сойти... Но программистам хорошо платят, поэтому это стоит того... Так ведь???

<!-- TODO: добавить арт с уставшим программистом, а на экране компа куча циферок
"День 12, наконец написал Hello, world!" -->

Спойлер: это не стоит того. Чтобы было понятнее, рассмотрим аналогию с шахматной нотацией.
Нужна она для того, чтобы компактно описывать последовательности ходов (почти как последовательности
инструкций!). Например, для дебюта четырёх коней - довольно распространённой тактики
начальной стадии игры - ходы описываются следующим образом с помощью шахматной нотации:

```
1. e4  e5
2. Kf3 Kc6
3. Kc3 Kf6
```

Если человек серьёзно занимается шахматами, то ему это будет понятно.
А для всех остальных такая запись будет всего лишь страшно выглядящей кучей букв и цифр.
То же самое можно сказать про процессорные инструкции в сыром виде. Только с ними ситуация
ещё хуже, потому что шахматная нотация хотя бы была создана для людей, а вот про процессорные
инструкции подобного сказать нельзя.

Однако эту же самую последовательность ходов можно описать человеческим языком:

```
Ход 1. Белая пешка ходит с e2 на e4, чёрная пешка ходит с e7 на e5
Ход 2. Белый конь ходит с g1 на f3, чёрный конь ходит с b8 на c6
Ход 3. Второй белый конь ходит с b1 на c3, второй чёрный конь ходит с g8 на f6
```

Информация передаётся абсолютно та же самая, только теперь её сможет понять любой человек,
знающий правила шахмат. Да, получается более громоздко - за всё приходится платить свою цену.
Но если ваша цель - сделать информацию более доступной, то эта самая цена полностью оправдана.

Процессорные инструкции тоже можно записать в более громоздком, но понятном человеку
виде. А потом использовать программу, переводящую их на язык, понятный процессору.

## Представляем вашему вниманию ассемблер и язык ассемблера
Ассемблер - это программа, переводящая процессорные инструкции, написанные на понятном человеку языке
(языке ассемблера) в формат, понятный процессору. Написание инструкций на языке ассемблера
регулируется жёсткими правилами, потому что иначе ассемблер не сможет их перевести. Это ведь всего
лишь довольно простенькая и тупенькая программа, с настоящим человеческим языком она неспособна
работать из-за того, насколько он сложен.

Приведём игрушечный пример, чтобы понять, с чем мы имеем дело. Возьмём последовательность
инструкций для процессора семейства x86. Тут четыре инструкции, закодированные при помощи тринадцати
байтов:

```
184 57 5 0 0 187 228 0 0 72 1 216 80
```

Это настоящие инструкции, понятные процессору. Человеку же не понятно нихрена, и разобраться в таком будет
крайне сложно, даже если постараться. Однако можно то же самое записать на языке ассемблера:

```asm
mov  rax,1337
mov  rbx,228
add  rax, rbx
push rax
```

Скорее всего тебе, читатель, такая запись тоже непонятна. Но она явно намного лучше, чем просто
последовательность чисел. Ниже приводится её расшифровка на русский язык. Там упоминается слово "регистр".
Регистр - это небольшая ячейка памяти внутри самого процессора. Регистров в процессоре несколько десятков.
Чтобы различать их, в языке ассемблера каждому регистру даётся имя, например, rax, rbx и rcx. В прошлой
главе говорилось, что Боб может запоминать числа в своей голове - это как раз и была метафора для регистров
процессора.

Расшифровка:
1. `mov rax,1337` - Помести в регистр rax число 1337
2. `mov rbx,228` - Помести в регистр rbx число 228
3. `add rax,rbx` - Прибавь к значению регистра rax значение регистра rbx
4. `push rax` - Запиши получившееся значение регистра rax в память компьютера

В результате всех этих действий в памяти компьютера окажется число, равное 1337+228 = 1565.

С помощью ассемблера понятную человеку запись инструкций можно преобразовать в настоящие инструкции для процессора.
В обратную сторону такую операцию тоже можно провернуть. Программа, делающая это, называется "дизассемблер".
