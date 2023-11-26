# RESUMO 1 JAVA

## 1. JDK
- Java Development Kit
- Conjunto de ferramentas para desenvolvimento Java
- Inclui JRE + Compilador Java + Ferramentas de desenvolvimento
- Em resumo, é o kit de desenvolvimento Java que contém o compilador Java, entre outras ferramentas.


## 2. Spring Boot
-Simplificação de configuração e publicação de aplicações Java
- Servidores embutidos
- Framework Java para desenvolvimento de aplicações web
- Baseado no Spring Framework
- Facilita a configuração e publicação de aplicações web
- Possui um servidor web embutidoss


## 3. API
- Application Programming Interface
- É um conjunto de regras e protocolos que permite que diferentes aplicações se comuniquem entre si
- É uma interface para a comunicação entre diferentes softwares



## 4. Contratos de API
- Documentação da API
- Descreve como acessar e utilizar os recursos expostos por uma API
- Define os recursos disponíveis
- Métodos Http disponíveis


## 5. HTTP
- HyperText Transfer Protocol
- Protocolo de transferência de dados
- Base da comunicação de dados na web
- Comunicação cliente-servidor
- Requisição e resposta
- Apis trabalham encima de URLs e requisições HTTP
- Códigos de status HTTP


## 6. REST
- Representational State Transfer
- Estilo de arquitetura de software
- Define um conjunto de regras para criação de web services
- Formato de dados leve e legível por humanos


## 7. JSON
- JavaScript Object Notation
- Formato de dados leve e legível por humanos
- Formato de dados utilizado em APIs REST
- EXEMPLO:
```
{
    "nome": "João",
    "idade": 30,
    "endereco": {
        "rua": "Rua 1",
        "numero": 10
    }
    filmes: [
        "filme 1",
        "filme 2"
    ]
}
```

## 8. SOFTWARES NECESSÁRIOS
- IDE: Eclipse ou IntelliJ
- JDK: Java Development Kit
- Postman


## 9. APIs RESTFUL
- API é um conjunto de regras e protocolos que permite que diferentes aplicações se comuniquem entre si
- Determina como os componentes de software devem interagir 
- Interface para a comunicação entre diferentes softwares
-Abstracao de Funcionalidades
-Padrão de comunicação
-Versioanmento de API
-Exemplos: Facebook, Twitter, Google Maps, Youtube, etc


## 10. MODELO
- Modelo de dados
- Representação de um objeto
- Atributos e comportamentos
- Classe
- Objeto


## 11. ESTRUTURA DE PASTAS NO INTELIJ
- src/main/java
- src/main/resources
- src/test/java


## 12. CONSTRUTOR
- Método especial para criar objetos
- Mesmo nome da classe
- Sem retorno, void
- Pode receber parâmetros
- Exemplo de construtor sem parâmetros:
```
public class Pessoa {
    public Pessoa() {
    }
}
```

- Exemplo de construtor com parâmetros:
```
public class Pessoa {
    public Pessoa(String nome, int idade) {
    }
}
```

## 13. GETTERS E SETTERS
- Métodos para acessar e modificar atributos
- Getters: retorna o valor do atributo
- Setters: modifica o valor do atributo
- Exemplo de getters e setters:
```
public class Pessoa {
    private String nome;
    private int idade;

    public Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public int getIdade() {
        return idade;
    }

    public void setIdade(int idade) {
        this.idade = idade;
    }
}
```



