## Solución propuesta

### 1. Estrategia de ramas (Git Flow simplificado)
```
main          ← producción estable
develop       ← integración continua
feature/xxx   ← desarrollo de cada issue
hotfix/xxx    ← correcciones urgentes
```

### 2. Ramas de vida corta
Cada rama de feature debe vivir máximo 2-3 días. Las ramas longevas son la principal causa de conflictos.

### 3. Pull Requests obligatorios con revisión
Nadie mergea directamente a `main` o `develop`. Todo cambio pasa por PR con al menos 1 revisor.

### 4. Sincronización frecuente
```bash
# Cada mañana antes de trabajar:
git fetch origin
git rebase origin/develop
```

### 5. Comunicación antes de tocar archivos compartidos
Si dos personas necesitan modificar el mismo archivo, coordinar quién va primero.
