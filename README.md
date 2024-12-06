from math import *
import sys

# Ввод данных
x = float(input(" x -> "))
y = float(input(" y -> "))

# Выбор вида функции f(x)
msg = " f(x): tgh(y^3) -> 1, sh(y) -> 2, x^3 -> 3 "
f = int(input(msg + "\n -> "))  # Изменено на int для корректной работы match
fx = None

# Конструкция проверки соответствия структуре шаблона
if f == 1:
    fx = tanh(y**3)
elif f == 2:
    fx = sinh(y)
elif f == 3:
    fx = x**3
else:
    print("error")
    sys.exit()  # Досрочное завершение программы

# Проверка условий и вычисление значения выражения
if x**3 > 5:
    B = log(fx)**3
    print(": ln(f(x))^3")
elif x**3 < 45:
    B = tan(x**3) + fx
    print(": tan(x^3) + f(x)")
else:
    B = (y**2 - x**2)**(1/3) + fx
    print(": (y^2 - x^2)^(1/3) + f(x)")

# Вывод значения выражения
print(":", B)
