O que é REST?

- É uma especificação que define a forta de comunicação entre componentes de
  software na web, independente da linguagem
  de programação usada.
- Conjunto de melhores praticas e regras pra desenvolvimento de Web Services
- Essas melhores praticas sao chamadas de constraints
- Rest API é uma API que segue regras especificadas por Roy Field

Vantagem

- Separação entre cliente e servidor
- Escalabilidade, qualquer maquina servidora pode atender qualquer requisição
- Rest API é independente de linguagem de programação
- As APIs podem iteragir entre si
- Demanda de mercado por utilização de Rest API

Constraints

- cliente-servidor : Precisa de um cliente enviando requisições para um
  servidor. O cliente e o servidor podem evoluir
  separadamente, sem dependencia. O cliente e o servidor podem ser substituidos
  desde que a interface nao mude.
- Stateless : A aplicação nao deve possuir estado. A requisição feita para a
  API tem que conter tudo devidamente para
  que a informação seja processada. Servidor nao pode manter sessão.
- Cache : API pode fazer cache de respostas das requisições, especialmente dos
  dados que não mudam frequentemente.
- Interface uniforme : conjunto de operações bem definidas no sistema.
  Identificar recursos do sistema usando URIs
  inserindo um padrao. Usar padrao de protocolo de comunicação para iteragir
  com a API, geralmente protocolo HTTP. A
  resposta de uma requisição deve ser padronizada.
- Sistema em camadas : Camadas de segurança, cache e etc. O cliente nao deve
  conhecer as camadas que possuem no meio
  entre o cliente e o servidor.
- Codigo sob demanda : Servidor enviar codigo que pode ser executado no cliente

Protocolo HTTP

- Protocolo Requisição Resposta
- Composição da Requisição
    - [METODO] [URI] HTTP/[VERSAO] [CABECALHOS] [CORPO/PAYLOAD]
    - Metodo tambem pode ser chamado de verbo HTTP
    - METODO : Conjunto de metodos definidos para realizar uma ação.
    - URI : Caminho que identifica o que queremos dentro do servidor
    - VERSAO : Versao do HTTP
    - CABECALHOS : Chaves e valores que podem ser usados pelo servidor para
      interpretar a requisiçao e executar a
      alteração
- Composição da Resposta
    - HTTP/[Versao] [STATUS] [Cabeçalhos] [CORPO]
    - VERSAO : Indica a versao do protocolo HTTP
    - STATUS : Descreve o resultado de processamento da requisição
    - CABECALHOS : Chaves e Valores que podem ser usadas pelo software
      consumidor para interpretar a resposta.
    - CORPO : Conteudo da resposta, é opcional.

Recursos REST

- Um recurso eh como uma instancia de um objeto de determinada classe
- Um recurso que representa uma unica coisa é conhecido por Singleton
  Resource (Recurso unico)
- O recurso pode ser agrupado em coleções, conhecido como Collection Resource (
  Recurso de coleção). Uma coleção de
  recursos, pode ser considerado um recurso.
- Identificando Recursos
    - REST usa URIs para identificar recursos.
    - URI significa: Uniform Resource Identifier/Identificador de Recurso
      Uniforme. Eh um conjunto de caracteres que tem
      como objetivo dar um endereço para um recurso de forma nao ambigua.
    - URI vs URL: URL é um tipo de URI. URL significa Uniform Resource Locator,
      ou localizador de recurso uniforme. Ela
      especifica um identificar e a localização do recurso tambem.
    - A URI deve se referir a uma coisa, ou seja, a um substantivo, nao um
      verbo ou uma ação, pq coisas possuem
      propriedades, verbos nao possuem.
    - Exemplo: /produtos SIM /listarProdutos NAO
    - Exemplo: /produto/{codigo-produto} -> produto/331 -> O ideal eh ter uma
      interface uniforome e dessa forma nao
      estah uniforme, pois o recurso de coleção foi identificado com /produtos
      e o recurso unico foi identificado com
      /produto/{codigo}. O ideal e eh consenso no mercado é utilizar os nomes
      sempre no plural.

Spring Rest

O que é Spring Rest ?

- Spring Rest não existe, é apenas um termo.
- Spring seria um conjunto de projetos que resolvem varios problemas do dia a
  dia de um programador java.
