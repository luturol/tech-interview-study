# C#


## Sumário

1. [Entity Framework](/PT-BR/Csharp/entityframework.md)
1. [Dependency Injection](/PT-BR/Csharp/dependencyinjection.md)
1. [Classes](/PT-BR/Csharp/classes.md)
1. [Record Type](/PT-BR/Csharp/record-type.md)

# Perguntas e Respostas (FAQ)

_Algumas perguntas e respostas foram tiradas do ChatGPT, outras inventadas e outras de sites que estão nas referências_

1. Qual é a diferença entre managed and unmanaged code?
1. Qual é a diferença entre C# e C?
1. O que é uma structure?
1. Qual a diferença entre value type e reference type?
1. Como funciona o Garbage Collector?
1. O que é um destructor?
1. O que é uma constante?
1. Qual a diferença entre const e readonly?
1. Quais são os tipos de classe em C#?

    Abstract, Partial, Static e Sealed. 
    
    Sealead não pode ser herdada, mas podem ser instanciadas. 
    
    Abstract serve de base para outras classes, a diferença entre ela e uma interface é que uma classe abstrata pode conter a implementação base de um método e métodos virtuais para serem alterados pela classe que herda dela,mas uma classe abstrata não pode ser instanciada.

    Partial é uma parte de uma classe que pode ser combinada com outras para formar uma classe.

    Static são classes que contém métodos estáticos e elas não são instanciadas. São criadas 

# Referências

1. [50 C# interview questions to find the best developer](https://www.testgorilla.com/blog/c-sharp-interview-questions/?utm_term=&utm_campaign=Performance+Max+%7C+RoW+Old&utm_source=google&utm_medium=cpc&hsa_acc=4932434860&hsa_cam=13402555368&hsa_grp=&hsa_ad=&hsa_src=x&hsa_tgt=&hsa_kw=&hsa_mt=&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAjw7oeqBhBwEiwALyHLMwoBb7ZIe9e07gePhcrKZOrkUPfTq81rZ12iwghdBM6OhPJ3IOczAxoCAwwQAvD_BwE)
1. [Static Classes and Static Class Members (C# Programming Guide)](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members)
1. [Partial Classes and Methods (C# Programming Guide)](https://learn.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/partial-classes-and-methods)