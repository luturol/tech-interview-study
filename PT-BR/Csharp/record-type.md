# Record Type

É possível declarar uma classe usando a keyword ```record``` no lugar da classe. Record Type é uma classe **imutável**, tornando possível a alteração de suas próprias somente com uma nova instância dela.

#### Observação:

A partir do C# 9, já é possível criar record **mutável**. No lugar do ```init``` colocar ```set```.

## Declaração de um Record

Há duas formas de declarar um record.

Tradicional:

```csharp
public record Pessoa {
    public string Nome { get; init; }
    public string Sobrenome { get; init; }
}
```

ou da seguinte forma (Positional syntax for property definition):

```csharp
public record Pessoa(string Nome, string Sobrenome);
```

Usando o Positional Syntax o compilador cria o seguinte:

- Propriedades públicas init-only para cada parâmetro. As propriedades só podem ter seus valores atribuídos no contrutor ou por uma Property Initializer.

- Um construtor primário de acordo com a posição das propriedades declarados no record.

- Um método ```Deconstruct``` com um parâmetro ```out``` para cada variável em suas respectivas posições.

Por default todas as propriedades são ```readonly```, mas podem ser declaradas com ```set``` e serem mutáveis. Entretanto, isso perde a capacidade **imutável** do record.

## Alterando o valor de um record

Para alterar o valor de um record é necessário criar uma nova instância dele. Porém, se tu quiser criar com os mesmos valores e só alterando um é possível utilizar a keyword ```with```.

```csharp
var pessoa = new Pessoa("teste", "testando");

var pessoa1 = pessoa with { Sobrenome = "novo valor" };
```

```pessoa1``` agora tem outro valor no ```Sobrenome``` e possui o mesmo valor para ```Nome``` da variável ```pessoa```.

## Value Equality

Agora record já possui implementado Value Equality. Significa que é possível verificar com ```==``` se um record é igual ao outro sem precisar comparar todas as propriedades. Só será **true** se os tipos das propriedades forem iguais e se os valores também. Além disso, se validar pela referência, ele irá buscar pelo ponteiro se é igual e não só pelos valores. Então, se tiver dois objetos instânciados com os mesmos valores é possível comparar tudo somente com ```==``` e se quiser pela referência então é preciso usar o ```RefereceEquals()``` método.

```csharp
 public record Monstro(string Nome, int HP);

public static void Main()
{
    var phoneNumbers = new string[2];
    Monstro monstro1 = new("Kobold", 6);
    Monstro monstro2 = new("Kobold", 6);
    Console.WriteLine(monstro1 == monstro2); // True
    
    Console.WriteLine(ReferenceEquals(monstro1, monstro2)); // False
}
```

## Herança

Um record só pode herdar de outro **record**

```csharp
public abstract record Monster(string Name, int HP);
public record Kobold(string Name, int HP, string Class) : Monster(Name, HP);

Monster kobold = new Kobold("Clave", 6, "Warrior");
Console.WriteLine(kobold);
```

Para dois records serem iguais, então o **run-time type** precisam ser iguais.

```csharp
public abstract record Monster(string Name, int HP);
public record Kobold(string Name, int HP, string Class) : Monster(Name, HP);
public record Orc(string Name, int HP, string Class) : Monster(Name, HP);

Monster kobold = new Kobold("Clave", 6, "Warrior");
Monster orc = new Orc("Clave", 6, "Warrior");

Console.WriteLine(kobold == orc); // False

Monster kobold1 = new Kobold("Clave", 6, "Warrior");
Console.WriteLine(kobold == kobold1); //True
```

## Referências

- [What's new in C# 9.0](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-9)
