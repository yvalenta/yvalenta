# cv.ynt.codes

Fuente del CV público de Yonatan Valencia: **`index.html`**, un solo archivo
autocontenido (HTML + CSS embebido, sin build, sin dependencias más allá de la
fuente Inter de Google Fonts).

| | |
|---|---|
| URL pública | https://cv.ynt.codes/ |
| Qué lo sirve | Un Worker de Cloudflare llamado **`hidden-art-0f96`** |
| Cómo se despliega hoy | A mano, desde el dashboard de Cloudflare |
| Build | Ninguno. Lo que está en `index.html` es lo que se sirve |

## Por qué vive acá

Hasta el 2026-08-03 **este archivo no tenía repo**: el Worker se editó siempre
desde el dashboard, así que la única copia era la desplegada. Un cambio malo no
se podía revertir y no había historia de qué decía el CV en qué fecha.

Este repo (`yvalenta/yvalenta`) ya es donde vive la identidad pública de
Yonatan —el README del perfil de GitHub, el diagrama de arquitectura del home
lab, el grafo de skills—, así que el CV es del mismo género que lo que ya
guarda. Los otros dos candidatos no servían: `cv-project/far-flare` es un
scaffold de Astro sin un solo commit, y meter un HTML plano ahí implicaría un
build que este artefacto no tiene; `cv_manager` es **otra cosa**, una app para
gestionar CVs, no este sitio.

> **GitHub Pages está apagado en este repo** (`yvalenta.github.io` responde
> 404), así que agregar esta carpeta no publica una segunda copia del CV por
> accidente. Si algún día se enciende Pages, hay que excluir `cv.ynt.codes/` en
> `_config.yml` — o el CV pasaría a servirse desde dos lugares distintos, que
> es exactamente el problema que este repo viene a cerrar.

## Desplegar

**Hoy, que es como está funcionando:**

1. Cloudflare Dashboard → Workers & Pages → `hidden-art-0f96` → *Edit code*.
2. Reemplazar el HTML embebido en el Worker por el contenido de `index.html`.
3. *Deploy*, y comprobar lo **servido**, no el editor:

```bash
curl -s https://cv.ynt.codes/ | diff - index.html && echo "servido == repo"
```

Ese `diff` es el punto: un 200 no prueba que se desplegó **esta** versión. Si
sale distinto, el Worker sigue sirviendo lo viejo (la propagación entre POPs
tarda; un cache-buster en la URL no la esquiva, hay que esperar y volver a
medir).

**Lo que todavía no existe:** no hay `wrangler.toml` ni deploy automatizado. Si
se quiere, el camino es un `wrangler deploy` que lea este archivo en vez de
tener el HTML pegado adentro del script — pero mientras no esté, el paso 3 es
obligatorio, porque es lo único que ata este repo a lo que ve un tercero.

## Editar

Es un archivo, se edita con un editor de texto. Dos cosas que conviene no
romper:

- **El sistema de diseño está en el `:root`** — tema oscuro, `--accent: #6C63FF`,
  tipografía Inter. Las secciones nuevas se construyen con las clases que ya
  existen (`.section-label`, `.skill-group`, `.project`, `.job-tools`, `.tool`)
  para que se vean nativas.
- **El CV está en inglés.** Los nombres propios de productos en español
  (*Simulador de Abonos a Capital*) se dejan tal cual.
