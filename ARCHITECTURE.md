# Estructura del Proyecto

```
Portafolio-y-presentación/
│
├── src/                           # Código fuente principal
│   ├── domain/                    # Capa de dominio (lógica de negocio pura)
│   │   ├── entities/
│   │   │   ├── ProfessionalProfile.js
│   │   │   ├── Project.js
│   │   │   └── index.js
│   │   └── value-objects/
│   │       ├── SocialLink.js
│   │       └── index.js
│   │
│   ├── application/               # Capa de aplicación (casos de uso)
│   │   ├── services/
│   │   │   ├── GetProfileService.js
│   │   │   └── GetProjectsService.js
│   │   └── dtos/
│   │       ├── ProfileDTO.js
│   │       └── ProjectDTO.js
│   │
│   ├── infrastructure/            # Capa de infraestructura (implementaciones externas)
│   │   ├── repositories/
│   │   │   ├── ProfileRepository.js
│   │   │   ├── LocalStorageProfileRepository.js
│   │   │   ├── ProjectRepository.js
│   │   │   └── LocalStorageProjectRepository.js
│   │   └── api-clients/
│   │       └── GitHubApiClient.js
│   │
│   ├── interfaces/                # Capa de interfaces (presentación)
│   │   └── ui/
│   │       ├── ProfilePresenter.js
│   │       ├── ProjectPresenter.js
│   │       ├── components/
│   │       │   ├── ProfileComponent.js
│   │       │   └── ProjectsComponent.js
│   │       └── pages/
│   │
│   ├── config/                    # Configuración centralizada
│   │   └── config.js
│   │
│   └── README.md                  # Documentación de src/
│
├── public/                        # Archivos estáticos
│   ├── index.html
│   ├── images/                    # Imágenes
│   ├── fonts/                     # Fuentes locales
│   ├── styles/
│   │   └── main.css
│   └── js/
│       ├── main.js
│       └── app/
│           └── PortfolioApp.js
│
├── tests/                         # Tests
│   ├── unit/
│   │   ├── ProfessionalProfile.test.js
│   │   └── Project.test.js
│   └── integration/
│
├── .git/                          # Repositorio Git
├── .gitignore
├── .editorconfig
├── package.json
├── jest.config.js
├── tsconfig.json
└── README.md
```

## Descripción de Capas (Arquitectura Hexagonal)

### Domain (src/domain/)
- **Propósito**: Contiene la lógica de negocio pura, independiente de cualquier framework o librería externa
- **Contenido**:
  - **Entities**: Objetos con identidad única (ProfessionalProfile, Project)
  - **Value Objects**: Objetos sin identidad, definidos por sus valores (SocialLink)
  - **Business Rules**: Reglas que deben cumplirse

### Application (src/application/)
- **Propósito**: Implementa los casos de uso del sistema
- **Contenido**:
  - **Services**: Coordina entidades del dominio y repositorios
  - **DTOs**: Objetos de transferencia de datos entre capas

### Infrastructure (src/infrastructure/)
- **Propósito**: Implementaciones técnicas y conectores externos
- **Contenido**:
  - **Repositories**: Abstracción para acceso a datos (LocalStorage, APIs, BD)
  - **API Clients**: Clientes para consumir APIs externas (GitHub, etc.)

### Interfaces (src/interfaces/)
- **Propósito**: Presentación y componentes UI
- **Contenido**:
  - **Presenters**: Adaptadores de datos del dominio a formato presentable
  - **Components**: Componentes reutilizables de UI
  - **Pages**: Páginas completas

## Colores Principales

- **Primary**: #1a1a1a (Gris oscuro)
- **Secondary**: #0066cc (Azul tecnológico)
- **Accent Purple**: #7c3aed (Morado)
- **Accent Yellow**: #fbbf24 (Amarillo)
- **Neutral White**: #ffffff (Blanco)
- **Neutral Light**: #f3f4f6 (Gris claro)

## Cómo Iniciar

1. Instalar dependencias: `npm install`
2. Iniciar desarrollo: `npm run dev`
3. Ejecutar tests: `npm test`
