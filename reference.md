## Ejemplo del método Runge Kutta RK4:

import numpy as np
import matplotlib.pyplot as plt

# Se define la función f(t, y)
def f(t, y):
    return y - t**2 + 1

# Implementación  del método RK4
def runge_kutta_4_orden(f, y0, t0, t_end, dt):
    t_values = np.arange(t0, t_end + dt, dt)
    y_values = np.zeros(len(t_values))
    y_values[0] = y0

    for i in range(1, len(t_values)):
        t = t_values[i - 1]
        y = y_values[i - 1]
        
        k1 = dt * f(t, y)
        k2 = dt * f(t + dt / 2, y + k1 / 2)
        k3 = dt * f(t + dt / 2, y + k2 / 2)
        k4 = dt * f(t + dt, y + k3)

        y_values[i] = y + (k1 + 2 * k2 + 2 * k3 + k4) / 6   ## cálculo de pendiente

    return t_values, y_values

# Se dan los parámetros
y0 = 0.1     # condición de inicio 
t0 = 0       # tiempo de inicio
t_end = 5    # tiempo de finalización
dt = 0.6     # diferencial de tiempo 

# Ejecutamos el método
t_values, y_values = runge_kutta_4_orden(f, y0, t0, t_end, dt)

# Gráfica de los resultados
plt.plot(t_values, y_values, label='RK4', marker='o')
plt.title('Método de Runge-Kutta de cuarto orden')
plt.xlabel('t')
plt.ylabel('y')
plt.legend()
plt.grid()
plt.show()

