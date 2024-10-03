## El método Runge Kutta 

Este es uno de los métodos más utilizados para resolver numéricamente problemas de ecuaciones diferenciales ordinarias con condiciones iniciales, este proporciona un pequeño margen de error con respecto a la solución real del problema. Resuelve ecuaciones diferenciales de la forma: 

$$
f(x,y,\frac{dy}{dx})= 0 
$$

Con 

$$
{y(x_0)}= {y_0}  
$$ 

El método es útil cuando la solución no puede hallarse mediante otros métodos. El método para este problema está dado por esta ecuación: 

$$
{y(i+1)= {y_i} + \frac{1}{6}[{k_1} + 2{k_2} + 2{k_3} + {k_4}] 
$$ 
