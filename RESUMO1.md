# RESUMO 1 JAVA



# PASSO A PASSO PARA CRIAR UM PROJETO 

- LIGAR O XAMPP
- CRIAR UM PROJETO NO SPRING INITIALIZR
- SELECIONAR AS DEPENDÊNCIAS NECESSÁRIAS (NO CASO, SPRING WEB, SPRING DATA JPA, MYSQL DRIVER E VALIDATION)
- BAIXAR O PROJETO
- IMPORTAR O PROJETO NO INTELLIJ
- CRIAR O BANCO DE DADOS E LIGAR ELE PELO INTELIIJ EM APPLICATION PROPERTIES
- AJUSTAR O POM.XML
- CRIAR A ESTRUTURA DE PASTAS
- EXEMPLOAPPLICATION.JAVA FICA NA PASTA PRINCIPAL
- CRIAR MODELO, REPOSITORY, SERVICE E CONTROLLER
- PRIMEIRO CRIAR OS MODELOS NECESÁRIOS
- CRIAR O REPOSITORY
- CRIAR O SERVICE
- CRIAR O CONTROLLER
- CRIAR OS MÉTODOS NO CONTROLLER
- CRIAR OS MÉTODOS NO SERVICE


## ESTRUTURA
- MODEL -> CONTROLLER -> SERVICE -> REPOSITORY -> BANCO DE DADOS




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


## 12. CLASSE
- Modelo de dados
- Representação de um objeto
- Atributos e comportamentos
- Exemplo de classe:
```
public class Pessoa {
    private String nome;
    private int idade;
}
```


## 13. OBJETO

- Instância de uma classe
- Atributos com valores específicos
- Exemplo de objeto:
```
Pessoa pessoa = new Pessoa();
pessoa.nome = "João";
pessoa.idade = 30;
```



## 14. ATRIBUTOS

- Características de um objeto
- Representam as partes que compõem um objeto
- Exemplo de atributos:
```
public class Pessoa {
    private String nome;
    private int idade;
}
```




## 15. PRINCIPAIS COMANDOS JAVA COM EXEMPLOS

- System.out.println("Hello World"): imprime uma mensagem no console

- int idade = 30: declara uma variável do tipo inteiro com o nome idade e atribui o valor 30

- String nome = "João": declara uma variável do tipo String com o nome nome e atribui o valor "João"

- main: método principal, ponto de entrada de uma aplicação Java

- public: modificador de acesso, indica que o método é público e pode ser acessado por qualquer classe

- static: indica que o método é estático, ou seja, pertence à classe e não a uma instância da classe

- void: indica que o método não possui retorno

- String[] args: parâmetro do método main, é um array de Strings

- System.out.println(): imprime uma mensagem no console

- System.out.print(): imprime uma mensagem no console






## 16. CONSTRUTOR
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

## 14. IMPORTANTE
- Por precaução sempre deixe o xampp ligado antes de iniciar o projeto
- Sempre que for iniciar o projeto, inicie o xampp primeiro
- Fazemos os contrutores e getters e setters fora da main e chamamos eles dentro da main instanciando um objeto


## 15. TESTE SIMPLES DA AULA1

-No meu caso coloquei o apache para rodar na PORTA 8070 e o projeto na PORTA 8080 pois estava dando conflito

-Coloque seu banco de dados para rodar no xampp

-NÃO ESQUEÇA DAS IMPORTAÇÕES E PACOTES ANTES DE RODAR O PROJETO



```
public class Aula1 {
    public static void main(String[] args) {
        SpringApplication.run(JavaApplication.class, args);

        System.out.println("Funcionou!");
    }
}


```


# AULA 2

## 1. PADRÃO DE ARQUITETURA MVC
- Model View Controller
- Separação de responsabilidades
- Model: modelo de dados, regras de negócio, acesso a dados
- View: interface gráfica
- Controller: controla o fluxo de execução, recebe requisições, processa dados, retorna respostas
- ISOLAMOS AS CAMADAS PARA FACILITAR A MANUTENÇÃO DO CÓDIGO

 
#### EXEMPLO DE UM CONTROLLER
```
@RestController
@RequestMapping("/teste")
public class HelloWorldController {

  @GetMapping
  public String teste(){
    HelloWorldService service = New HelloWorldService();
    return service.teste();
  }
}
```

#### EXEMPLO DE UM SERVICE
```
@Service
public class HelloWorldService {

  public String teste(){
    return "Hello World!";
  }
}
```

#### EXEMPLO DE UM MODEL
```
@Data
public class HelloWorldModel {
  private String mensagem = "Hello World!";
}
```



#### SIGNIFICADO DOS COMANDOS
- @RestController: indica que a classe é um controller, basicamente diz que é uma api rest
- @RequestMapping é a rota do navegador, no caso localhost:8080/teste
- @GetMapping: indica que o método será executado quando houver uma requisição GET para a rota /teste
- @Service: indica que a classe é um service
- @Data: cria os getters e setters automaticamente


