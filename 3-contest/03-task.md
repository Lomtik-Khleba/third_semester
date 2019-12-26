Submit a solution for up03-1-Саша пересчитывает биты 
Time limit:	1 s
Real time limit:	5 s
Memory limit:	64M
Stack limit:	8M
Problem up03-1: Саша пересчитывает биты
Напишите функцию bitcount со следующим прототипом на Си:

int bitcount(STYPE value);
Где STYPE — это некоторый целый знаковый тип. Кроме того, определен тип UTYPE — это некоторый целый беззнаковый тип того же размера, что и STYPE.

Функция возвращает число единичных бит, установленных в значении параметра value.

Используйте битовые операции для обработки параметра функции.

Отрицательные числа представляются в дополнительном коде.

Не используйте sizeof, не используйте константы, зависящие от размера типов. Не используйте 64-битные типы в процессе вычислений (если только STYPE не 64-битный).

Не используйте GCC __builtin функции.

Для того, чтобы определить типы STYPE и UTYPE в своей программе для тестирования, можно использовать typedef следующим образом:

typedef int STYPE;
typedef unsigned int UTYPE;
Соблюдайте рекомендованный стиль форматирования программ.

Submit a solution for up03-2-Леша считает чапельники
Time limit:	1 s
Real time limit:	5 s
Memory limit:	64M
Stack limit:	8M
Problem up03-2: Леша считает чапельники
В аргументах командной строки задаются 32-битные знаковые целые десятичные числа.

На стандартный поток вывода напечатайте два числа: сначала сумму положительных аргументов командной строки, затем сумму отрицательных аргументов командной строки. Если чисел соответствующей категории нет, выводите 0.

Пример запуска программы:

./solution 1 -3 5 -7 +12
Результат выполнения программы:

18
-10
Не забывайте выводить символ перехода на новую строку в конце вывода!

Submit a solution for up03-3-Камиль пересчитывает динары
Time limit:	1 s
Real time limit:	5 s
Memory limit:	64M
Stack limit:	8M
Problem up03-3: Камиль пересчитывает динары
В аргументах командной строки задаются вещественные числа:

Начальный курс некоторой валюты.
Изменения к курсу в процентах за один день. (ноль или более раз).
Курс валюты задается с четырьмя дробными цифрами, например, 69.5634. Изменения к курсу задаются в процентах и могут быть как положительными, так и отрицательными. Например, изменение курса -10.0 означает, что за день валюта подешевела на 10%, то есть, если в начале дня курс был 100.0000, то в конце дня он окажется 90.0000. Курс валюты в конце дня фиксируется с четырмя цифрами дробной части округлением по математическим правилам, все цифры дробной части после четвертой после округления отбрасываются.

Гарантируется, что ежедневные изменения курса больше -100 и меньше 100. Изменения курса задаются не более чем с четырьмя знаками дробной части. Курс валюты — положительный и не превосходит 10000 за все время.

На стандартный поток вывода напечатайте курс валюты в конце последнего дня, заданного в командной строке. Курс печатайте с четырьмя знаками дробной части.

Пример запуска программы:

./solution 100.0 -10.0 -5.5 1.0
Результат выполнения программы:

85.9005
Не забывайте выводить символ перехода на новую строку в конце вывода!


Submit a solution for up03-4-Максим пишет речь Игорю
Time limit:	1 s
Real time limit:	5 s
Memory limit:	64M
Stack limit:	8M
Problem up03-4: Максим пишет речь Игорю
На стандартном потоке ввода задается последовательность знаковых целых чисел. Целые числа записываются в десятичной форме со знаком + или - перед числом и разделяются одним или несколькими пробельными символами (то есть символами, для которых isspace возвращает истинное значение). Знак при положительном числе может опускаться.

На стандартный вывод напечатайте младшие 64 бита суммы этих чисел в виде знакового целого числа в десятичной записи.

Для чтения со стандартного ввода используйте системный вызов read с размером буфера для чтения 16 байт!

Не накапливайте в памяти считываемые символы.

Не забывайте выводить символ перехода на новую строку в конце вывода!

Глобальные (и static) переменные запрещены.


Submit a solution for up03-5-ССС (секретная связь Славы)
Time limit:	1 s
Real time limit:	5 s
Memory limit:	512M
Stack limit:	8M

Problem up03-5: ССС (секретная связь Славы)
На стандартном потоке ввода задаются строки текста неограниченной длины, содержащие целые числа, разделенные пробельными символами. Произвольное количество пробельных символов может присутствовать в начале и конце строки. Для каждой считанной строки на стандартный поток вывода выведите сумму чисел в этой строке текста.

Пробельный символ — это символ, для которого функция isspace возвращает истинное значение. Для построчного чтения используйте функцию getline2, корректная реализация которой будет доступна вашей программе при компиляции и тестировании. Однако в вашем исходном коде должен присутствовать корректный прототип этой функции. Во входных данных отсутствует байт 0.

Если считанная строка не содержит ничего, кроме пробельных символов, на стандартный поток вывода выведите значение 0x0bad1dea плюс порядковый номер данной считанной строки, отсчитываемый от 1. То есть если первая строка не содержит данных выведите число 195894763, если вторая строка не содержит данных - выведите 195894764 и так далее...

В случае пустого файла, то есть файла размера 0, ничего не выводите.

Если считанная строка содержит что-либо кроме последовательности чисел, например, буквы, на стандартный поток вывода выведите значение 0xbedabeda плюс порядковый номер данной считанной строки, отсчитываемый от 1. Число выводите как десятичное.

Если очередное считанное число непредставимо как знаковое 32-битное целое, замените его на порядковый номер этого числа в строке, отсчитываемый от 1, с сохранением знака числа. То есть, например, третье в строке число 11111111111111111111111111111111 должно быть заменено на число 3, а пятое в строке число -9999999999999999999999999 должно быть заменено на число -5.

Суммируйте 32-битные знаковые значения с игнорированием переполнения. То есть сумма чисел 2147483645 и 10 равна -2147483641. Результат суммирования всегда будет 32-битным знаковым числом.

Не забывайте освобождать память. Не забывайте выводить \n в конце каждой строки. Для преобразования строки в число используйте функции стандартной библиотеки Си. Не пишите свои функции преобразования! Не допускайте undefined behavior, в частности в стандартных библиотечных функциях. Не используйте явно 64-битные типы (long long, int64_t) и вещественные типы. Тип long использовать можно только для получения результата функции strtol.

Examples
Input
-100 25
     
50 -999999999999999999999999
23 5f
Output
-75
195894764
48
-1092960546
