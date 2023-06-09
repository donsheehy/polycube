# Example Polycubes

There are several builtin methods for generating specific polycubes.

```python {cmd}
from polycube import *

square_4 = square(4)
tri_9 = triangle(9)
tet_6 = tet(6)
pyr_8 = pyr(8)

```

## stl generation

The `scad_to_stl` method in the `polycube.stl` module can be used to produce a `.stl` file suitable for 3D printing.

```python {cmd}
from polycube import *
from polycube.stl import scad_to_stl

scad_to_stl(tet(6), 'tet6')
```

## More general polycubes

```python {cmd}
from polycube import *
from polycube.stl import scad_to_stl

general_polycube = polycube([[0,0,0],
                             [0,0,1],
                             [0,1,0],
                             [1,0,0],
                             [2,0,0],
                             [3,0,0],
                             [3,1,0]])

scad_to_stl(general_polycube, 'general_polycube')
```
