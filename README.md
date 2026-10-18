# jellyfin-plugins-repo

Repositorio personal de plugins de Jellyfin. El workflow `publish.yml`
compila los plugins y publica `manifest.json` + los `.zip` en GitHub Pages.

## Uso en Jellyfin

**Panel → Plugins → Repositories → +** y añade:

```
https://nen155.github.io/jellyfin-plugins-repo/manifest.json
```

Tras guardar, los plugins aparecerán en el catálogo con instalación y
actualización automática.

## Plugins incluidos

| Plugin | Repositorio |
|---|---|
| Media Only Filter | [Jellyfin.Plugin.MediaOnly](https://github.com/nen155/Jellyfin.Plugin.MediaOnly) |
| Gallery Optimizer | [Jellyfin.Plugin.GalleryOptimizer](https://github.com/nen155/Jellyfin.Plugin.GalleryOptimizer) |
| Photo Thumbnails | [Jellyfin.Plugin.PhotoThumbs](https://github.com/nen155/Jellyfin.Plugin.PhotoThumbs) |

## Regenerar el repositorio

El workflow se ejecuta semanalmente, en cada push a `main`, o manualmente
desde **Actions → Build plugin repository → Run workflow**. Coge el `main`
de cada repo de plugin, compila con jprm y redeploya el manifest.
