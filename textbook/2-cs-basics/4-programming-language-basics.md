# Высокоуровневые языки программирования

<!-- TODO: Покупайте лень. Продам за бесценок -->

## Зачем они нужны?
Язык ассемблера - хорошая вещь. По крайне мере, если тебе надо написать что-нибудь не слишком сложное.
Однако, когда в программе много инструкций, запутаться в них проще простого.
Да и с памятью приходится работать вручную. А ещё необходимо учитывать особенности процессора и ОС,
под которые ты пишешь программу. Создавать реально сложные программы на языке
ассемблера можно, но это боль. На потакание процессору и операционной системе уходит
больше сил и времени, чем на написание логики самой программы. 

Мы уже абстрагировались от процессорных инструкций с помощью языка ассемблера. И от языка
ассемблера тоже абстрагируемся. Лучше один раз напрячься и создать инструмент, который
облегчит тебе работу в будущем, чем страдать, делая всё вручную.
То же самое можно сказать при помщи выражения "Лень - двигатель прогресса".

Программисты - люди ленивые, поэтому давным давно они хорошенько напряглись и создали высокоуровнеые
языки программирования. Их суть вот в чём: ты описываешь свою программу при помощи особого
"высокоуровневого" языка, представляющего из себя смесь человеческого и математического языков.
После этого специальная программа под названием "компилятор" переводит эту запись на язык
ассемблера, либо напрямую в процессорные инструкции.

<!-- 
TODO: Привести аналогию, чтобы описать различия между высокоуровнемыми языками и ассемблером.
Рассказать о том, компиляция - это необратимый процесс.
-->

Ещё один плюс высокоуровневых языков в том, что программы, написанные не них, как правило,
полностью отвязаны от конкретного процессора или операционной системы. Программисту достаточно
написать программу один раз, а 







<!--
## Что и зачем?
Программировать на ассемблере реально, но очень сложно и трудоёмко. Программисты - люди ленивые, им
вообще не хочется иметь дело с Бобом. Хочется общаться с компьютером на человеческом языке.
Для удовлетворения этой самой хотелки и были созданы высокоуровневые языки программирования.
По факту большинство языков скорее заимствуют всё из языка математики, а не из человеческого языка,
однако даже математический язык намного более понятен человеку, чем язык ассемблера.

Ещё один плюс высокоуровневых языков в том, что код, написанный на них, как правило, не привязан
к конкретной процессорной архитектуре или операционной системе. А это значит, что программу
достаточно написать всего лишь один раз, а её адаптацией под различные платформы будет
заниматься компилятор.

Команды, написанные на каком-то языке программирования, ещё надо перевести на понятный
процессору язык. Есть много разных способов сделать это. Каждый инструмент, выполняющий
подобную задачу, по-своему уникален, однако для простоты их делят на две категории:
1. Компиляторы. Они берут написанный человеком текст, *целиком* преобразовывают его в
набор инструкций для процессора и сохраняют их в файл для дальнейшего использования.
2. Интерпретаторы. Они преобразовывают написанный человеком код в инструкции по маленьким частям.
Чаще всего - по одной строчке. И, чаще всего, не сохраняют эти инструкции в файл, а сразу же
отправляют их процессору на исполнение.

Некоторые компиляторы преобразовывают код в инструкции для процессора напрямую. Некоторые
генерируют мнемоническую запись этих самых инструкций на языке ассемблера, а потом
отправляют ассемблеру, чтобы тот преобразовал их в инструкции. Это целиком и
полностью зависит от внутреннего устройства компилятора.

Компилятор, сам по себе, не выдаёт готовый исполняемый файл. Он производит так называемый
"объектный файл" - инструкции для процессора, в которых ещё не разрешены ссылки
на библиотечные функции. Чтобы разрешить их, объектный файл (Или сразу несколько
зависящих друг от друга объектных файлов) надо пропустить через компановщик.
Компановщик соберёт все эти файлы в единый исполняемый файл, а также разрешит
ссылки на динамические библиотеки. После этой процедуры, если она прошла успешно,
получится рабочий и готовый к запуску исполняемый файл.

## Основы (Почти) любого языка программирования

### Переменные


Переменные, команды, операторы, файлы с исходным кодом, ключевые слова, компиляторы и IDE,
как называть переменные, функции, комментарии
-->
