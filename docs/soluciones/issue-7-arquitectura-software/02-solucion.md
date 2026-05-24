## Solución propuesta

### 1. Diagrama de arquitectura en el repositorio
Crear `docs/arquitectura.md` con:
- Diagrama de capas (presentación, lógica, datos)
- Flujo de datos principal
- Responsabilidad de cada módulo/carpeta

### 2. Sesión de Architecture Walkthrough
Reunión de 1 hora donde el arquitecto/lead explica el sistema completo. Grabar la sesión.

### 3. Pair Programming supervisado
El miembro con dificultades trabaja en pareja con un desarrollador senior por al menos 1 semana.

### 4. Code Review más detallado
Durante el período de aprendizaje, sus PRs reciben feedback explicando el "por qué" además del "qué".

### Estructura de carpetas documentada
```
src/
├── api/          # Controladores y rutas HTTP
├── services/     # Lógica de negocio
├── repositories/ # Acceso a base de datos
├── models/       # Definición de entidades
└── utils/        # Funciones auxiliares
```
