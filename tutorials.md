
## Funciones:  

En esta parte se muestran las funciones que se deben implementar para resolver el problema y otra que el usuario debe implementar para obtener la solución al problema dinámico.

Por ejemplo, primero debe implementarse la función que genera el estado dinámico: 

def dyn_generator(oper, state):
"""Este es el docstring de la función"""
    oOper= np.array([[0, 1], [1, 0]])
    state= np.array([[1, 0], [0, 0]])
    dyn= np.dot(oOper, state) 

    return dyn_generator 

def rk4(func, oper, state, h):
"""Este es el docstring de la función"""
    t_values = np.arange(t0, t_end + dt, dt)
    y_values = np.zeros(len(t_values))
    y_values[0] = y0

Aquí el usuario debe introducir valores y realizar el for loop. 

for tt in range(times.size):
    # Guarde el valor de las entradas (0,0) y (1,1) en los arreglos que definimos
    # Obtenga estos valores de las entradas de yInit
    # Código aquí ->
    
    # Invoque rk4 operando sobre yInit
    # y devuelva el resultado a un nuevo yN
    # Código aquí ->
    
    # Ahora asignamos yN a yInit
    # De esta manera, en la siguiente iteración, el operador de esta iteración se convierte en el inicial
    # de la siguiente iteración
    yInit = yN
