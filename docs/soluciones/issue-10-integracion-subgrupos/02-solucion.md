## Solución propuesta

### 1. Definir contrato de API entre módulos PRIMERO
Antes de desarrollar, ambos subgrupos acuerdan:
```json
// Contrato de ejemplo: módulo A llama a módulo B
{
  "endpoint": "/api/usuarios/{id}",
  "method": "GET",
  "response": {
    "id": "integer",
    "nombre": "string",
    "email": "string",
    "activo": "boolean"
  }
}
```

### 2. Rama de integración
```bash
git checkout -b integration/modulo-a-modulo-b
# Ambos subgrupos trabajan aquí para resolver conflictos
```

### 3. Sesión de integración conjunta
- 2-3 horas con representantes de ambos subgrupos
- Revisar interfaces, formatos de datos y dependencias
- Resolver incompatibilidades en tiempo real

### 4. Tests de integración
Escribir tests que prueben la comunicación entre módulos:
```python
def test_integracion_modulo_a_b():
    resultado = modulo_a.procesar(datos_entrada)
    assert modulo_b.recibir(resultado) == esperado
```
