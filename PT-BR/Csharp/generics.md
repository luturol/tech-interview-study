# Generics

## O que é?

# Perguntas e Respostas (FAQ)

_Algumas perguntas e respostas foram tiradas do ChatGPT, outras inventadas e outras de sites que estão nas referências_

1. Qual o significado de ```where T: class, new()```?

    O ```new()``` significa que é possível criar uma nova instância de T, e que T deve ter um construtor sem parâmetros permitindo a criação de uma nova instância de T usando ```new T();``` dentro da classe genérica. A keyword ```class``` depois do ```where``` indica que T deve ser uma classe, não uma struct, para poder ser usado como parâmetro na classe genérica.


## Referências

- [where (generic type constraint) (C# Reference)](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/where-generic-type-constraint)
- ["where" keyword in class declaration in c sharp](https://stackoverflow.com/questions/1598487/where-keyword-in-class-declaration-in-c-sharp)
