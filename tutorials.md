
## Funciones:  

En esta parte se muestran las funciones que se deben implementar para resolver el problema y otra que el usuario debe implementar para obtener la solución al problema dinámico.

Por ejemplo, primero debe implementarse la función que genera el estado dinámico: 

def dyn_generator(oper,state):
"""Genera la función de estado dinámico

Ejemplos: 
   >>> np.dot(oOper, state)
   np.array([0,0], [0,0]])

Args: 

   np.oOper(list): primer argumento
   np.state(list): segundo argumento 

Returns: 

   list: retorna el resultado de multiplicar `np.oOper` y `np.state`

   """
return np.dot(oOper, state)

    

    return dyn_generator 

def rk4(func, oper, state, h):
"""La función Runge Kutta"""
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

    def sum(a, b):
    """Sum of two floats.

    Examples:
        >>> sum(3.0, 4.0)
        7.0

    Args:
        a (float): First argument
        b (float): Second argument

    Returns:
        float: Returns the sum operation of `a` and `b`.

    """
    return a + b
