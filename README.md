# RETO #3
Para este reto tenemos como objetivo plantear el algoritmo para obtener los números primos hasta n, usando pseudocódigo y diagramas de flujo.

Primero comenzaremos con pseudocodigo y luego continuaremos con el diagrama de flujo:

## PSEUDOCODIGO

Inicio
    Escribir "Ingrese un número entero n:"
    Leer n

    Para i desde 2 hasta n hacer
        primo ← Verdadero
        Para j desde 2 hasta i - 1 hacer
            Si i mod j = 0 Entonces
                primo ← Falso
                Salir del ciclo
            FinSi
        FinPara

        Si primo = Verdadero Entonces
            Escribir i
        FinSi
    FinPara
    Fin

## DIAGRAMA DE FLUJO

```mermaid
flowchart TD
    A[Inicio] --> B[Leer n]
    B --> C{i = 2 hasta n}
    C --> D[primo = Verdadero]
    D --> E{j = 2 hasta i-1}
    E -->|Sí| F{i mod j == 0}
    F -->|Sí| G[primo = Falso]
    G --> H[Salir del ciclo interno]
    F -->|No| E
    H --> I{primo == Verdadero}
    E -->|No| I
    I -->|Sí| J[Imprimir i]
    I -->|No| K[Incrementar i]
    J --> K
    K --> C
    C -->|No| L[Fin]
```
