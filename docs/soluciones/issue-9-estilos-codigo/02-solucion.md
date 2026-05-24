## Solución propuesta

### 1. Guía de estilo del proyecto
Crear `docs/CODING_STANDARDS.md` con:

#### Convenciones de nombres
```python
# Variables y funciones: snake_case
nombre_usuario = "Juan"
def calcular_total():

# Clases: PascalCase  
class UsuarioAdmin:

# Constantes: UPPER_SNAKE_CASE
MAX_INTENTOS = 3
```

#### Estructura de archivos
```
Máximo 300 líneas por archivo
Una clase principal por archivo
Imports ordenados: stdlib → third-party → local
```

### 2. Linter y formatter automático
Configurar herramientas que apliquen el estilo automáticamente:
- **Python:** `black` (formatter) + `flake8` (linter)
- **JavaScript:** `prettier` + `eslint`

### 3. Pre-commit hooks
```bash
# .pre-commit-config.yaml
repos:
  - repo: https://github.com/psf/black
    hooks:
      - id: black
```
El código se formatea automáticamente antes de cada commit.

### 4. Configuración en el repositorio
Agregar archivos de configuración al repo para que todos usen los mismos settings.
