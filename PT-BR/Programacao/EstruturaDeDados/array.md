# Array

Array é uma estrutura de dados de uma coleção pré determinada de dados com um tamanho específico. O aceso nele é através do index de cada posição. Benefícios: Tamanho fixo, acesso por index e todos os dados são do mesmo tipo.


## Como implementar

Normalmente Arrays são criados já informando o tipo e o seu tamanho final.

```csharp
int[] array = new int[5];
```

Para inicializar um array já com valores:

```csharp
int[] array = new int[5] { 1, 2, 3, 4, 5 };
```


Para acessar um array:

```csharp
int[] array = new int[5] { 1, 2, 3, 4, 5 };

var valor = array[0];
```

Normalmente os arrays começam na posição 0 e vão até ```Lenght - 1```. Prestar muita atenção nisso ao realizar uma operação com Array.

# Perguntas e Respostas (FAQ)

_Algumas perguntas e respostas foram tiradas do ChatGPT, outras inventadas e outras de sites que estão nas referências_

1. **Qual a diferença entre um Array e uma Lista?**

    Um array possui um tamanho fixo, enquanto uma lista pode crescer ou diminuir conforme o número de dados aumenta/diminui. Listas são mais eficazes para inserção e remoção. Arrays são melhores para o acesso do dados.

1. **Como você declara e inicializa um array na sua linguagem de programação favorita?**

    Em C# inicializamos um array da seguinte forma: ```int[] array = new int[5];```. Podendo também atribuir valores já na inicialização da seguinte forma: ```int[] array = new { 1, 2 ,3 ,4, 5};```.

1. **Como você acessa o primeiro elemento de um Array?**

    É possível acessar através do index dele, 0. 
    
    ```array[0]```

1. **O que é um Array multidimensional?**

    É um array de arrays, ou seja, um array que possui no dado mais um array de outro dado. Exemplo: ```int[,] array2D = new int[2, 4];``` um array de duas dimensões em que a primeira dimensão possui tamanho 2 e a segunda tamanho 4, ou de forma mais simples, duas linhas com 4 colunas.

    | Valor 1 | Valor 2 | Valor 3 | Valor 4
    | -------- | ------- | -------- | ------- |
    | 1 | 2 | 3 | 4 |
    | 1 | 2 | 3 | 4 |

1. **Qual é a complexidade para acessar um elemento num Array?**

    O(1) porque pelo index tu já recebe de volta o elemento, não é preciso iterar sobre ele então o custo para acessar ele é constante.

1. **Quais são as vantagens e desvantanges de usar arrays estáticos em comapração com arrays dinâmicos (Array List)?**

    Arrays estáticos possui um tamanho fixo então o custo de memória será sempre o mesmo e o acesso rápido. Já arrays dinâmicos podem crescer e diminuir conforme o número de dados aumenta/diminui o que pode ser menos eficiente em questão de memória.

1. **Como inverter um array?**

    Você precisa trocar as posições dos elementos do array. É possível utilizando um loop de for para iterar sobre o array do forma decrescente e ir adicionando no começo do array os elementos até todos serem preenchidos.

    ```csharp
    int[] arr = { 1, 2, 3, 4, 5 };
    int[] reversed = new int[arr.Length];

    for(int i = arr.Length - 1; i >= 0; i--){
    		reversed[arr.Length - i - 1] = arr[i];
    }
    ```

1. **O que é um array circular?**

    É um array em que o próximo elemento depois do último é o primeiro elemento, ou seja, um ciclo. É útil quando é necessário ficar percorrendo a lista de forma ciclica.

# Referências

- [C# - Conceitos - Apresentando Arrays](https://macoratti.net/10/05/c_arrays.htm)