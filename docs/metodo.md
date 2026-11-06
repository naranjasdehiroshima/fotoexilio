# Método

## 1. Localizar la foto de archivo
1. Buscar en el fondo indicado en `fondo` y anotar la signatura exacta en `toma`.
2. Hacer búsqueda inversa (Google Lens y Yandex) para encontrar otras copias con mejor pie: fecha, lugar, nombres.
3. Cruzar con los nodos del [Mapa colaborativo](https://exilio3639.org/), que ya vienen geolocalizados.

## 2. Ubicar el punto de toma
- Buscar referencias fijas: letreros, números de calle, esquinas, cornisas, edificios de fondo, vías de tranvía.
- Contrastar con planos de época y con la aérea de la Fundación ICA cuando exista.
- Tener presente que muchas calles cambiaron de nombre y muchos edificios del Centro cayeron en el sismo de 1985.
- Guardar `coords` y dejar `coords_verificadas: false` hasta estar en el sitio.

## 3. Refotografiar
- Ir al punto, igualar altura de cámara, ángulo y distancia focal aparente. Llevar impresa la foto original.
- Hacer varias tomas con pequeños desplazamientos; elegir la que mejor alinee las líneas fijas.
- Nombrar el archivo `fotos/ahora/<id>.jpg` y anotar `fecha_refoto` (AAAA-MM-DD).
- Marcar `coords_verificadas: true`.

## 4. Publicar la ficha
- Subir la foto de archivo a `fotos/antes/<id>.jpg` solo con permiso del fondo, con `credito_antes` completo.
- Actualizar `estado` a `A` cuando la toma y el lugar estén confirmados.
