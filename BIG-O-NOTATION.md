# Introdução à Notação Big O

A notação Big O é uma convenção matemática utilizada na ciência da computação para descrever o comportamento assintótico de algoritmos ou funções. Ela descreve a complexidade de um algoritmo em termos do tamanho da entrada.

Em termos simples, a notação Big O informa como o tempo de execução ou os requisitos de espaço de um algoritmo aumentam à medida que o tamanho da entrada aumenta. Isso auxilia na compreensão da eficiência de um algoritmo em termos de tempo e espaço.

## Pontos-chave

- **Definição**: A notação Big O descreve o limite superior do tempo de execução ou da complexidade espacial de um algoritmo no pior caso, frequentemente representado como O(f(n)), onde 'n' é o tamanho da entrada e 'f(n)' é uma função que descreve o desempenho do algoritmo em termos de 'n'.

- **Análise assintótica**: A notação Big O foca no comportamento de um algoritmo à medida que o tamanho da entrada se aproxima do infinito. Ela desconsidera fatores constantes e termos de ordem inferior, pois tornam-se insignificantes para entradas grandes.

- **Tipos de complexidade**:

  | Complexidade | Descrição                |
  |--------------|--------------------------|
  | O(1)         | Complexidade constante   |
  | O(log n)     | Complexidade logarítmica |
  | O(n)         | Complexidade linear      |
  | O(n log n)   | Complexidade log-linear  |
  | O(n^2)       | Complexidade quadrática  |
  | O(2^n)       | Complexidade exponencial |
  | O(n!)        | Complexidade fatorial    |

- **Melhor, pior e casos médios**: A notação Big O geralmente descreve o pior caso, mas também pode ser usada para descrever os melhores ou casos médios, denotados como notações Ω (Omega) e Θ (Theta), respectivamente. No entanto, a notação Big O é a mais comumente utilizada.

- **Comparação de algoritmos**: A notação Big O é útil para comparar a eficiência de diferentes algoritmos. Um algoritmo com uma ordem de complexidade menor (por exemplo, O(n) versus O(n^2)) geralmente terá melhor desempenho para entradas grandes.

Compreender e analisar algoritmos utilizando a notação Big O é crucial para projetar algoritmos eficientes e tomar decisões informadas sobre a seleção de algoritmos com base nos requisitos do problema e nas restrições de entrada.

---

### Exemplos de Código:

#### Complexidade: O(1) - Complexidade constante

```python
def get_first_element(arr):
    return arr[0]  # Complexidade de tempo: O(1), Complexidade de espaço: O(1)
```

#### Complexidade: O(log n) - Complexidade logarítmica

```python
def binary_search(arr, target):
    low, high = 0, len(arr) - 1
    while low <= high:
        mid = (low + high) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            low = mid + 1
        else:
            high = mid - 1
    return -1  # Complexidade de tempo: O(log n), Complexidade de espaço: O(1)
```

#### Complexidade: O(n) - Complexidade linear

```python
def find_max(arr):
    max_element = arr[0]
    for element in arr[1:]:
        if element > max_element:
            max_element = element
    return max_element  # Complexidade de tempo: O(n), Complexidade de espaço: O(1)
```

#### Complexidade: O(n log n) - Complexidade log-linear

```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    mid = len(arr) // 2
    left_half = merge_sort(arr[:mid])
    right_half = merge_sort(arr[mid:])
    return merge(left_half, right_half)

def merge(left, right):
    result = []
    while left and right:
        if left[0] < right[0]:
            result.append(left.pop(0))
        else:
            result.append(right.pop(0))
    return result + left + right  # Complexidade de tempo: O(n log n), Complexidade de espaço: O(n)
```

#### Complexidade: O(n^2) - Complexidade quadrática

```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n - 1):
        min_index = i
        for j in range(i + 1, n):
            if arr[j] < arr[min_index]:
                min_index = j
        arr[i], arr[min_index] = arr[min_index], arr[i]
    return arr  # Complexidade de tempo: O(n^2), Complexidade de espaço: O(1)
```

#### Complexidade: O(2^n) - Complexidade exponencial

```python
def generate_subsets(s):
    subsets = [[]]
    for elem in s:
        new_subsets = []
        for curr in subsets:
            new_subset = curr.copy()
            new_subset.append(elem)
            new_subsets.append(new_subset)
        subsets.extend(new_subsets)
    return subsets  # Complexidade de tempo: O(2^n), Complexidade de espaço: O(2^n)
```

#### Complexidade: O(n!) - Complexidade fatorial

```python
import itertools

def generate_permutations(s):
    return list(itertools.permutations(s))  # Complexidade de tempo: O(n!), Complexidade de espaço: O(n!)
```

---

## Tabela de Complexidade de Tempo e Espaço para Algoritmos Conhecidos

| Algoritmo                  | Complexidade de Tempo (pior caso) | Complexidade de Espaço (pior caso) | Comentários                                                                                                        |
|----------------------------|-----------------------------------|------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| Binary Search              | O(log n)                          | O(1)                               | Algoritmo de busca binária para arrays ordenados.                                                                  |
| Merge Sort                 | O(n log n)                        | O(n)                               | Algoritmo de ordenação eficiente baseado em comparação.                                                            |
| Quick Sort                 | O(n^2)                            | O(log n) (in-place)                | Algoritmo de ordenação eficiente in-place com complexidade média de tempo O(n log n).                              |
| Breadth-first Search (BFS) | O(V + E)                          | O(V)                               | Algoritmo de travessia de gráfico, onde V é o número de vértices e E é o número de arestas.                        |
| Depth-first Search (DFS)   | O(V + E)                          | O(V) (recursivo)                   | Algoritmo de travessia de gráfico, onde V é o número de vértices e E é o número de arestas.                        |
| Dijkstra's Algorithm       | O((V + E) log V)                  | O(V)                               | Algoritmo do caminho mais curto, onde V é o número de vértices e E é o número de arestas.                          |
| A* Search Algorithm        | O(b^d)                            | O(b^d)                             | Algoritmo de busca heurística, onde b é o fator de ramificação e d é a profundidade da solução na árvore de busca. |

Compreender as complexidades de tempo e espaço desses algoritmos pode ajudar na seleção do algoritmo apropriado para resolver diferentes tipos de problemas de forma eficiente.