- Spring ajuda a criar aplicações com simplicidade e flexibilidade.
- Spring ajuda a focar no desenvolvimento das regras de negocio e nao perder
  tempo desenvolvendo codigo de
  infraestrutura da aplicação.

Por que usar Spring?

- Resolve vários problemas de desenvolvimento de software
    - Gerenciamento de objetos
    - Injeção de dependência
    - Acesso a diferentes fontes de dados: sql, nosql
    - Criação de projetos web
    - Rest API
    - Segurança da aplicação
    - MAIS
- É simples
- É uma tecnologia madura e usada em produção pelas maiores empresas do mundo
- Modularidade:
    - pode ser organizado por projetos e até subprojetos
    - pode se escolher qual deles resolver os problemas.
    - É possível até usar spring junto com outras tecnologias que não são do
      mesmo ecossistema.
- Evolução constante
- Código Open Source
    - Significa que qualquer pessoa pode contribuir com a tecnologia e corrigir
      qualquer problema.
- A comunidade de Spring é grande e tem muita ajuda disponivel, documentações,
  foruns e etc.
- É muito popular
- Empregabilidade alta

Documentação dos projetos Spring

- Doc disponivel aqui: https://spring.io/projects

O que é Spring Data?

- Projeto guarda-chuva que agrupa varios outros projetos relacionados a acesso
  a dado.

O que é Spring Data JPA?

- Será um projeto usado no curso.
- Ajuda a implementar repositorio JPA de forma simples
- Conhecido por Jakarta Persistance (JPA) é uma especificação de persistencia
  de dados pra Java
- Tecnologia que ajuda com acesso e operações com banco de dados relacional +
  java.
- Spring data vai ajudar no sentidoo de quando é necessário programar coisas
  que se tornam repetitivas, isso é chamado de Código Boilerplate, um código
  que precisa ser escrito varias vezes dentro do mesmo projeto com poucas
  variações.

O que é Spring Boot?

- Projeto que se auto configura seguindo convenções com visão opinativa
- Quer dizer que o Spring Boot decide como configurar o projeto de acordo com
  uma opinião propria dos desenvolvedores dele. Ou seja, de acordo com
  convenções que eles acham que são as melhores.
- Então não precisa se preocupar com a maioria das configurações.
- O Spring Boot tambem pode configurar bibliotecas terceiras que pode ser usado
  pelo projeto.
- O Spring Boot não substitui outros projetos do ecossistema.

Como atualizar o projeto quando ele está apresentando erro?

- Clique com o botão direito no arquivo pom.xml
- Busque por maven > Reload Project
- Outra opção é clicar na letra m > botão direito no awpag-api > Reload
  Project

Como utilizar o maven para realizar o clean e o package do projeto?

- Execute o comando: ```mvn clean package``` na raiz do projeto

Como executar o arquivo gerado .jar?

- Execute o comando: ```java -jar <NOME_ARQUIVO.JAR>```

Documentação sobre HTTP Status Code Registry

- https://www.iana.org/assignments/http-status-codes/http-status-codes.xhtml
- https://httpstatuses.io/

O que é Content Negotiation?

- Permitir que o servidor trabalhe respondendo com JSON ou XML é o Content
  Negotiation.
- Para permitir que ocorra o Content Negotiation foi necessario utilizar
  uma dependencia para formatar a resposta para XML.
- Dependencia: jackson-dataformat-xml

Como atualizar automaticamente a aplicação a cada modificação feita?

- Utilize a dependencia devtools no pom.xml
- Ao finalizar a edição no codigo, faça o build project Ctrl+F9

Como levantar o MySql?

- Execute o comando ```docker compose up -d``` na pasta raiz onde o arquivo
  docker-compose.yml está
- Execute o comando ```docker container stop <container_id>``` para parar o
  container
- Execute o comando ```docker container start <container_id>``` para
  levantar o container parado

O que é, para que serve Jakarta EE?

- Jakarta servirá, no projeto, para realizar a persistencia de dados.
- Uma das especificações do Jakarta é o "Jakarta Persistence"
- https://jakarta.ee/specifications/persistence/
- Jakarta fornece uma API e o mapeamento de objeto relacional.
- A dependencia do Jakarta está presente na dependencia spring boot starter
  data jpa > hibernate core > jakarta persistence api

O que é, para que serve Spring Data JPA?

