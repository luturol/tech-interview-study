# Estrutura de Dados

Estrutura de dados são formas de organizar, gerencia e acessar os dados. A estrutura de dados define a forma como um sistema vai trabalhar para acessar aquele dados. Além do mais, as diversas formas de estrutura de dados possuem seus próprios propositos para facilitar e acelerar a nevegação entre eles.

## Quais os tipos de estrutura de dados?

Há vários tipos de estrutura de dados. Esses são alguns deles:

- [Array](/PT-BR/Programacao/EstruturaDeDados/array.md)
- [Pilha (Stack)](/PT-BR/Programacao/EstruturaDeDados/pilha.md)
- [Fila (Queue)](/PT-BR/Programacao/EstruturaDeDados/fila.md)
- Grafo
- [Árvore binária](/PT-BR/Programacao/EstruturaDeDados/arvorebinaria.md)
- Heap
- Priority Queue
- Dequeue
- [Listas Encadeadas (Linked List)](/PT-BR/Programacao/EstruturaDeDados/linkedlist.md)
- Matriz
- Array Multidemensional
- List
- Hash Table

## Perguntas e Respostas (FAQ)

_Algumas perguntas e respostas foram tiradas do ChatGPT, outras inventadas e outras de sites que estão nas referências_

1. O que é Estrutura de Dados?
1. O que é um array multidimensional?
1. Onde pode ser usado estrutura de dados?
1. **O que é uma lista encadeada (Linked List)?**

    É uma estrutura de dados de uma coleção de nodos e que cada nodo aponta para o próximo ou aponta para o anterior também. Linked List não possui memória alocada préviamente a ela, ela utiliza ponteiros para apontar para o próximo elemento, ou seja, de início o custo de memória é baixo e conforme cresce só vai adicionando o peso do novo elemento. As que apontam para o anterior e para o próximo são duplamente encadeadas. Isso facilita inserção e remoção de um nodo em qualquer posição da lista.

1. Quais são as vantagens de Linked List sobre Array? Em quais cenários utilizamos Array e quando utilizamos Linked List?
1. O que é uma Linked List duplamente encadeada?
1. O que são Estruturas de Dados dinâmicos?
1. O que é uma pilha?
1. O que é uma fila?
1. Para que pilha é usado?
1. O que é uma Queue Data Structure?
1. **O que é Dequeue?**

    Uma fila com duas saídas ou uma estrutura de dados em que os elementos possam ser adicionados tanto no final quando no inicio.

1. O que é Heap?
1. Quais as vantagens do Heap sobre uma Pilha?
1. **Qual a diferença entre uma Árvore Binárias (Binary Tree) e uma Árvore Binária de Pesquisa (BST)?**
    
    Uma Árvore Binária é uma árvore em que cada node possui no máximo dois filhos. Enquanto uma BST, ela é otimizada para facilitar a pesquisa entre os dados de uma árvore binária, organizando de forma que o nodo da esquerda sempre será menor que o nodo pai e o nodo da direita vai possuir um valor maior que o nodo Pai. Assim, a navegação para encontrar um dado é mais rápida e menos custosa sendo **O(log n)**. Porém, quando a BST está desequilibrada o custo fica **O(n)** porquê ela vai ter que navegar por todos os nodos até encontrar o valor.

# Referências

- [Data Structure Interview Questions and Answers [Top 46]](https://www.simplilearn.com/data-structure-interview-questions-and-answers-article)
- [Heap](https://pt.wikipedia.org/wiki/Heap)
- [Linked List](https://en.wikipedia.org/wiki/Linked_list)
- [Linked List Data Structure](https://www.geeksforgeeks.org/data-structures/linked-list/)