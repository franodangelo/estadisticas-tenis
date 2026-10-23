# Estadísticas de Tenis

App web de una sola página para llevar estadísticas de tenis punto a punto, con análisis
y devolución para el jugador. No necesita servidor ni base de datos: todo se guarda en el
navegador de cada persona (localStorage).

- `index.html` — la app completa (HTML + CSS + JS, todo embebido).
- `vercel.json` — configuración mínima para Vercel (static, URLs limpias).

## Subirla a Vercel

Es un sitio estático: no hay build ni backend. Tres formas, de la más simple a la más
"profesional":

### Opción A — Arrastrar y soltar (lo más rápido)
1. Entrá a https://vercel.com/new (iniciá sesión o creá una cuenta gratis).
2. Buscá la opción de desplegar sin Git / "deploy a static project".
3. Arrastrá **la carpeta `tennis-web`** (que contiene `index.html`).
4. Deploy. En segundos te da una URL pública (p. ej. `tennis-stats.vercel.app`) para
   compartir con tus amigos.

### Opción B — Vercel CLI (desde tu terminal)
```bash
npm i -g vercel          # instalar la CLI (una vez)
cd tennis-web            # entrar a la carpeta del proyecto
vercel login             # iniciar sesión en tu cuenta
vercel                   # deploy de previsualización (te hace unas preguntas; aceptá las de por defecto)
vercel --prod            # publicar en producción (URL definitiva)
```

### Opción C — Desde GitHub (deploys automáticos en cada cambio)
1. Creá un repo en GitHub y subí el contenido de `tennis-web`.
2. En https://vercel.com/new elegí "Import Git Repository" y seleccioná ese repo.
3. Framework Preset: **Other** (es estático, sin build). Deploy.
4. Desde ahí, cada `git push` genera un nuevo deploy automático.

## Notas
- Los datos (partidos, comentarios, historial) se guardan en el navegador de cada usuario,
  no se comparten entre personas ni entre dispositivos. Cada amigo arma su propio historial.
- Para un nombre más lindo podés agregar un dominio propio en Vercel → Settings → Domains.
