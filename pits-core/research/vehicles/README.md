# /research/vehicles — Ontología Automotriz Colombiana

## Propósito

Esta carpeta contiene el activo técnico diferencial más importante de PITS MARKET: la base de datos de vehículos, modelos, motorizaciones y compatibilidades específica para el mercado colombiano.

> **Por qué es nuestro mayor diferencial:** Ningún proveedor externo tiene esta información para Colombia. Los datos de CARFAX y AutoData son para EEUU/Europa. Las versiones que llegan a Colombia via importación directa, las versiones JDM que circulan en el país, y los años específicos de los modelos vendidos aquí — solo lo sabemos nosotros, con la comunidad.

---

## Qué contiene

| Documento | Descripción |
|-----------|-------------|
| `database-makes-colombia.md` | Todas las marcas presentes en Colombia |
| `database-bmw-models-colombia.md` | Modelos BMW en Colombia con años y motorizaciones |
| `database-vag-models-colombia.md` | VW, Audi, Seat, Skoda en Colombia |
| `database-honda-models-colombia.md` | Honda Colombia con motorizaciones JDM y USDM |
| `database-subaru-mitsubishi-colombia.md` | JDM performance cars en Colombia |
| `database-engine-codes.md` | Todos los códigos de motor con specs y aliases |
| `database-platform-compatibility.md` | Plataformas compartidas y compatibilidades cruzadas |

---

## Cómo Contribuir a la Ontología

La ontología mejora con el conocimiento de la comunidad. El proceso:

1. Abrir un Issue con el label `area: research` y el título `[VEHICLES] Agregar [Modelo] [Año]`
2. Incluir: modelo exacto, año de producción para Colombia, motorización con código, versiones disponibles
3. Verificar con dos fuentes independientes antes de agregar
4. Agregar nota de fuente al documento

---

## Convención de Nombres

```
database-[marca/tipo]-[descripcion]-[fecha-si-versioned].md

Ejemplos:
  database-bmw-models-colombia.md
  database-engine-codes.md
  database-platform-compatibility.md
  database-import-vehicles-colombia.md
```

---

*Esta base de datos es de acceso público para la comunidad. Es uno de los activos que consideramos open source para construir confianza con el ecosistema.*
