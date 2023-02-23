# Project folder structure

```bash
├── main.dart
├── external
│  ├── database
│  ├── geolocation
│  ├── http
│  ├── local_storage
│  └── xpto_api
│    └── xpto_api_service.dart
├── features
│  ├── auth
│  │  ├── auth.dart
│  │  ├── data
│  │  │  └── repositories
│  │  │    ├── sign_in_repository.dart
│  │  │    └── sign_up_repository.dart
│  │  ├── domain
│  │  │  ├── entities
│  │  │  │  ├── sign_in_entity.dart
│  │  │  │  └── sign_up_entity.dart
│  │  │  ├── interfaces
│  │  │  │  └── interfaces.dart
│  │  │  └── usecases
│  │  │    ├── params
│  │  │    │  ├── sign_in_params.dart
│  │  │    │  └── sign_up_params.dart
│  │  │    ├── sign_in_usecase.dart
│  │  │    └── sign_up_usecase.dart
│  │  └── presentation
│  │    ├── sign_in
│  │    │  ├── sign_in_states.dart
│  │    │  ├── sign_in_store.dart
│  │    │  ├── sign_in_view.dart
│  │    │  └── widgets
│  │    ├── sign_up
│  │    │  ├── sign_up_states.dart
│  │    │  ├── sign_up_store.dart
│  │    │  └── sign_up_view.dart
│  │    └── widgets
│  └── common
│    ├── common.dart
│    ├── data
│    │  └── repositories
│    │    ├── database_repository.dart
│    │    ├── geolocation_repository.dart
│    │    └── local_storage_repository.dart
│    ├── domain
│    │  ├── interfaces
│    │  │  └── interfaces.dart
│    │  └── usecases
│    │    ├── database_usecase.dart
│    │    ├── geolocation_usecase.dart
│    │    └── local_storage_usecase.dart
│    └── presentation
│      ├── base_view_model.dart
│      ├── base_view.dart
│      ├── loading_view.dart
│      └── widgets
│        └── xpto_custom_widget.dart
├── setup
│  ├── routes
│  └── themes
└── shared
  ├── constants
  ├── types
  │  ├── failure.dart
  │  └── result.dart
  └── utils
    └── validators
```