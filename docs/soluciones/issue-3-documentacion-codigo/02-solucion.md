## Solución propuesta

### 1. Estándar de documentación de funciones
Todo función/método debe incluir:
```python
def calcular_descuento(precio: float, porcentaje: float) -> float:
    """
    Calcula el precio final aplicando un descuento.
    
    Args:
        precio: Precio original del producto (en soles)
        porcentaje: Porcentaje de descuento (0-100)
    
    Returns:
        Precio final después del descuento
    
    Raises:
        ValueError: Si el porcentaje no está entre 0 y 100
    """
```

### 2. README.md obligatorio por módulo
Cada directorio principal debe tener su README con:
- Propósito del módulo
- Cómo ejecutarlo
- Dependencias
- Ejemplos de uso

### 3. Wiki del proyecto en GitHub
Usar GitHub Wiki para documentar:
- Arquitectura general
- Decisiones técnicas tomadas (ADRs)
- Guía de configuración del entorno

### 4. Documentación como criterio de Definition of Done
Una tarea NO está completa si el código no está documentado.
