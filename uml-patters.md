## Bridge Pattern
```mermaid
classDiagramBridgPattern
    class Abstraction {
        -implement:Implementor
        +function:()
    }

    class RefinedAbstraction {
        +redefinedFunction()
    }

    class Implementor {
        +implementation()
        +adicionarNovaAba(URL url)
        +atualizarPagina()
    }

    class ConcreteImplementor {
        +implementation()
    }

    Abstraction o-- Implementor
    Abstraction <|-- RefinedAbstraction
    Implementor <|-- ConcreteImplementor
```
##
```mermaid
classDiagram
    class ReprodutorMusical {
        -musicaAtual:Musica
        -musicas:List<Musica>
        +tocar()
        +pausar()
        +selecionarMusica(String musica)
    }

    class AparelhoTelefonico {
        +ligar(String numero)
        +atender()
        +iniciarCorreioVoz()
    }

    class NavegadorInternet {
        -linkAtual:URL
        -linksAbertos:List<URL>
        +exibirPagina(String url)
        +adicionarNovaAba(URL url)
        +atualizarPagina()
    }

    class iPhone {
        #reprodutor:ReprodutorMusical
        #telefone:AparelhoTelefonico
        #navegador:NavegadorInternet
    }

    class Musica {
        -titulo:String
        -autor:String
    }

    class URL {
        -link:String
    }

    iPhone --> ReprodutorMusical
    iPhone --> AparelhoTelefonico
    iPhone --> NavegadorInternet
    Musica --> ReprodutorMusical
    URL --> NavegadorInternet
```
