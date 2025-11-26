# Sistema de Gestión de Bar 🍺

Sistema completo de gestión para establecimientos de bebidas y aperitivos, desarrollado con arquitectura de microservicios.

## 📋 Descripción

Sistema web desarrollado para administrar todas las operaciones de un bar, incluyendo:
- Gestión de productos (catálogo de bebidas y aperitivos)
- Gestión de sedes y mesas
- Gestión de usuarios y roles
- Gestión de órdenes y pagos
- Historial de ventas
- Reportes y analíticas

## 🏗️ Arquitectura

El sistema está construido con una arquitectura de microservicios:

### Frontend
- **FR-BAR-RT-main**: Aplicación React con TypeScript, Vite y Tailwind CSS

### Microservicios Backend (Go)
- **MS-AUTH-GO-main**: Autenticación y autorización (JWT, RBAC)
- **MS-CATALOG-GO-main**: Gestión de catálogo de productos
- **MS-VENUE-GO-main**: Gestión de sedes y mesas
- **MS-SALES-GO-main**: Gestión de ventas, órdenes y pagos (Sprint 3)
- **MS-REPORTS-GO-main**: Generación de reportes
- **MS-OPTIMIZATION-GO-main**: Algoritmos de optimización

### Infraestructura
- **INFRA-BAR-DK-main**: Configuración Docker Compose, Nginx API Gateway, PostgreSQL

## 🚀 Inicio Rápido

### Requisitos Previos
- Docker Desktop instalado y corriendo
- Git

### Instalación

1. Clonar el repositorio:
```bash
git clone https://github.com/Anyi-gomez/dise-o-de-alggoritmos.git
cd dise-o-de-alggoritmos
```

2. Ejecutar el script de montaje (Windows PowerShell):
```powershell
.\montar-proyecto.ps1
```

3. Acceder al sistema:
- URL: http://localhost:8080
- Email: `admin@bar.com`
- Password: `Admin@123`

## 📚 Documentación

- **Manual de Usuario**: Ver [MANUAL_USUARIO.md](./MANUAL_USUARIO.md)
- **Base de Datos**: Ver [INFRA-BAR-DK-main/database/init.sql](./INFRA-BAR-DK-main/database/init.sql)

## 🎯 Funcionalidades Principales

### Sprint 1-2
- ✅ Autenticación y autorización (ISO 27001)
- ✅ Gestión de usuarios y roles
- ✅ Gestión de sedes y mesas
- ✅ Catálogo de productos

### Sprint 3
- ✅ Gestión de pagos y cierre (Cajero)
- ✅ Historial y consulta de ventas
- ✅ Procesamiento de múltiples métodos de pago
- ✅ Reportes de ventas

## 🗄️ Base de Datos

El sistema utiliza PostgreSQL con el siguiente esquema:
- Usuarios y roles
- Sedes y mesas
- Categorías y productos
- Órdenes y items
- Pagos

### Datos de Ejemplo

Para cargar datos de ejemplo y probar los reportes:
```bash
# Desde el directorio compose
docker compose exec postgres-db psql -U bar_user -d bar_management_db -f /path/to/complete_sample_data.sql
```

## 🔧 Scripts Disponibles

- `montar-proyecto.ps1`: Monta todo el proyecto (Docker build + up)
- `inicializar-admin.ps1`: Inicializa el usuario administrador
- `levantar-servicios.ps1`: Levanta los servicios Docker
- `iniciar-servicios.ps1`: Inicia servicios individuales

## 📊 Tecnologías Utilizadas

- **Frontend**: React, TypeScript, Vite, Tailwind CSS
- **Backend**: Go (Golang), Gin Framework
- **Base de Datos**: PostgreSQL
- **Contenedores**: Docker, Docker Compose
- **API Gateway**: Nginx
- **Autenticación**: JWT (JSON Web Tokens)

## 🔐 Seguridad

- Autenticación basada en JWT
- Validación de contraseñas según ISO 27001
- Control de acceso basado en roles (RBAC)
- Registro de intentos de login
- Bloqueo de cuentas tras múltiples intentos fallidos

## 📝 Estructura del Proyecto

```
.
├── FR-BAR-RT-main/          # Frontend React
├── MS-AUTH-GO-main/         # Microservicio de Autenticación
├── MS-CATALOG-GO-main/      # Microservicio de Catálogo
├── MS-VENUE-GO-main/        # Microservicio de Sedes
├── MS-SALES-GO-main/        # Microservicio de Ventas
├── MS-REPORTS-GO-main/      # Microservicio de Reportes
├── MS-OPTIMIZATION-GO-main/ # Microservicio de Optimización
├── INFRA-BAR-DK-main/       # Infraestructura Docker
├── MANUAL_USUARIO.md        # Manual de usuario
└── README.md                # Este archivo
```

## 🤝 Contribución

Este es un proyecto académico. Para contribuir:
1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto es de uso académico.

## 👥 Autores

- **Anyi Gómez** - [GitHub](https://github.com/Anyi-gomez)

## 🙏 Agradecimientos

- Equipo de desarrollo
- Tutores y profesores
- Comunidad de código abierto

---

**Versión**: 1.0.0  
**Última Actualización**: Noviembre 2025

