# Plataforma Fintech de Billeteras Digitales

Proyecto final de Estructuras de Datos - Sistema de gestión de billeteras digitales y analítica de transacciones.

## Arquitectura del Proyecto

### Backend (Spring Boot)
```
backend/
├── src/main/java/com/fintech/billetera/
│   ├── config/          # Configuración de Spring Boot
│   ├── controller/      # Controladores REST API
│   ├── service/         # Lógica de negocio
│   ├── repository/      # Acceso a datos (JPA)
│   ├── model/           # Entidades de base de datos
│   ├── dto/             # Data Transfer Objects
│   ├── datastructures/  # Implementaciones de estructuras de datos
│   │   ├── listas/      # Listas para historiales
│   │   ├── pilas/       # Pilas para operaciones reversibles
│   │   ├── colas/       # Colas para operaciones programadas
│   │   ├── arboles/     # Árboles para rankings
│   │   ├── tablashash/  # Tablas hash para acceso rápido
│   │   └── grafos/      # Grafos para análisis de relaciones
│   ├── exception/       # Manejo de excepciones
│   └── util/            # Utilidades
└── src/main/resources/
    └── application.properties
```

### Frontend (React)
```
frontend/
├── src/
│   ├── components/      # Componentes React
│   │   ├── common/      # Componentes reutilizables
│   │   ├── auth/        # Autenticación
│   │   ├── dashboard/   # Dashboard principal
│   │   ├── billetera/   # Gestión de billeteras
│   │   ├── transaccion/ # Transacciones
│   │   ├── operacion/   # Operaciones programadas
│   │   ├── notificacion/# Alertas y notificaciones
│   │   └── reporte/     # Reportes y analítica
│   ├── pages/           # Páginas principales
│   ├── services/        # Servicios API
│   ├── hooks/           # Custom hooks
│   ├── context/         # Contextos React
│   ├── utils/           # Utilidades
│   └── styles/          # Estilos CSS
└── package.json
```

## Tecnologías

### Backend
- Java 17
- Spring Boot 3.2.0
- Spring Data JPA
- Spring Security
- H2 Database (desarrollo)
- MySQL (producción)
- Swagger/OpenAPI

### Frontend
- React 18
- React Router
- Axios
- TailwindCSS
- Recharts (gráficos)
- React Hook Form

## Estructuras de Datos Implementadas

1. **Listas**: Historial de transacciones y notificaciones
2. **Pilas**: Operaciones reversibles y deshacer
3. **Colas**: Operaciones programadas y notificaciones pendientes
4. **Árboles**: Ranking de usuarios por puntos
5. **Tablas Hash**: Acceso rápido a usuarios y billeteras
6. **Grafos**: Análisis de relaciones financieras

## Instalación

### Backend
```bash
cd backend
mvn clean install
mvn spring-boot:run
```

### Frontend
```bash
cd frontend
npm install
npm start
```

## Endpoints Principales

- `GET /api/usuarios` - Listar usuarios
- `POST /api/billeteras` - Crear billetera
- `POST /api/transacciones` - Realizar transacción
- `GET /api/reportes/dashboard` - Dashboard de analítica
- `POST /api/operaciones/programar` - Programar operación

## Documentación

La documentación de la API está disponible en:
- Swagger UI: http://localhost:8080/swagger-ui.html
- API Docs: http://localhost:8080/api-docs
