# REST API (Representational State Transfer Application Programming Interface)

É um conjunto de princípios e restrições para o design de serviços web.

## Principais Caracteristicas

- Stateless

    Cada requisição deve conter toda a informação necessária para processar a solicitação. E o servidor não deve armazenar informações sobre o estado do cliente entre requisições, o que diminui a lógica do servidor por não precisar armazenar o estado do cliente.

- Interface Uniforme (URI - Uniform Resource Identifiers)

    Os recursos são identificados a partir da sua URI e manipulados por um conjunto de ações definidas como GET, PUT, POST, DELETE e PATCH.

- Representações

    Os recursos podem ser em diversas representações como: JSON e XML.

- Construído sobre o protocolo HTTP

    Utiliza o protocolo HTTP para fazer a comunicação entre as aplicações e serviços. Então cada recurso é acessado a partir da sua URI e seu HTTP método. O uso do HTTP facilita a integração com diversos recursos disponíveis atualmente.

- Stateless Comunication

    As comunicações com o servidor não possuem estado, então cada requisição possui somente a necessária informação para a solicitação e retorna somente o necessário. Isso simplifica o desenvolvimento e a manutenção dos servidores e clientes.

## HTTP Status

1xx - Informational: indica que a solicitação está sendo processada.
2xx - Success: indica que a solicitação foi recebida, compreendida e aceita com sucesso
3xx - Redirection: indica que o cliente precisa executar mais algumas operações para completar a solicitação
4xx - Client Error: indica que ocorreu um erro por parte do cliente
5xx - Server Error: indica que aconteceu um erro por parte do servidor.

## Convenções de nomenclatura

1. Use sempre substantivos em vez de verbos para indicar um recurso

    Exemplo: ```/users``` no lugar de ```/getUsers```

1. Usar plural para coleção de recursos

    Exemplo: ```/users``` no lugar de ```/user```


# Perguntas e Respostas (FAQ)

_Algumas perguntas e respostas foram tiradas do ChatGPT, outras inventadas e outras de sites que estão nas referências_

1. O que é REST e o que significa RESTful?
1. Quais são os principais princípios de REST?
1. Explique o Stateless.
1. Quais são os métodos HTTPs mais utilizados e quais são os seus significados?
1. Qual a diferença entre PUT e POST?
1. O que é Content-Type em uma requisição e o por que é importante no REST?
1. Como lidar com Autenticação em uma REST API?
1. **O que é HATEOAS?**

    Hypermedia As The Engine Of Application State é um princípio que sugere que a navegação de um dado em um serviço deve ser guiada por links dinâmicos nos dados das aplicações.

1. **Qual a diferença entre HTTP Status 404 e 204?**

    O 404 significa que o recurso não foi encontrado, ou seja, que a URL que foi informada não existe. Já o 204, informa que a requisição foi bem sucedida e que o servidor não encontrou nenhum conteúdo para retornar.

# Referências

1. [O que é uma API RESTful?](https://aws.amazon.com/pt/what-is/restful-api/)
1. [API REST](https://www.redhat.com/pt-br/topics/api/what-is-a-rest-api)