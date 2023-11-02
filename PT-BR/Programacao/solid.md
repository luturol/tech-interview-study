# S.O.L.I.D.

É um acrônimo sobre 5 princípios da orientação a objetos.

S - Single Responsability Principle (Princípio da responsabilidade única)

O - Open-Close Principle (Princípio Aberto-Fechado)

L - Liskov Substitution Principle (Princípio da substituição de Liskov)

I - Interface Segregation Principle (Princípio da segregração da interface)

D - Dependency Inversion Principle (Princípio da inversão de dependência)


## Single Responsability Principle

"A class should have one, and only one, reason to change".

Quando criamos uma classe, essa classe deve ter apenas um motivo e executar somente uma tarefa. O motivo desse princípio é para que você não sobrecarrega a classe com responsabilidades que não são dela. Assim, você faz classes menores, que possuem responsabilidades definidas, fáceis de entender e testar.

## Open-Close Principle

"You should be able to extend a class behaviour, without modifying it"

Quer dizer que quando temos uma classe que já possui um comportamento definido, é melhor extender essa classe e adicionar esse novo comportamento numa nova classe para evitar criar um bug onde já está funcionando. Ou seja, usar interface e herança para implementar novas funcionalidades sem afetar o código já existente.

Esse princípio funciona muito bem com o Dependency Inversion Principle, pois nele você define que uma classe recebe uma interface ou classe abstrata como parâmetro no método. Adicione a interface como dependência desse método/classe e por último, só implemente uma nova classe a partir da interface com o novo comportamento. Isso evita criação de novos bugs e torna os testes mais fáceis e simples.

## Liskov Substitution Principle

"Derived classes must be substitutable for their base classes"

Você deve poder substituir uma classe que deriva de uma abstração/interface/heranca pela classe base dela. Isso significa que o seu código não deve depender da abstração/implementação da classe e sim poder receber qualquer uma e continuar funcionando. 

Exemplo: quando temos uma classe Orc que herda de mosntro e queremos que a nossa classe Player ataque algum monstro, o método Atacar não deve ter a assinatura ``public void Atacar(Orc orc)`` e sim ``public void Atacar(Monstro monstro)``. O código deve funcionar independente de qual abstração você passar para ele.

## Interface Segregation Principle

"Make fine grained interfaces that are client specific."

Você deve criar interfaces específicas e únicas para resolver um problema. Não é uma boa prática criar uma classe que resolva mais de um problema, isso torna o código difícil de entender e complica a manutenção.

É possível implementar mais de uma interface numa classe.

## Dependency Inversion Principle

"Depend on abstractions, not on concretions."

Classes devem ter como dependência abstrações e não classes concretas. Isso facilita que uma classe possa receber uma nova implementação da interface e que ela não vai parar de funcionar por causa disso, tornando o código mais flexível.


## Referencias

- [The Principles of OOD](http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod)
- [SOLID](https://pt.wikipedia.org/wiki/SOLID)
- [O que é SOLID: O guia completo para você entender os 5 princípios da POO](https://medium.com/desenvolvendo-com-paixao/o-que-%C3%A9-solid-o-guia-completo-para-voc%C3%AA-entender-os-5-princ%C3%ADpios-da-poo-2b937b3fc530)
- [O que é SOLID e quais são seus princípios?](https://luby.com.br/desenvolvimento/software/conceitos/o-que-e-solid/)
