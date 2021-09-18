# ExampleOptimizationACS
В данной работе представлен пример оптимизации САУ.

---

## 1. Цель работы

Необходимо оценить эффективность решение задачи оптимизации коэффициентов с использованием инструментов Python, в частности:
- `numpy` — библиотека для работы с матрицами больших размерностей
- `scipy` — библиотека для выполнения научных и инженерных расчётов, в том числе:
    - `odeint` — функция численного интегрирования
    - `minimize` — функция минимизации функции вида y = y(x)
    - `Bounds` — функция создания класса Bounds для определения границ минимизации
    
---

## 2. Задача оптимального управления

Дана система:
![Динамическая система](/images/scheme.png)

Необходимо подобрать такие коэффициенты <img src="https://render.githubusercontent.com/render/math?math=\large{k_\omega, k_e}">, чтобы минимизировать следующий критерий:
<img src="https://render.githubusercontent.com/render/math?math=\center{\large{J = q \int_0^\infty (\omega_z (t) - \omega_{zld}})^2 dt"}>

Физический смысл критерия - площадь, ограниченная кривыми выходного сигнала и сигнала управления: 

![Критерий](/images/Kriteriy.png)

---

## 3. Решение

1. Создать функцию, описывающую поведение динамической системы
2. Создать функцию, возвращающую оценку критерия
3. Минимизировать функцию критерия и оценить время минимизации
4. Сделать выводы

<img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1">