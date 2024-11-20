
# Sistema de Clases Particulares API

API REST desarrollada con Flask y SQLAlchemy siguiendo Clean Architecture para gestionar un sistema de clases particulares.

## Tecnologías

- Python 3.12
- Flask 
- SQLAlchemy
- SQL Server
- Docker

## Estructura del Proyecto

```
src/
├── application/
│   └── usecases/         # Casos de uso por entidad
├── domain/
│   ├── entities/         # Entidades de dominio
│   └── repositories/     # Interfaces de repositorios
├── infrastructure/
│   └── persistence/      # Implementación de persistencia
└── interfaces/
    └── http/            # Controllers y rutas HTTP
```

## Entidades

- Usuarios (tutores y participantes)
- Asignaturas
- Anuncios de clases
- Clases particulares
- Comentarios

## Endpoints

### Usuarios
- `GET /api/usuarios` - Listar usuarios
- `GET /api/usuarios/{id}` - Obtener usuario
- `POST /api/usuarios` - Crear usuario
- `PUT /api/usuarios/{id}` - Actualizar usuario
- `DELETE /api/usuarios/{id}` - Eliminar usuario

### Asignaturas
- `GET /api/asignaturas` - Listar asignaturas
- `POST /api/asignaturas` - Crear asignatura 
- `PUT /api/asignaturas/{id}` - Actualizar asignatura
- `DELETE /api/asignaturas/{id}` - Eliminar asignatura

### Anuncios
- `GET /api/anuncios` - Listar anuncios
- `GET /api/anuncios/asignatura/{id}` - Anuncios por asignatura
- `POST /api/anuncios` - Crear anuncio
- `PUT /api/anuncios/{id}` - Actualizar anuncio
- `DELETE /api/anuncios/{id}` - Eliminar anuncio

### Clases 
- `GET /api/clases` - Listar clases
- `GET /api/clases/participante/{id}` - Clases por participante
- `POST /api/clases` - Crear clase
- `PUT /api/clases/{id}` - Actualizar clase
- `DELETE /api/clases/{id}` - Eliminar clase

### Comentarios
- `GET /api/comentarios` - Listar comentarios
- `GET /api/comentarios/tutor/{id}` - Comentarios por tutor
- `POST /api/comentarios` - Crear comentario
- `PUT /api/comentarios/{id}` - Actualizar comentario
- `DELETE /api/comentarios/{id}` - Eliminar comentario

## Instalación

1. Clonar repositorio
2. Crear entorno virtual: `python -m venv venv`
3. Activar entorno: `source venv/bin/activate`
4. Instalar dependencias: `pip install -r requirements.txt`
5. Configurar variables de entorno
6. Iniciar contenedor SQL Server: `docker-compose up -d`
7. Ejecutar aplicación: `python src/app.py`

## Variables de Entorno

```env
DATABASE_URI=mssql+pyodbc://sa:password@localhost:1433/db
```
