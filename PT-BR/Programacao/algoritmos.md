# Algoritmos

São conjuntos de instruções feitas para solucionar um problema.

## Big O

É uma medida utilizada para calcular o tempo em que um algoritmo irá concluir com base nos seus dados de entrada e instruções. É utilizado para descrever o quanto levaria de tempo no pior caso, no médio e no melhor um algoritmo com base em sua entrada de dados.

- O(1) Tempo Constante

    Significa que o algoritmo não é afetado com o volume de dados.

- O(log n) Tempo logarítmico

    O desempenho melhor conforme o tamanho dos dados, mas não de forma proporcional.

- O(n) Tempo linear

    O tempo de execução cresce conforme o tamanho dos dados.

- O(n log n) Tempo log-linear

    É proporcional ao produto do tamanho de entrada e o logaritmo desse tamanho. Algoritmos que possuem essa complexidade são frequentemente muito performáticos.

- O(n²) Tempo quadrático

    O tempo de execução é proporcional ao quadrado da entrada.

- O(2^n) Tempo exponencial

    O desempenho do algoritmo cresce de maneira exponencial conforme o tamanho dos dados de entrada.
    
## Memória e espaço

# Perguntas e Respostas (FAQ)

_Algumas perguntas e respostas foram tiradas do ChatGPT, outras inventadas e outras de sites que estão nas referências_

1. **O que é um algoritmo de ordenação?**

    É um algoritmo especilizado em ordenar uma estrutura de dados para facilitar o seu consumo e manejo. Uma estrutura de dados ordenada facilita a busca dos elementos e a leitura.

1. **O que é complexidade de tempo de execução?**

    É a estipulação de quanto tempo levaria para concluir o algoritmo a partir da quantidade de dados e também instruções que são efetuadas no algoritmo. Instruções de loop podem afetar o tempo de execução positivamente ou negativamente.

1. **Explique o algoritmo "Bubble Sort".**

    O Bubble Sort é um algoritmo de ordenação utilizado para ordenar dados em uma estrutura de dados como Array ou outros tipos de Lista. Nele é feito um loop dentro de outro para fazer a troca das posições até ele estar perfeitamente ordenado. A ordenação é feita comparando os elementos de toda a lista com o elemento que será ordenado para encontrar a posição que ele deve ser colocado. A performance dele nos piores casos é ```O(n²)``` porque ele precisa percorrer toda a lista n vezes para um total de n elementos para poder ordenar ela e no caso ideal é ```O(n)``` porque a lista já está ordenada.

1. **Explique o algoritmo "Quick Sort".**

    É um algoritmo de ordenação em que é escolhido um elemento da lista, normalmente o do meio, e é feita uma divisão da lista para ordernar cada parte e depois juntar elas. Sendo necessário cuidar na hora da escolha do Pivot porque dependendo da escolha pode afetar a performance do algoritmo e no resultado. No pior dos casos a complexidade dele pode ser ```O(n²)```, mas no caso ideal é ```O(log n)```, onde n é o número de elementos.

1. **Qual é a complexidade do Quick Sort?**

    No pior dos casos a complexidade dele pode ser ```O(n²)```, mas no caso ideal é ```O(n log n)```, onde n é o número de elementos.

1. **Como o Merge Sort funciona?**

    É um algoritmo de ordenação que utiliza a recursão para fazer subdivisões dos elementos e ir ordenando eles até que todos estejam ordenados. No final as subdivisões ordenadas são mescladas para formar a lista ordenada. A complexidade do Merge Sort é ```O(n log n)```. É um algoritmo muito eficiente para ordenar estruturas de dados.

1. Explique o "Insertion Sort"?

    Insertion Sort é um algoritmo de ordenação utilizado para ordenar um elemento no momento em que será inserido na lista. Ele funcionar ordenando uma pequena sequência de dados por vez. Ele divide a lista em dois, elementos ordenados e elementos não ordenados, e compara os não ordenados com os ordenados para poder inserir na posição adequada. O processo é repetido até que todos os dados estejam ordenados. No pior dos casos a complexidade é O(n²) e na melhor é O(n). Ele é eficiente para pequenas listas quase ordenadas.