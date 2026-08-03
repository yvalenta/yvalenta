# El CV — `index.html`

La hoja de vida pública de Yonatan Valencia. Un solo archivo HTML autocontenido:
se abre con doble clic y se ve igual que publicado. Sin build.

Está en la **raíz del repo a propósito**, no en una subcarpeta: es lo que este
repo publica. GitHub Pages copia un `index.html` sin front matter tal cual, así
que lo que se ve es exactamente lo que hay acá.

## Dónde se ve hoy, y dónde debería verse

Medido el 2026-08-03:

| URL | Qué sirve hoy |
|---|---|
| `https://yvalenta.github.io/yvalenta/` | **este repo**, por GitHub Pages |
| `https://cv.ynt.codes` | un **Worker de Cloudflare** (`hidden-art-0f96`) con su propia copia, sin fuente en ningún repo |

Los dos publican un CV y **no son el mismo archivo**: al medirlo, el Worker
servía 21.685 bytes y este repo 32.848. Ahí está toda la explicación de por qué
el CV publicado se quedaba atrás — actualizarlo exigía acordarse de pegar el
HTML en el panel de Cloudflare.

## Para que `cv.ynt.codes` sea este repo

Tres pasos, **en este orden**. El segundo sin el primero deja el sitio
inalcanzable: al aparecer un `CNAME`, Pages deja de servir en `github.io` y
empieza a esperar el dominio propio.

1. En Cloudflare: borrar el registro de `cv.ynt.codes` que apunta al Worker y
   crear un `CNAME` a `yvalenta.github.io` **sin proxy** (nube gris). Con el
   proxy encendido, la validación del dominio de Pages no pasa.
2. En este repo: `Settings → Pages → Custom domain` = `cv.ynt.codes`. Eso crea
   el archivo `CNAME` en la raíz.
3. Esperar el certificado y marcar *Enforce HTTPS*.

Desde entonces, publicar el CV es `git push`.

Hasta que eso pase, `cv.ynt.codes` sigue mostrando la copia vieja del Worker: no
hay forma de actualizarla desde acá.

## Comprobar lo servido, no lo editado

```bash
curl -s https://cv.ynt.codes/ | diff - index.html && echo "lo servido = lo del repo"
```

Se compara contra **lo que responde el dominio**, no contra lo que dice el
editor. Un archivo correcto en disco no prueba nada sobre lo publicado.
