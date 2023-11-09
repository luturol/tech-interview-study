# Arquitetura em Camadas

É um padrão de arquitetura de software em que partes do projeto são separados em camadas ou módulos distintos com suas próprias responsabilidades. As camadas representam níveis diferentes de abstração e responsabilidade no sistema, e cada camada só interage com as camadas imediatas adjacentes.

## Principais Camadas

1. Camada de Apresentação

    É responsável pela interface do usuário e interação dele. Pode incluir telas, APIs, páginas web...

1. Camada de Lógica de Aplicação ou Lógica de Negócios

    Contém a lógica do negócio. Processa os dados e aplica as necessárias regras de negócio. É independente da camada da interface de usuário.

1. Camada de Acesso aos Dados
    
    Responsável pela conexão com o banco de dados e fornece operações de CRUD para as entidades.

1. Camada de Infraestrutura

    Inclui serviços de log, gerenciamento de configuração, autenticação, entre outros. Não contém a lógica do negócio. Presta suporte para outras camadas.

## Benefícios

1. Separação de Responsabilidade

    Cada camada tem responsabilidade específicas, facilitando a manutenção do sistema.

1. Reusabilidade

    Componentes de cada camada podem ser reutilizados em diferentes partes do sistema ou em outros projetos.

1. Testabilidate

    Cada camada pode ser testada independente.

1. Flexibilidade e Escalabilidade

    Mudanças em uma camada não necessariamente afetam outra camada. É possível escalar camadas conforme a necessidade.

1. Sustentação

    A estrutura modular facilita a manutenção e resolução de bugs.


# Perguntas e Respostas (FAQ)

_Algumas perguntas e respostas foram tiradas do ChatGPT, outras inventadas e outras de sites que estão nas referências_

# Referências

1. [Arquitetura multicamada](https://pt.wikipedia.org/wiki/Arquitetura_multicamada)
1. [Arquitetura em Camadas](https://imasters.com.br/arquitetura-da-informacao/arquitetura-em-camadas)
1. [Camadas](https://guia.dev/pt/pillars/software-architecture/layers.html)