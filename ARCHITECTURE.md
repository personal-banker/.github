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
- Cada feature deverá ter sua própria pasta onde conterá todas as camadas necessárias para a execução dos casos de uso da feature.
- Todos os designs patterns usados no projeto devem estar listados na sessão “Design Patterns” desse documento, caso contrário será considerado implementação errônea.
- Packages e plugins novos só poderão ser usados nos projetos após avaliação e aprovação de toda equipe responsável pelo projeto.
- Atualizações no modelo de domínio só poderão ser aceitas se primeiro for adicionada nesse documento e aprovado por todos os envolvidos no projeto.
- Não é permitido ter uma classe concreta como dependência de uma camada. Só será aceita coesão com classes abstratas ou interfaces, exceto Stores.
- Stores devem estar no mesmo nivel de suas respectivas pages e não devem ter regras de negócio, mas devem ser o elo entre a camada de apresentação e o domínio.
- Cada camada deve ter apenas uma responsabilidade.


## Entidades



## Casos de Uso



## Design Patterns

- Repository Pattern: Para acesso a API externa.
- Service Pattern: Para isolar trechos de códigos e segmentar responsabilidades.
- Dependency Injection: Resolver dependências das classes.
- Store: Guardar e mudar estados.
- State pattern: Padrão que auxilia no gerenciamento estados.
- Result: Metodos retornarem Success ou Failures.


## Packages

- [flutter_modular](https://pub.dev/packages/flutter_modular): Modularização de rotas e injeção de dependências.
- [flutter_triple](https://pub.dev/packages/flutter_triple): Implementação de Stores para gerência de estado
- [result_dart](https://pub.dev/packages/result_dart): Retorno múltiplo no formato Failure e Success.
- [uno](https://pub.dev/packages/uno): Cliente HTTP.
- [mocktail](https://pub.dev/packages/mocktail): Para testes de unidade.
- [realm](https://pub.dev/packages/realm): Base de dados local.