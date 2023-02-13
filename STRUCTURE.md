# Project folder structure

```bash
├── app
│   ├── main.dart
│   ├── shared/
│   │   ├── main_module.dart
│   │   ├── main_store.dart
│   │   │   
│   │   ├── themes/
│   │   │   └── themes.dart
│   │   │   
│   │   └── widgets/
│   │       └── custom_widget_1.dart
│   │
│   ├── src/
│   │   ├── data
│   │   │   ├── services
│   │   │   │   ├── http_service.dart
│   │   │   │   └── local_storage_service.dart
│   │   │   │  
│   │   │   └── repositories
│   │   │       └── auth/
│   │   │           ├── sign_up_repository.dart
│   │   │           └── sign_in_repository.dart
│   │   │
│   │   ├── domain
│   │   │   ├── interfaces
│   │   │   │   └── auth_interfaces.dart
│   │   │   │
│   │   │   ├── entities
│   │   │   │   ├── auth/
│   │   │   │   │   ├── sign_up_entity.dart
│   │   │   │   └── └── sign_in_entity.dart
│   │   │   │  
│   │   │   └── usecases
│   │   │       └── auth/
│   │   │           ├── sign_up_entity.dart
│   │   │           └── sign_in_entity.dart
│   │   │
│   │   ├── presentation
│   │   │   ├── pages
│   │   │   │   ├── sign_up
│   │   │   │   │   ├── sign_up_module.dart
│   │   │   │   │   ├── sign_up_page.dart
│   │   │   │   │   │  
│   │   │   │   │   └── widgets
│   │   │   │   │       └── custom_widget_2.dart
│   │   │   │   │
│   │   │   │   └── sign_in
│   │   │   │       ├── sign_in_module.dart
│   │   │   │       ├── sign_in_page.dart
│   │   │   │       │  
│   │   │   │       └── widgets
│   │   │   │           └── custom_widget_3.dart
│   │   │   │  
│   │   │   ├── states
│   │   │   |   └── sign_in
│   │   │   |       ├── sign_up_state.dart
│   │   │   |       └── sign_in_state.dart
│   │   │   |
│   │   │   └── stores
                └── sign_in
                    ├── sign_up_store.dart
                    └── sign_in_store.dart
```