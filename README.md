# image_recognition
=======================================================
Автор работы: Овчинников Дмитрий, 3 поток, кафедра СП, группа №327
В данной работе реализована база задания, многоклассовая классификация, пирамида дескрипторов и цветовые признаки.
Для упрощения реализации и уменьшения памяти, цветовые признаки у меня сохраняются не в конце дескриптора, а в конце каждой клетки
(т.е. после того как программа посчитает дескриптор одной клетки, она записывает цветовые признаки в соотвтетствии с описанным 
в файле task2.pdf алгоритмом, подробнее см. /src/task2.cpp, функция getHOG() строки 131-146 ) 
Параметры для дескриптора, а именно размер сетки и количество сегментов разделяющих угол 2Pi описаны вначале файла task2.cpp (строчки 15-21)
Они подобраны вручную для улучшения результата на конкретной выборке.
Пирамида дескрипторов реализована многократным (3 раза) применением функции getHOG(), она улучшила результат на ~ 7-8% на обеих выборках.

Стандартный скрипт проверки compare.py работает неверно, если predictions.txt лежит в одной директории с этим скриптом 
(добавляется "/" к каждой строчке файла predictions.txt), поэтому скрипт проверки пришлось переделать(см. compare.py).

В архиве модель обучена на выборке multiclass.
Обучение другой модели происходит аналогично шаблону, описанному в task2.pdf (к архиву он НЕ прилагается). 

=======================================================

За дополнительной информацией обращаться ovchinnikov.d94@gmail.com

