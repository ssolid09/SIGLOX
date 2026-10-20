# SIGLOX · Sistema Integral de Gestión (versión con servidor)

Página estática en GitHub Pages + base de datos y login en Supabase.
Usuarios, permisos y datos de los 3 dashboards son los mismos en todos los dispositivos.

## 1. Crear el proyecto en Supabase (gratis)
1. Entra a supabase.com → **New project** (anota la contraseña de la base de datos; elige región cercana, p. ej. South America).
2. Menú **SQL Editor → New query** → pega el contenido de `supabase-setup.sql` → **Run**.
   Debe responder "Success". Crea el usuario maestro `sacc` con la clave inicial.
3. **Project Settings → API**: copia la **Project URL** y la clave **anon / publishable**.
   (Nunca uses la `service_role` ni la `secret`.)

## 2. Configurar la página
Abre `config.js` y pega la URL y la clave pública.

## 3. Publicar en GitHub Pages
Sube a un repositorio: `index.html`, `config.js`, `.nojekyll`, `README.md`.
**No subas `supabase-setup.sql`** (contiene la clave inicial del maestro).
Settings → Pages → Deploy from a branch → `main` / `(root)`.

## 4. Primer ingreso
- Entra como maestro y cambia la contraseña con **Cambiar contraseña**.
- Si ya tenías datos guardados en un navegador, haz el primer ingreso desde ese mismo navegador:
  se suben al servidor automáticamente (una sola vez por dispositivo).

## Respaldo de usuarios
En **Gestión de Usuarios** hay **Exportar** e **Importar**. El archivo incluye las contraseñas cifradas de los operadores: guárdalo en un lugar seguro y no lo subas a GitHub.
Importar crea los usuarios que falten y sobrescribe los que ya existan; el maestro y el SUPER nunca se modifican por importación.
Si instalaste Supabase antes de esta función, ejecuta una vez `supabase-actualizacion-exportar-importar.sql`.

## Notas
- Si dos personas editan el mismo dashboard a la vez, gana el último guardado.
- Los datos se descargan al abrir cada módulo; para ver cambios de otra persona, vuelve al menú y ábrelo de nuevo.
- Los proyectos gratuitos de Supabase se pausan tras una semana sin uso; se reactivan desde su panel.

© Elaborado por Santiago y Sebastián Chávez con fines educativos.
