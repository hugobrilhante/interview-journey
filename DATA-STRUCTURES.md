# Estruturas de Dados Comuns em Entrevistas Técnicas

Nas entrevistas técnicas, os entrevistadores frequentemente testam o conhecimento e a compreensão dos candidatos sobre estruturas de dados fundamentais. Essas estruturas de dados são essenciais para resolver uma variedade de problemas de programação e são amplamente utilizadas na construção de algoritmos eficientes. Abaixo estão algumas das estruturas de dados comuns, juntamente com suas descrições aprimoradas, principais casos de uso e complexidades.

## 1. **Listas Ligadas (Linked Lists)**
   - **Descrição:** Uma lista ligada é uma estrutura de dados na qual os elementos, chamados de nós, são organizados em uma sequência linear. Cada nó contém dois componentes principais: um valor (ou dado) e um ponteiro que aponta para o próximo nó na sequência. 
   - **Principais Casos de Uso:**
     - Armazenamento de dados de forma dinâmica, sem a necessidade de uma alocação contígua de memória.
     - Implementação de pilhas (stacks) e filas (queues).
     - Útil quando a inserção e remoção de elementos são frequentes ou quando o tamanho da coleção pode variar dinamicamente.
   - **Complexidade:**
     - Inserção: O(1)
     - Remoção: O(1)
     - Acesso (por índice): O(n)

## 2. **Pilhas (Stacks)**
   - **Descrição:** Uma pilha é uma estrutura de dados linear que segue o princípio Last In, First Out (LIFO). Os elementos podem ser inseridos ou removidos apenas do topo da pilha.
   - **Principais Casos de Uso:**
     - Avaliação de expressões infixas, prefixas e pós-fixas.
     - Implementação de algoritmos de rastreamento de chamadas (call stack) e de desfazer (undo).
   - **Complexidade:**
     - Inserção: O(1)
     - Remoção: O(1)
     - Acesso: O(n)

## 3. **Filas (Queues)**
   - **Descrição:** Uma fila é uma estrutura de dados linear que segue o princípio First In, First Out (FIFO). Os elementos são inseridos no final da fila e removidos do início.
   - **Principais Casos de Uso:**
     - Processamento de tarefas em ordem de chegada.
     - Implementação de sistemas de cache e buffers.
     - Resolução de problemas de gerenciamento de recursos.
   - **Complexidade:**
     - Inserção: O(1)
     - Remoção: O(1)
     - Acesso: O(n)

## 4. **Árvores (Trees)**
   - **Descrição:** Uma árvore é uma estrutura de dados hierárquica composta por nós conectados por arestas. Cada nó tem um pai (exceto o nó raiz) e zero ou mais filhos.
   - **Principais Casos de Uso:**
     - Organização de dados hierarquicamente, como sistemas de arquivos em computadores.
     - Busca eficiente de dados em árvores binárias de busca.
     - Implementação de estruturas de dados avançadas, como árvores balanceadas.
   - **Complexidade (Árvore Binária Balanceada):**
     - Inserção: O(log n)
     - Busca: O(log n)
     - Remoção: O(log n)

## 5. **Grafos (Graphs)**
   - **Descrição:** Um grafo é uma estrutura de dados que consiste em um conjunto de vértices (ou nós) e um conjunto de arestas que conectam pares de vértices.
   - **Principais Casos de Uso:**
     - Modelagem de redes complexas, como redes sociais e sistemas de transporte.
     - Resolução de problemas de caminho mais curto, como o algoritmo de Dijkstra.
     - Análise de relações entre entidades em sistemas de recomendação.
   - **Complexidade (em geral):**
     - Inserção: O(1)
     - Busca: O(V + E) onde V é o número de vértices e E é o número de arestas.
     - Remoção: O(1)

## 6. **Tabelas de Hash (Hash Tables)**
   - **Descrição:** Uma tabela de hash é uma estrutura de dados que mapeia chaves para valores, onde os valores são armazenados de forma indexada pela função hash aplicada às chaves.
   - **Principais Casos de Uso:**
     - Busca eficiente em grandes conjuntos de dados.
     - Implementação de caches e tabelas de dispersão.
     - Garantia de unicidade de elementos em uma coleção.
   - **Complexidade (média):**
     - Inserção: O(1)
     - Busca: O(1)
     - Remoção: O(1)

## 7. **Arrays**
   - **Descrição:** Um array é uma estrutura de dados que armazena uma coleção de elementos de tamanho fixo, onde cada elemento é acessado por um índice único. Os elementos são armazenados em locais de memória contíguos e ocupam um espaço fixo na memória.
   - **Principais Casos de Uso:**
     - Armazenamento de dados quando o acesso aleatório é necessário, permitindo o acesso eficiente a qualquer elemento através do seu índice.
     - Implementação de estruturas de dados simples e eficientes, como pilhas e filas, quando o tamanho da coleção é conhecido antecipadamente.
     - Manipulação de matrizes e vetores multidimensionais para representar dados tabulares, imagens, entre outros.
   - **Complexidade:**
     - Inserção (no final): O(1)
     - Busca: O(n)
     - Remoção: O(n) (no pior caso)

Essas estruturas de dados são essenciais para qualquer desenvolvedor de software e compreendê-las bem é crucial para resolver problemas de programação complexos e eficientemente. Durante as entrevistas técnicas, os candidatos podem ser solicitados a implementar essas estruturas, analisar algoritmos que as utilizam ou resolver problemas usando-as.