Python\_Numerical\_Integration\_Tool
================

Ejemplo de uso

``` python
import sys
sys.path.append(<path_to_integral_tool>)
from numeric_integration.integration import Integrate
```

### Define una función

``` python
def double_gaussian(x, y): # puede ser cualquier función
    return exp(-(x ** 2 + y ** 2))
```

### Build an Integrate object

``` python
integral = Integrate(double_gaussian)
```

### Calculate the integral

``` python
result = integral.double_integral([[-500, 500], [-500, 500]], precision=3)
```

### Show the result and the accuracy

``` python
print("The result is", result)
```

### Calculate the error range

``` python
print("\nThe accuracy of this result is", integral.error)
```