##### Como testamos a aplicação?
- Iniciamos o xampp
- Iniciamos o projeto
- Chamamos a rota no postman localhost:8080/teste
- A mesma rota que colocamos no @RequestMapping


# ATALHOS IMPORTANTES ATÉ AGORA
- CTRL + SHIFT + O: IMPORTA AS CLASSES NECESSÁRIAS
- BOTÃO DIREITO DO MOUSE + GENERATE: GERA OS GETTERS E SETTERS
- BOTÃO DIREITO DO MOUSE + GENERATE: GERA O CONSTRUTOR
- sout + TAB: GERA O System.out.println("");
- main + TAB: GERA O MÉTODO MAIN
 


 # ANOTAÇÕES IMPORTANTES
    - @RestController: indica que a classe é um controller, basicamente diz que é uma api rest
    - @RequestMapping é a rota do navegador, no caso localhost:8080/teste
    - @GetMapping: indica que o método será executado quando houver uma requisição GET para a rota /teste
    - @Service: indica que a classe é um service
    - @Data: cria os getters e setters automaticamente
    - @ResponseEntity: retorna uma resposta personalizada
    - @PathVariable: indica que o parâmetro da rota é uma variável
    - @RequestBody: indica que o parâmetro da requisição é um objeto
    - @PostMapping: indica que o método será executado quando houver uma requisição POST para a rota /teste
    - @PutMapping: indica que o método será executado quando houver uma requisição PUT para a rota /teste
    - @DeleteMapping: indica que o método será executado quando houver uma requisição DELETE para a rota /teste
    


# AULA 3 e 4 

- Facade: é um padrão de projeto estrutural que fornece uma interface simplificada para uma biblioteca, um framework ou qualquer conjunto complexo de classes.

- DTO: Data Transfer Object, é um padrão de projeto de software usado para transferir dados entre subsistemas de um software. DTOs são frequentemente usados em conjunção com objetos de acesso a dados para obter dados de um banco de dados.

- Controller: controla o fluxo de execução, recebe requisições, processa dados, retorna respostas

- Service: regras de negócio, acesso a dados

- Model: modelo de dados, basicamente uma classe com atributos e getters e setters

- Repository: acesso a dados

- Entity: representa uma tabela do banco de dados



# AULA 5

### JPA
- Java Persistence API
- Especificação para persistência de dados
- Mapeamento objeto-relacional
- ORM: Object Relational Mapping
- Mapeamento de classes Java para tabelas de banco de dados
- Mapeamento de atributos para colunas

##### Controller -> Service -> Repository -> Banco de Dados



###### COMANDOS USADOS 
- @Entity: indica que a classe é uma entidade
- @Id: indica que o atributo é uma chave primária
- @GeneratedValue: indica que o valor do atributo é gerado automaticamente
- @Column: indica que o atributo é uma coluna
- findall: retorna todos os registros
- findbyid: retorna um registro pelo id
- save: salva um registro
- deletebyid: deleta um registro pelo id
- @RequestBody: indica que o parâmetro da requisição é um objeto
- @ResponseEntity: retorna uma resposta personalizada
- @Autowired: injeta uma dependência, uma instância da classe

- @ManyToOne: indica que a relação é de muitos para um
- @OneToMany: indica que a relação é de um para muitos
- @JsonIgnore ou @JsonIgnoreProperties: ignora o atributo na serialização do JSON




##### SEMPRE LEMBRAR QUE SE NÃO PASSARMOS ROTA PARA OS MÉTODOS, ELES SERÃO EXECUTADOS QUANDO HOUVER UMA REQUISIÇÃO GET PARA A ROTA DO CONTROLLER(PRINCIPAL)

##### SEMPRE FILTRAR POR ID NA ROTA QUANDO FOR FAZER ALGO ESPECÍFICO COM UM REGISTRO


### ANOTAÇÕES IMPORTANTES

- Verificar estrutura de pastas
- Verificar se o xampp está ligado
- Verificar se o banco de dados está rodando
- Verificar se o projeto está rodando
- Verificar se o projeto está na porta correta
- Verificar se o projeto está na rota correta
- Verificar se o projeto está com as dependências corretas
- Verificar se o projeto está com as importações corretas
- Primeiro criar o model, depois o repository, depois o service e por último o controller
- Model: modelo de dados, basicamente uma classe com atributos e getters e setters
- Repository: acesso a dados
- Service: regras de negócio, acesso a dados
- Controller: controla o fluxo de execução, recebe requisições, processa dados, retorna respostas
- Os metodos sao feitos no controller, mas a lógica é feita no service
- Por exemplo o @GetMapping("/pessoas") é a rota que vai ser chamada no navegador, e o método que vai ser executado é o findAll() que está no service, mas o @GetMapping("/pessoas") está no controller