- Substitui EntityManager e evite codigo Boilerplate
- Ajuda na implementação de repositorios
- Repositorio é um padrao de projetos: Padrao onde classes são criadas com
  o objetivo de fazer operações de persistencia de dados.

O que é, para que serve o Jakarta Validation?

- É uma especificação do Jakarta EE (anteriormente Java EE) que define um
  conjunto de anotações e APIs para validação de dados em Java.
- https://jakarta.ee/specifications/bean-validation/

O que é a especificação RFC 7807? (Boas praticas com Exception Handler)

- RFC é uma publicação oficial de uma organização conhecida por IETF
- IETF padroniza como a internet, protocolos, procedimentos, especificações
  técnicas e etc funcionam.
- RFC 7807 serve para padronizar representação de informações de erro em
  respostas HTTP.
- RFC 7807 - Problem Details for HTTP APIs
- https://datatracker.ietf.org/doc/html/rfc7807
- ```
  {
    "type": "https://example.com/probs/out-of-credit", URI QUE IDENFITICA O 
  TIPO DO PROBLEMA, NAO NECESSARIAMENTE DEVE SER ACESSIVEL PELO NAVEGADOR
    "title": "You do not have enough credit.", BREVE DESCRICAO DO PROBLEMA
    "detail": "Your current balance is 30, but that costs 50.", DESCRICAO 
  DETALHADA
    "instance": "/account/12345/msgs/abc", URI DE ONDE OCORREU O PROBLEMA
    "balance": 30, PROPRIEDADE COSTUMIZADA
    "accounts": ["/account/12345",
                 "/account/67890"] OUTRA PROPRIEDADE COSTUMIZADA
   }
  ```
- O Spring Framework MVC na versao 6 dá suporte para essa RFC 7807
- Para aderir RFC, necessário extender ResponseEntityExceptionHandler
- MethodArgumentNotValidException > codes [Email.cliente.email, Email.email,
  Email.java.lang.String, Email]
- Escolha um dos codigos para costumizar a mensagem, lembrando que cada
  codigo tem o seu nivel de especificidade.
- Lembre de alterar o File Encoding do messages.properties para UTF-8, pra
  isso acesse:
- Settings > File Encodings > Default encoding for propertis files: UTF-8

### Boas práticas para trabalhar com data/hora

- O spring faz serialização e deserialização de data/hora para JSON ou do
  JSON, automaticamente utilizando o padrao ISO-8601
- Esse padrão é internacional e recomendado para usar em Rest API's
- Offset é a diferença de horas entre UTC e o horario em que está sendo
  trabalhado, por exemplo horario de Brasilia.
- É importante trabalhar com Offset na data/hora quando estiver trabalhando
  com Rest APIs

### Pq nao usar uma Domain Model como Resources Representation de uma API?

- Atualmente as entidades da aplicação que estão no Domain Model estão
  sendo utilizadas como Modelo de representação do recurso (Resources
  Representation) da API
- Versionamento: Se as entidades de domínio mudarem ao longo do tempo, pode ser
  difícil gerenciar versões diferentes da mesma entidade para atender às
  necessidades de diferentes versões da API. Usar objetos DTO (Data Transfer
  Objects) separados como representações de recursos pode simplificar o
  processo de versionamento, pois permite que você evolua a API
  independentemente do modelo de domínio subjacente.
- Acoplamento entre camadas: Suas entidades de domínio podem ter uma estrutura
  de dados específica para atender às necessidades do seu domínio. Expor
  diretamente essas entidades através da API pode criar um acoplamento
  indesejado entre a camada de domínio e a camada de apresentação (API), o que
  pode dificultar a evolução independente das diferentes partes do sistema.
- Desacoplamento de formato de representação: Ao usar objetos DTO dedicados,
  você pode definir formatos de representação diferentes para diferentes casos
  de uso da API. Por exemplo, você pode ter representações diferentes para a
  mesma entidade que são otimizadas para diferentes dispositivos ou tipos de
  clientes (por exemplo, JSON para clientes da web e protobuf para clientes
  móveis).
- No lugar de usar a entidade, é importante usar um DTO, Data Transfer Object
- É interessante nao misturar as informações da camada de dominio com as 
  informações da camada de api
- Why the domain model should not be used as resources in REST API? 
- https://encr.pw/domainModelShouldNotBeUsedAsResourcesInRestApi