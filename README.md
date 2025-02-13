# reto9
### Algoritmos de Ordenamiento (Clasificación)

Los algoritmos de ordenamiento son técnicas utilizadas para organizar elementos de una lista o arreglo en un orden específico, ya sea ascendente o descendente. Son esenciales en informática, ya que mejoran la eficiencia de operaciones como búsquedas y análisis de datos.

### Bubble Sort (Ordenamiento de Burbuja)

El Bubble Sort es un algoritmo sencillo que ordena una lista comparando e intercambiando elementos adyacentes si están en el orden incorrecto. Su nombre proviene de la forma en que los elementos más grandes "suben" hacia su posición correcta, similar a burbujas.

#### Pasos del Bubble Sort:

1. **Comparación e intercambio**: Se recorre la lista comparando pares de elementos adyacentes.
   - Si el elemento actual es mayor que el siguiente, se intercambian.

2. **Repetición**: Este proceso se repite hasta que no se necesitan más intercambios, lo que indica que la lista está ordenada.

#### Ejemplo:

Para el arreglo `[5, 3, 8, 4, 2]`:

- **Primer pasada**:
  - `[3, 5, 4, 2, 8]` (el 8 llega al final).

- **Segunda pasada**:
  - `[3, 4, 2, 5, 8]` (el 5 se coloca en su lugar).

- **Tercer pasada**:
  - `[3, 2, 4, 5, 8]` (el 4 se coloca en su lugar).

- **Cuarta pasada**:
  - `[2, 3, 4, 5, 8]` (lista ordenada).

#### Implementación en Python (Optimizada):

```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        swapped = False
        for j in range(0, n - i - 1):
            if arr[j] > arr[j + 1]:
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
                swapped = True
        if not swapped:
            break
    return arr
```

#### Ventajas y Desventajas:

- **✅ Simple**: Es fácil de entender e implementar.
- **✅ Estable**: Mantiene el orden de elementos iguales.
- **✅ Eficiente en pequeños conjuntos de datos o listas casi ordenadas**.
- **❌ Ineficiente**: No es recomendado para grandes volúmenes de datos debido a su complejidad O(n²).

#### Variante: Cocktail Shaker Sort

El Cocktail Shaker Sort es una variante que recorre la lista en ambas direcciones, pero mantiene la complejidad O(n²).

### Conclusión

El Bubble Sort es ideal para fines educativos o listas pequeñas. Sin embargo, en aplicaciones prácticas con grandes volúmenes de datos, se prefieren algoritmos más eficientes como Quick Sort o Merge Sort.
