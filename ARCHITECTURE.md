# Arquitetura

## Objetivo

- Documentar a arquitetura do projeto.
- Descrever os critérios de desenvolvimento de software e qualidade de código esperados.
- Catalogar patterns e packages a serem utilizados.

## Regras 

- Designs patterns usados no projeto devem estar listados na sessão Design Patterns desse documento.
- Packages usados no projeto devem estar listados na sessão Packages desse documento.
- As entidades e casos de uso devem ser criadas e mantidas conforme às sessões `Entidades` e `Casos de Uso` desse documento.
- Cobertura mínima de testes (70%) e regras de lint serão checados pelo CI à cada Pull Request, aceitando apenas alterações que atendam os requisitos.
- Não é permitido ter uma classe concreta como dependência de uma camada. Só será aceita coesão com classes abstratas ou interfaces, exceto Stores.
- Stores não devem ter regras de negócio, mas sim ser o elo entre a camada de apresentação e o domínio.
- Este documento precede ao código, se existir a necessidade de alterar alguma das regras ou contratos descritos deve-se:
  - Debater o assunto com os envolvidos no projeto
  - Obter aceite para a alteração em questão
  - Modificar este documento registrando o novo cenário
  - Implementar no código

## Estrutura da aplicação

- Camadas globais da aplicação, como constantes e utilitários, devem ficar na pasta `app/shared`.
- Itens referentes à configuração da aplicação, como temas e rotas, devem ficar na pasta `app/setup`.
- Packages que possibilitam acesso à itens externos à aplicação devem ser encapsulados e disponibilizados em serviços na pasta `app/external`
  - Ex 1: Criar o `httpService` que encapsula o package `http`.
  - Ex 2: Criar o `localStorageService` que encapsula algum package de armazenamento local.
  - Ex 3: Criar o `xptoApiService` que utilizará o `httpService` para acessar uma api externa chamada `Xpto`
- Seguindo o conceito de `feature first`, cada feature será uma pasta em `app/features`
- Cada feature é dividida em Data, Domain e Presentation
  - Data: acesso à infraestrutura previamente encapsulada pelos serviços da pasta `app/external`.
  - Domain: representação do domínio com as entidades, casos de uso e das abstrações a serem implementadas.
  - Presentation: camada visual aplicação com as pages, stores e states.
- Features devem ser independentes entre si tanto quanto possível, para controlar isto um arquivo na raíz de cada feature expõem quais itens podem ser exportados.
  - Ex: A feature `auth` possui a regra de `sign_in` e expõem a entidade `sign_in_entity` no arquivo `app/features/auth/auth.dart`.
- Regras, entidades, repositórios, etc, que sejam comuns entre features também podem ser criadas na feature `common`.
- A relação entre features e pages não é 1:1 necessáriamente, uma feature é uma sessão da aplicação que tem funções relacionadas
  - Ex: A feature de `auth` possui as paginas de `sign_out`, `sign_in`, `update_password`, etc...


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
