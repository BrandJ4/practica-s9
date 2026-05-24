## Solución propuesta

### 1. Análisis de compatibilidad
Identificar las partes del código con dependencias de OS:
- Rutas de archivos (`/` vs `\`)
- Comandos de sistema
- Librerías nativas
- Variables de entorno

### 2. Usar abstracciones multiplataforma
```python
# MAL: específico de OS
path = "C:\Users\usuario\archivo.txt"

# BIEN: multiplataforma
import os
path = os.path.join("usuarios", "usuario", "archivo.txt")

# AÚN MEJOR:
from pathlib import Path
path = Path("usuarios") / "usuario" / "archivo.txt"
```

### 3. Docker para normalizar ambientes
```dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
CMD ["python", "main.py"]
```

### 4. CI con múltiples OS en GitHub Actions
```yaml
strategy:
  matrix:
    os: [ubuntu-latest, windows-latest, macos-latest]
```
