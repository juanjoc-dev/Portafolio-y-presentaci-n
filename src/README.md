# Desarrollo

Este directorio contiene el código fuente de la aplicación.

## Estructura

- **domain**: Lógica de negocio pura (entidades, value objects, reglas)
- **application**: Casos de uso y servicios de aplicación
- **infrastructure**: Implementaciones externas (BD, APIs, repositorios)
- **interfaces**: Presentación y componentes UI
- **config**: Configuración centralizada

## Arquitectura Hexagonal

La arquitectura hexagonal separa las responsabilidades en capas:

1. **Domain (Núcleo)**: La lógica de negocio más pura e independiente
2. **Application**: Casos de uso que coordinan el dominio
3. **Infrastructure**: Detalles técnicos y conexiones externas
4. **Interfaces**: Cómo se presenta la información al usuario

Este diseño permite cambiar implementaciones sin afectar la lógica de negocio.
