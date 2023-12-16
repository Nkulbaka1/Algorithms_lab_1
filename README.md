# Лабораторная работа №1
В ходе лабораторной работы были реализованы 3 алгоритма поиска элемента в матрице (Ladder search, Binary search, Exponencial + Ladder search) и две генерации данных для матрицы (линейная и экспоненциальная). Код был написан на С++ и запускался в Visual Studio. Файлы для запуска находятся в папке Algorithms_Lab_1.

Код содержит ряд фунций:
~~~
first_matrix_generation() - заполнение матрицы согласно линейной генерации данных

second_matrix_generation() - заполнение матрицы согласно экспоненциальной генерации данных 

ladder_search() - лестничный поиск. O(M+N)

binary_search() - бинарный поиск. O(MlogN)

exp_lad_search() - экспоненциальный поиск. O(M(LogN - LogM + 1))

ladder_search_test() - тесты лестничного поиска

binary_search_test() - тесты бинарного поиска

exp_lad_search_test() - тесты экспоненциального поиска с лестничной оптимизацией
~~~
**Генерация данных выбирается вручную при запуске кода.**

Результаты запусков и графики можно найти по ссылке: https://docs.google.com/spreadsheets/d/1dbpvRcXpxakb9oCqXL3uV4Sf6HTs1GVF_ioQH_Y4RfE/edit?usp=sharing

## Выводы
**Первая генерация данных**

Самым эффективным оказался алгоритм Ladder search, т. к. является наиболее стабильным по времени работы. Пока М < 256 Binary search заметно быстрее, но при М >= 256 алгоритм Ladder search является наиболее быстрым.

Binary search отлично показывает себя на матрицах с M < 256. На этом промежутке он явяется лидером по скорости.

Экспоненциальный поиск с лестничной оптимизацией имеет график производительности, схожий с графиком бинарного поиска, но работает медленне примерно в 2 раза.

**Вторая генерация данных**

На экспоненциальной генерации данных лидером всё ещё остаётся лестничный поиск(снова наиболее стабилен), а бинарный поиск показывает лучшую производительность при M < 256.

Линейный поиск и экспоненциальный поиск работают быстрее на экспоненциальной генерации данных, а бинарный - медленнее.
