# Problema do Best Time to Buy and Sell Stock

O problema do Best Time to Buy and Sell Stock consiste em encontrar o maior lucro possível ao comprar e vender ações em um mercado financeiro. Dado um array de preços, onde o índice representa os dias e o valor representa o preço da ação nesse dia, é necessário determinar o maior lucro que pode ser obtido ao comprar uma vez e vender depois.

## Descrição do Problema

Dado um array de preços de ações, encontrar o máximo lucro possível ao comprar uma vez e vender depois.

## Solução em Python

```python
def maxProfit(prices):
    if not prices:
        return 0
    
    min_price = prices[0]
    max_profit = 0
    
    for price in prices:
        min_price = min(min_price, price)
        max_profit = max(max_profit, price - min_price)
        
    return max_profit

# Exemplo de uso:
prices = [7, 1, 5, 3, 6, 4]
print(maxProfit(prices))  # Saída esperada: 5
```

## Complexidade

- **Complexidade de Tempo**: A solução percorre a lista de preços uma vez, realizando operações de comparação em cada elemento. Portanto, a complexidade de tempo é O(n), onde n é o número de elementos na lista de preços.

- **Complexidade de Espaço**: A solução utiliza uma quantidade constante de espaço, independentemente do tamanho da entrada. Portanto, a complexidade de espaço é O(1).