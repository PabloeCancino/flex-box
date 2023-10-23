```Mermaid
---
Método de Steffenson
---
graph TD
    %% Definición de variables
    Start["Inicio: Método de Steffenson"]
    A["INPUT x_0, TOL, N"]
    B["Set n=1"]
    C{"While n <= N"}
    D["Set x_1=g(x_0)"]
    E["Set x_2=g(x_1)"]
    F["Set x=x_0-(x_1-x_0)^2/(x_2-2*x_1+x_0)"]
    G{"If |x-x_0| < TOL"}
    H["Print(x) and STOP"]
    I["Set n++"]
    J["Set x_0=x"]
    K["Print('El método ha fallado después de N iteraciones') "]
    End["Fin"]

    %% Definición del flujograma
    Start --> A
    A --> B
    B --> C
    C -- SI --> D
    D --> E
    E --> F
    F --> G
    G -- NO --> I
    I --> J
    J --> C
    C -- NO --> K
    K --> End

    G -- SI --> H
    H --> End
```
