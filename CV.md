# El CV — `index.html`

La hoja de vida pública de Yonatan Valencia. Un solo archivo HTML autocontenido:
se abre con doble clic y se ve igual que publicado. Sin build.

Está en la **raíz del repo a propósito**, no en una subcarpeta: es lo que este
repo publica. GitHub Pages copia un `index.html` sin front matter tal cual, así
que lo que se ve es exactamente lo que hay acá.

## Dónde se ve

Medido el 2026-08-11, tras la migración:

| URL | Qué sirve |
|---|---|
| `https://cv.ynt.codes` | **este repo**, por GitHub Pages — dominio propio, HTTPS forzado |
| `https://yvalenta.github.io/yvalenta/` | lo mismo (Pages redirige al dominio propio) |

**Publicar el CV es `git push`.** El `CNAME` de la raíz es lo que ata el
dominio; borrarlo lo desata.

## La migración, ya ejecutada (2026-08-11)

`cv.ynt.codes` fue un **Worker de Cloudflare** (`hidden-art-0f96`) con su propia
copia pegada a mano, sin fuente en ningún repo: al medirlo el 2026-08-03, el
Worker servía 21.685 bytes y este repo 32.848 — el CV publicado se quedaba
atrás porque actualizarlo exigía acordarse de pegar el HTML en el panel.

Los tres pasos que lo arreglaron, **en este orden** (el segundo sin el primero
deja el sitio inalcanzable):

1. En Cloudflare: soltar el *custom domain* del Worker y crear un `CNAME` a
   `yvalenta.github.io` **sin proxy** (nube gris) — con proxy, la validación
   del dominio de Pages no pasa.
2. En este repo: el archivo `CNAME` en la raíz + custom domain en Pages.
3. Esperar el certificado y marcar *Enforce HTTPS*.

El Worker `hidden-art-0f96` quedó vivo en la cuenta, ya sin dominio: no sirve
nada y no cuesta nada, pero que nadie lo redescubra como "el CV".

## Comprobar lo servido, no lo editado

```bash
curl -s https://cv.ynt.codes/ | diff - index.html && echo "lo servido = lo del repo"
```

Se compara contra **lo que responde el dominio**, no contra lo que dice el
editor. Un archivo correcto en disco no prueba nada sobre lo publicado.
