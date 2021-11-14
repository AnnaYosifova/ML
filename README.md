ВАРИАНТ 8

Упражнение 4.

При выполнении упражнения была построена модель дерева с обрезкой ветвей и оптимизирован её параметр с помощью перекрёстной проверки. Оптимальное значение параметра составило 149. Размер дерева не позволяет представить его в графическом виде полностью.

Также была построена модель методом Случайный лес. Оптимальные значения параметров этой модели:
- количество деревьев у лучшей модели: 50
- количество объясняющих у лучшей модели: 3
- точность модели: 0.82

Все модели показывают среднюю точность по показателю Acc, однако самой точной оказывается модель случайного леса. Прогноз на отложенные наблюдения для этой модели дал следующие результаты параметров:
- специфичность: 0.69
- чувствительность: 0.90
- совокупная точность: 0.83

Таким образом, можно говорить о хорошем качестве полученной модели.

Также сравним полученную совокупную точность на отложенных наблюдениях с точностью, полученной для модели, построенной на обучающей выборке с перекресной проверкой (0.83 и 0.82), они практически совпадают.







------------------------------------------------------------------------------------------------------------------------------------------
Упражнение 3.

При выплнении задания для снижения размерности пространства признаков используется метод частных наименьших квадратов (PLS) и строится логистическая регрессия с регуляризацией параметров (метод лассо). Точность всех моделей оценивается методом перекрёстной проверки по 10 блокам.

Вывод: Методом логистической регрессии со сжатием коэффициенты с L1-регуляризацией мы получили самую точную модель с Acc(лассо)=0,75. Для модели PLS: Acc(PLS)=0,73.







------------------------------------------------------------------------------------------------------------------------------------------
Упражнение 2.

Выводы:
Y = 48.77 + 1.172cyl_over_4 - 0.069displacement_cyl_over_4 - 0.024weight

При объясняющих переменных равных нулю Y равен 48.77.

Если дискретная переменная cyl_over_4 = 1, то Y увеличивается на 1.172, если же равно 0, тогда значение Y зависит только от непрерывных переменных. При увеличении displacement_cyl_over_4 на единицу, Y уменьшится на 0.069. При увеличении weight на единицу, Y уменьшится на 0.024.

Ошибка на отложенных наблюдениях составляет 18.6% от среднего значения Y







------------------------------------------------------------------------------------------------------------------------------------------
Упражнение 1.

Задание 1. 
Для модели с n_all = 60 ошибки на обучающей и тестовой выборках составиили 0.28 и 0.71 соответсвенно. Наименьшее значение MSE достигается при 28 степенях свободы, а ошибки на обучающей и тестовой выборках составили 0.60057 и 0.51634 соответсвенно.

Задание 2. 
Для модели с n_all = 300 ошибки на обучающей и тестовой выборках составиили 0.79 и 1.39 соответсвенно. Наименьшее значение MSE достигается при 11 степенях свободы, а ошибки на обучающей и тестовой выборках составили 0.95476 и 1.14492 соответсвенно.
Для модели с n_all = 250 ошибки на обучающей и тестовой выборках составиили 0.77 и 1.11 соответсвенно. Наименьшее значение MSE достигается при 12 степенях свободы, а ошибки на обучающей и тестовой выборках составили 0.948923 и 0.983036 соответсвенно.
Для модели с n_all = 200 ошибки на обучающей и тестовой выборках составиили 0.78 и 0.89 соответсвенно. Наименьшее значение MSE достигается при 13 степенях свободы, а ошибки на обучающей и тестовой выборках составили 1.001225 и 0.814976 соответсвенно.

Вывод:
При уменьшении значения n_all ошибки на тестовой выборке уменьшаются. Лучшей моделью является 3ья при n_all = 200, т.к. в ней ошибка на тестовой выборке минимальна. 
Чем больше наблюдений, через которые прошёл сплайн, тем точнее модель. Это говорит о переобучении. Лучшую модель следуют выбирать по минимуму на кривой MSE на тестовой выборке.
При слишком большом числе степеней свободы (как в задании 1 с 28 степенями свободы) происходит переобучение.
