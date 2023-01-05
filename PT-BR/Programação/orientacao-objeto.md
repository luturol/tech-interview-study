# Orientação a objetos (POO)

Programação orientada a objetos é um paradigma da programação baseada no conceito de objetos.

## O que é?

É a ideia de classificar o código em uma abstração envolvendo objetos para deixar mais concreto e organizado o código. Você organiza o mundo real como uma coleção de objetos.

## 4 pilares da orientação a objetos

- Abstração

    É a habilidade de se concentrar somente no conceito e não no que realmente faz. Pode ser uma classe ou uma função em que pelo nome dela você entende o contexto e não precisa ler o código para entender como funciona. Exemplo: quando você tem um carro e pede para ligar, você sabe que o carro pode ligar, não entende como faz, mas sabe o que irá resultar.

- Encapsulamento

    Significa que cada classe deve controlar o próprio estado, ou seja, determinar quais são as propriedades ou métodos públicos e quais serão privados para evitar que outra parte do código altere o estado dela. Exemplo: quando temos um carro, não podemos alterar o carro para ter somente duas rodas porque um carro funciona somente com 4 rodas. Nesse caso, deixamos os métodos e a propriedade que alteram o número de rodas como privados e o método que nos retorna a quantidade de rodas como público.

- Herança

    Significa que quem herdar dela terá as mesmas características dela. É agrupar conjuntos de classes que possuem características semelhantes e propósitos parecidos umas com as outras e traçar uma relação entre elas para evitar código repetido. Exemplo: no cenário em que temos umas monstros como Dragão, Orc, Beholder. Todas possuem propriedades como lista de magia, nome, vida, mana e funções como gritar, atacar, lançar mágia. Queremos facilitar e evitar que todas possuam código repetido e que possam haver diferenças também na escrita desses códigos que possam criar bugs no nosso código. Para isso, podemos dizer que todas herdam de uma classe chamada Monstro que possui todas definições que diz que aquela implementação é um monstro. Adicionamos na classe Monstro as propriedades lista de magia, nome, vida, mana e funções como gritar, atacar e lançar magia e fazemos com que todas herdem de Monstro. Agora, se quisermos criar um novo monstro, exemplo goblin, é só criar uma nova classe que herda de Monstro e o nosso código continuará a funcionar.

- Polimorfismo

    Significa fazer um objeto se comportar de formas diferentes trazendo o mesmo resultado. Exemplo: Um carro e uma moto podem herdar de uma classe chamada automóvel. Os dois aceleram ou dois fazem a mesma coisa (locomover alguém de um lugar para outro), porém, de formas diferentes.

## Referências

- [Orientação a objetos, Wikipédia](https://pt.wikipedia.org/wiki/Orienta%C3%A7%C3%A3o_a_objetos)
- [POO: o que é programação orientada a objetos?, Alura](https://www.alura.com.br/artigos/poo-programacao-orientada-a-objetos)
- [Os quatro pilares da Programação Orientada a Objetos - com JavaScript, FreeCodeCamp](https://www.freecodecamp.org/portuguese/news/os-quatro-pilares-da-programacao-orientada-a-objetos-com-javascript/)
- [O que significa Orientação a objetos ?, Macoratti.net](https://www.macoratti.net/oo_conc2.htm)