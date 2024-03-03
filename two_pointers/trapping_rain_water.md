# Problema do Trapping Rain Water

O problema do "Trapping Rain Water" (ou "Retenção de Água da Chuva") é um problema clássico de programação que envolve determinar a quantidade de água que pode ser retida entre as paredes de uma paisagem representada por uma matriz de alturas. A água é retida apenas entre duas paredes, portanto, a capacidade de retenção depende da altura das paredes e da distância entre elas.

## Descrição do Problema

Dada uma matriz de alturas representando uma paisagem, onde cada elemento da matriz representa a altura de uma parede, o objetivo é determinar a quantidade total de água que pode ser retida entre as paredes.

## Solução em Python

```python
def trap(height):
    if not height:
        return 0    

    n = len(height)
    left_max = [0] * n
    right_max = [0] * n

    # Inicializa o valor máximo da esquerda
    left_max[0] = height[0]
    for i in range(1, n):
        left_max[i] = max(left_max[i - 1], height[i])

    # Inicializa o valor máximo da direita
    right_max[n - 1] = height[n - 1]
    for i in range(n - 2, -1, -1):
        right_max[i] = max(right_max[i + 1], height[i])

    # Calcula a quantidade total de água retida
    total_water = 0
    for i in range(n):
        total_water += min(left_max[i], right_max[i]) - height[i]

    return total_water


# Exemplo de uso
height = [0,1,0,2,1,0,1,3,2,1,2,1]
print(trap(height))  # Saída: 6
```

## Complexidade

- **Complexidade de Tempo**: O algoritmo passa pela matriz três vezes, portanto, a complexidade de tempo é O(n), onde n é o número de elementos na matriz.

- **Complexidade de Espaço**: O algoritmo usa duas listas adicionais, `left_max` e `right_max`, para armazenar as alturas máximas à esquerda e à direita de cada posição na matriz, respectivamente. Portanto, a complexidade de espaço é O(n), onde n é o número de elementos na matriz.