## Bridge Pattern
```mermaid
classDiagram
    class abstraction {
        -implement:implementor
        +function()
    }

    class refinedAbstraction {
        +redefinedFunction()
    }

    class implementor {
        +implementation()
        +adicionarNovaAba(URL url)
        +atualizarPagina()
    }

    class concreteImplementor {
        +implementation()
    }

    abstraction o-- implementor : bridge pattern
    abstraction <|-- refinedAbstraction
    implementor <|-- concreteImplementor
```
## Decorator
```mermaid
classDiagram
    class masterClass {
        -variable:Type
        +getValue()*
    }

    class sonClassOne {
        +getValue()
    }
    class sonClassTwo {
        +getValue()
    }

    masterClass <|-- sonClassOne
    masterClass <|-- sonClassTwo
```
## Bridge Pattern
```mermaid
classDiagram
    class facadaClass {
        -implement:implementor
        +functionA()
        +functionB(String text):String
        +functionC(Int number):Int
    }

    class classA {
        +functionA()
    }

    class classB {
        +functionB(String text):String
    }

    class classC {
        +functionC(Int number):Int
    }
    facadaClass *--> classA
    facadaClass *--> classB
    facadaClass *--> classC
```
