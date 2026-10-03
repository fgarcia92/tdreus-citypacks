# TDReus — paquetes de ciudad (City Packs)

Paquetes de mapa que descarga el juego **TDReus (Defensa Reus)**. Son una base de datos derivada de **OpenStreetMap**.

**Datos © OpenStreetMap contributors, bajo la [Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/).**
Atribución y licencia: <https://www.openstreetmap.org/copyright>. El texto de la licencia está en [`LICENSE`](LICENSE).
*(English: map data packs for the TDReus game, a derivative database of OpenStreetMap, © OpenStreetMap contributors, ODbL 1.0.)*

## Qué hay aquí

Este repositorio **no contiene código del juego ni datos en el árbol de git**: solo este texto y la licencia. Los paquetes están en la
pestaña **Releases**. Cada release (`citypacks-<fecha>-<versión de las reglas>`) publica ficheros de nombre plano:

| Fichero | Qué es |
|---|---|
| `catalogue.json` | Catálogo (`tdreus.catalogue/1`): ciudades, sha256 y tamaño de cada paquete |
| `<ciudad>-<sha16>.zip` | El paquete de la ciudad (zip sin comprimir; lleva dentro `LICENSE.txt` con la atribución) |
| `<ciudad>-<sha16>.METHOD.txt` | Método (ODbL 4.6): extracto de OpenStreetMap de origen (fecha de réplica y md5), reglas de generación y comandos |

`<sha16>` son los 16 primeros caracteres del sha256 del paquete. Para comprobar un paquete: `shasum -a 256 <fichero>.zip` y compara
con el del catálogo o con `METHOD.txt`.

## Cómo se usa

El juego descarga el catálogo y los paquetes a través del servidor de TDReus, que sirve exactamente estos ficheros (y una página
`/odbl/` con la atribución y la descarga). No hace falta usar este repositorio a mano.

## Reutilizar los datos

Puedes reutilizar los paquetes bajo la ODbL 1.0: mantén la atribución «© OpenStreetMap contributors» y publica bajo la misma licencia
las bases de datos derivadas que distribuyas (ODbL 4.2, 4.3). Para obtener los datos originales actualizados, ve a OpenStreetMap.
