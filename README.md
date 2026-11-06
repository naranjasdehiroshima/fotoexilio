# El exilio en la Ciudad de México, antes y ahora

Proyecto de refotografía sobre los lugares del exilio republicano español en la Ciudad de México (1939 en adelante). Cada lugar reúne la fotografía de archivo, el punto exacto donde se tomó, su estado actual y una toma nueva hecha desde el mismo ángulo.

Piloto: 25 lugares.

## Estructura

```
index.html            Sitio (GitHub Pages): mapa, filtros y comparador antes/ahora
data/lugares.json     Una entrada por lugar; es la fuente única de datos
fotos/antes/          Fotos de archivo (solo con permiso del fondo; ver abajo)
fotos/ahora/          Refotografías propias
docs/metodo.md        Cómo se busca, se ubica y se refotografía cada lugar
```

## Estados

| Código | Significado |
|---|---|
| `A` | Foto identificada: hay una toma concreta con signatura y el lugar existe |
| `B` | Lugar seguro: la dirección está documentada; falta localizar la toma en el fondo |
| `C` | Por ubicar: existe la foto o la institución, pero no su punto exacto |

## Campos de `lugares.json`

| Campo | Contenido |
|---|---|
| `id` | Número de ficha, `01`–`25` |
| `estado` | `A`, `B` o `C` |
| `titulo`, `fecha` | Nombre del lugar o la escena, y fecha de la foto de archivo |
| `fondo`, `toma` | Archivo de procedencia y signatura o pie de la foto |
| `lugar`, `hoy` | Dirección histórica y estado actual con su fuente |
| `coords` | `[lat, lng]` o `null` |
| `coords_verificadas` | `false` mientras sean aproximadas; `true` tras verificar en campo |
| `foto_antes`, `credito_antes` | Ruta en `fotos/antes/` y crédito completo del fondo |
| `foto_ahora`, `fecha_refoto` | Ruta en `fotos/ahora/` y fecha ISO de la toma |
| `fuentes` | Lista de `{titulo, url}` |

El comparador deslizable aparece en una ficha en cuanto tiene `foto_antes` y `foto_ahora`.

## Ver el sitio en local

```
python3 -m http.server
```
y abrir http://localhost:8000 (abrir `index.html` directamente no carga el JSON).

## Publicar

Settings → Pages → Deploy from a branch → `main` / root.

## Derechos

- **Código:** MIT.
- **Datos (`data/`) y refotografías propias (`fotos/ahora/`):** CC BY-SA 4.0.
- **Fotos de archivo (`fotos/antes/`):** conservan los derechos de su fondo (AGN, Hermanos Mayo, Ateneo Español de México, etc.). Solo se suben con autorización y con su crédito en `credito_antes`. Mientras no haya permiso, la ficha enlaza al fondo en lugar de reproducir la imagen.

## Referencias

- Archivo General de la Nación, Archivo Fotográfico Hermanos Mayo
- [Mapa colaborativo del exilio español en México](https://exilio3639.org/) (VHPlab y GPS Museum)
- Ateneo Español de México; Centro de Memoria Histórica del Colegio Madrid
