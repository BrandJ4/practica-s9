## Solución propuesta

### Herramienta única: GitHub Projects
Por estar el código ya en GitHub, usar GitHub Projects elimina el cambio de contexto.

#### Configuración del tablero
```
Columnas:
📋 Backlog → 🎯 Sprint Actual → 🔄 En Progreso → 👀 En Revisión → ✅ Hecho
```

#### Vinculación con Issues y PRs
- Cada tarea del tablero está ligada a un Issue de GitHub
- Los PRs se vinculan automáticamente al Issue con: `Closes #N`
- El Issue se cierra automáticamente al mergear el PR

### Convención de etiquetas (Labels)
- `priority: high` / `priority: medium` / `priority: low`
- `type: feature` / `type: bugfix` / `type: documentation`
- `status: blocked`
