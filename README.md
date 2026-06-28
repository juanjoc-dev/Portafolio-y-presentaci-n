# Portafolio Profesional

Portafolio minimalista y elegante para mostrar mi perfil profesional, acceso a redes sociales y proyectos futuros.

## Características

- 📋 Perfil profesional detallado
- 🔗 Enlaces a redes sociales
- 🎨 Diseño minimalista y elegante
- 🎭 Paleta de colores tecnológicos fríos
- 🏗️ Arquitectura hexagonal

## Paleta de Colores

- **Primario**: Gris oscuro (#1a1a1a)
- **Secundario**: Azul tecnológico (#0066cc)
- **Acentos**: Morado (#7c3aed), Amarillo (#fbbf24)
- **Neutros**: Blanco (#ffffff), Gris claro (#f3f4f6)

## Estructura del Proyecto

```
.
├── src/
│   ├── domain/           # Lógica de negocio pura
│   ├── application/      # Casos de uso y servicios
│   ├── infrastructure/   # Implementaciones externas
│   ├── interfaces/       # Presentación y UI
│   └── config/           # Configuración
├── public/               # Assets estáticos
│   ├── images/
│   ├── fonts/
│   ├── styles/
│   └── js/
├── tests/                # Tests unitarios e integración
└── README.md
```

## Arquitectura Hexagonal

El proyecto sigue el patrón de arquitectura hexagonal (Puertos y Adaptadores) para mantener la separación de responsabilidades:

- **Domain**: Contiene la lógica de negocio independiente de cualquier framework
- **Application**: Implementa los casos de uso del sistema
- **Infrastructure**: Maneja la comunicación externa (APIs, bases de datos)
- **Interfaces**: Proporciona la presentación (UI)

## Instalación

```bash
npm install
```

## Desarrollo

```bash
npm run dev
```

## Build

```bash
npm run build
```

## Pruebas

```bash
npm test
```

## Licencia

MIT
