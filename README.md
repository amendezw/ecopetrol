# Wigilabs × Ecopetrol · Oportunidades tecnológicas

Sitio estático. No requiere build.

## Estructura
- `index.html` — sitio principal (mapa, Observabilidad, Ciberseguridad, IA, Automatización)
- `Momentum Ecopetrol.dc.html`, `BOb Ecopetrol.dc.html`, `MetaMAP Ecopetrol.dc.html` — demos que carga `index.html`
- `support.js` — runtime de los componentes
- `assets/`, `vendor/`, `_ds/` — imágenes, Leaflet + geometría de Colombia, tokens del sistema de diseño Wigi

## Subir a GitHub
```bash
git init
git add .
git commit -m "Wigilabs x Ecopetrol"
git branch -M main
git remote add origin https://github.com/<usuario>/<repo>.git
git push -u origin main
```

## Deploy en Vercel
1. vercel.com → Add New → Project → importar el repositorio.
2. Framework Preset: **Other**. Build Command: vacío. Output Directory: `./` (raíz).
3. Deploy.

O desde la terminal: `npx vercel --prod` dentro de esta carpeta.

## Notas
- Requiere conexión a internet para fuentes (Google Fonts, Fontshare) e íconos (Lucide, Tabler).
- `vercel.json` agrega `noindex` para que los buscadores no indexen el sitio. Elimínelo si quiere que sea indexable.
- No abrir `index.html` con doble clic (file://): las demos se cargan por fetch y necesitan un servidor. Para probar local: `npx serve .`
