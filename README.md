# Página personal académica — Pablo Borrego Ramos

Sitio estático puro (HTML/CSS, sin JavaScript ni proceso de build) para GitHub Pages.
Sitio en producción: https://pabloalmendralejo.github.io

## Estructura

```
website/
├── index.html            # Bio, foto, intereses de investigación, contacto
├── publications.html     # Publicaciones y working papers
├── projects.html         # Proyectos de software e investigación
├── 404.html              # Página de error personalizada
├── assets/
│   ├── style.css         # Única hoja de estilos compartida
│   ├── photo.jpg         # Foto de perfil (≤ 60 KB, JPEG/WebP)
│   └── favicon.svg
└── README.md
```

Nota: `assets/photo.jpg` es un marcador de posición; sustitúyelo por la foto real
(máximo 60 KB en JPEG o WebP). El CV en PDF se añadirá más adelante.

## Previsualización local

Desde este directorio, lanza un servidor estático con Python:

```bash
python -m http.server 8000
```

y abre http://localhost:8000 en el navegador. Cualquier otro servidor estático
sirve igualmente; no hay build ni dependencias.

## Despliegue

El contenido de este directorio se corresponde 1:1 con el repositorio
`PabloAlmendralejo.github.io`:

1. Copia (o versiona directamente) el contenido en el repo público
   `PabloAlmendralejo.github.io`.
2. Haz push a la rama `main`:

   ```bash
   git add -A && git commit -m "Update site" && git push origin main
   ```

3. GitHub Pages despliega automáticamente (~1 minuto) mediante el workflow
   `pages-build-deployment`.
4. En Settings → Pages, comprueba que "Enforce HTTPS" está activado.

El sitio queda publicado en https://pabloalmendralejo.github.io
