# SIGLOX · Sistema Integral de Gestión

Plataforma de logística con login, usuario maestro, roles y permisos por módulo
(Reporte Devoluciones Móviles, Nivel de Servicio Móviles, Reporte de Móviles, Gestión de Usuarios).

Es un único archivo (`index.html`) sin dependencias ni servidor.

## Publicar en GitHub Pages

1. En GitHub: **New repository** → nombre `siglox` → **Create repository**.
2. **Add file → Upload files** → sube `index.html`, `.nojekyll` y `README.md` → **Commit changes**.
3. **Settings → Pages → Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **main** · carpeta **/ (root)** → **Save**.
4. En 1–2 minutos queda en: `https://TU-USUARIO.github.io/siglox/`

### Con Git (alternativa)

```bash
git init
git add .
git commit -m "SIGLOX v1"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/siglox.git
git push -u origin main
```

## Actualizar

Reemplaza `index.html` en el repositorio (o haz `git push`). Los usuarios ya creados no se pierden,
porque viven en el navegador de cada persona, no en el archivo.

## Importante

- Los usuarios y datos se guardan en el navegador (localStorage): no se comparten entre equipos.
- El sitio de GitHub Pages es público: el login limita el uso de la app, pero no es seguridad real,
  porque el código (incluido el hash de la clave inicial del maestro) es visible para cualquiera.
- Se recomienda cambiar la clave del maestro en el primer ingreso con **Cambiar contraseña**.

© Elaborado por Santiago y Sebastián Chávez con fines educativos.
