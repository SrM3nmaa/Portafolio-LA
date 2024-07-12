import numpy as np
import matplotlib.pyplot as plt

def solve_quadratic(a, b, c):
    # Comprobamos que "a" sea mayor que 0 y que "4ac" sea mayor que "b^2"
    if a <= 0 or 4*a*c <= b**2:
        print("La ecuación no cumple las condiciones necesarias.")
        return None, None

    discriminant = np.sqrt(b**2 - 4*a*c) # Calculamos el discriminante

    # Calculamos las dos soluciones de la ecuación de segundo grado
    x1 = (-b + discriminant) / (2*a)
    x2 = (-b - discriminant) / (2*a)

    return x1, x2

def plot_quadratic(a, b, c):
    x = np.linspace(-10, 10, 400) # Creamos un rango de valores para x
    y = a*x**2 + b*x + c # Calculamos los valores de y usando la ecuación cuadrática

    plt.figure(figsize=(8, 6))
    plt.plot(x, y, label=f'{a}x^2 + {b}x + {c}') # Graficamos la función cuadrática
    plt.axhline(0, color='black', linewidth=0.5) # Línea horizontal en y=0
    plt.axvline(0, color='black', linewidth=0.5) # Línea vertical en x=0
    plt.xlabel('x')
    plt.ylabel('y')
    plt.title('Gráfico de la función cuadrática')
    plt.legend()
    plt.grid(True)
    plt.show()

# Coeficientes de la ecuación cuadrática
a = 1
b = -3
c = 2

# Resolvemos la ecuación cuadrática
x1, x2 = solve_quadratic(a, b, c)

# Imprimimos las soluciones
print("Solución x1:", x1)
print("Solución x2:", x2)

# Graficamos la función cuadrática
plot_quadratic(a, b, c)
