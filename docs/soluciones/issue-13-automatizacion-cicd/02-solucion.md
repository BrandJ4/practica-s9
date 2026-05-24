## Solución propuesta

### 1. Pruebas unitarias básicas
Empezar con lo simple:
```python
# test_calculadora.py
import pytest

def test_suma():
    assert suma(2, 3) == 5

def test_division_por_cero():
    with pytest.raises(ZeroDivisionError):
        dividir(10, 0)
```

### 2. GitHub Actions CI Pipeline
Crear `.github/workflows/ci.yml`:
```yaml
name: CI Pipeline

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Setup Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.11'
      - name: Install dependencies
        run: pip install -r requirements.txt
      - name: Run tests
        run: pytest --cov=src tests/
      - name: Lint check
        run: flake8 src/
```

### 3. Estrategia de implementación gradual
- **Semana 1:** Configurar GitHub Actions con un test simple
- **Semana 2:** Agregar tests para funcionalidades críticas
- **Semana 3:** Agregar cobertura de código mínima (70%)
- **Semana 4:** Configurar deploy automático a staging
