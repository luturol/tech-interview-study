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

Quer dizer que quando temos uma classe que já possui um comportamento definido, é melhor extender essa classe e adicionar esse novo comportamento numa nova classe para evitar criar um bug onde já está funcionando. Esse princípio funciona muito bem com o Dependency Inversion Principle, pois nele você define que uma classe recebe uma interface ou classe abstrata no método, adicione a interface como dependência desse método ou classe e no final só implemente uma nova interface com o novo comportamento. Isso evita criação de novos bugs e torna os testes mais fáceis.

## Liskov Substitution Principle

"Derived classes must be substitutable for their base classes"
