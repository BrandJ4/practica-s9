## Solución propuesta

### Respuesta inmediata (dentro de las primeras 2 horas)
1. **Crear hotfix branch** desde main:
```bash
git checkout main
git pull origin main
git checkout -b hotfix/bug-critico-descripcion
```
2. Asignar al desarrollador más familiarizado con el módulo afectado
3. Notificar al cliente proactivamente con ETA estimado

### Corrección focalizada
- Corregir SOLO el bug crítico, sin refactorizaciones adicionales
- Escribir test unitario que reproduzca el bug antes de corregirlo (TDD)
- Revisión de código express: al menos 2 personas revisan el fix

### Pruebas de regresión rápida
- Ejecutar suite de pruebas automatizadas
- Prueba manual del flujo crítico afectado
- Smoke test de las funcionalidades principales

### Merge y deploy
```bash
git checkout main
git merge hotfix/bug-critico-descripcion
git tag -a v1.0.1 -m "Hotfix: descripción del bug"
git push origin main --tags
```
