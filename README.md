from math import *
import sys

x = float(input(" x -> "))
y = float(input(" y -> "))

msg = " f(x): tgh(y^3) -> 1, sh(y) -> 2, x^3 -> 3 "
f = int(input(msg + "\n -> ")) 
fx = None

if f == 1:
    fx = tanh(y**3)
elif f == 2:
    fx = sinh(y)
elif f == 3:
    fx = x**3
else:
    print("error")
    sys.exit()  

if x**3 > 5:
    B = log(fx)**3
    print("ln(f(x))^3:")
elif x**3 < 45:
    B = tan(x**3) + fx
    print("tan(x^3) + f(x):")
else:
    B = (y**2 - x**2)**(1/3) + fx
    print("(y^2 - x^2)^(1/3) + f(x):")

print("", B)
