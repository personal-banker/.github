# Arquitetura

## Objetivo

- Documentar a arquitetura do projeto.
- Descrever os critérios de desenvolvimento de software e qualidade de código esperados.
- Catalogar patterns e packages a serem utilizados.

## Regras iniciais

Pontos a serem levados em consideração antes de introduzir uma nova feature:

- Todo projeto precisará respeitar as regras de Lint escritas no pacote flutterando-analysis.
- Esse projeto deve ter cobertura mínima de testes de no mínimo 70%.
- Camadas globais devem ter um lugar específico na aplicação, por tanto, devem estar na pasta Shared.
- Além da pasta Shared, o projeto será divido em Data, Domain e Presentation
  - Data: responsável pelos acessos à infraestrutura, como API's, bancos de dados, armazenamento local, etc.
  - Domain: representação do domínio com as entidades, casos de uso e das abstrações a serem implementadas na aplicação
  - Presentation: camada visual aplicação com as pages, stores e states.
- A separação de responsabilidades entre as camadas deve ser mantida.
- Todos os designs patterns usados no projeto devem estar listados na sessão Design Patterns desse documento.
- Packages e plugins novos só poderão ser usados nos projetos após avaliação e aprovação de toda equipe responsável pelo projeto.
- Atualizações no modelo de domínio só poderão ser aceitas se primeiro for adicionada nesse documento e aprovado por todos os envolvidos no projeto.
- Não é permitido ter uma classe concreta como dependência de uma camada. Só será aceita coesão com classes abstratas ou interfaces, exceto Stores.
- Stores não devem ter regras de negócio, mas sim ser o elo entre a camada de apresentação e o domínio.


## Entidades



## Casos de Uso



## Design Patterns

- Dependency Injection: Resolver dependências das classes.
- Repository Pattern: Para acesso a API externa.
- Result: Metodos retornarem Success ou Failures.
- State pattern: Padrão que auxilia no gerenciamento estados.
- Service Pattern: Para isolar trechos de códigos e segmentar responsabilidades.
- Store: Guardar e mudar estados.


## Packages

- [flutter_triple](https://pub.dev/packages/flutter_triple): Implementação de Stores para gerência de estado
- [http](https://pub.dev/packages/http): Cliente HTTP.
- [get_it](https://pub.dev/packages/get_it): Registro e localização de dependências.
- [mocktail](https://pub.dev/packages/mocktail): Para testes de unidade.
- [realm](https://pub.dev/packages/realm): Base de dados local.
- [result_dart](https://pub.dev/packages/result_dart): Retorno múltiplo no formato Failure e Success.