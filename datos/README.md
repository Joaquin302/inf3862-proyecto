# Datos

Los datasets **no se suben al repositorio** (≈ 450 MB). Descárgalos desde Canvas (módulo del
proyecto) y déjalos en esta carpeta con exactamente esta estructura:

```text
datos/
└── foodcom/
    ├── recipes.parquet                 Food.com · 522 517 recetas (179 MB)
    ├── reviews.parquet                 Food.com · 1 401 982 reseñas (174 MB)
└── wearable/
    ├── LEEME.md                    descripción oficial de los archivos del wearable
    ├── dispositivos.csv            315 relojes de 300 usuarios
    ├── sesiones.jsonl              4 840 sesiones de actividad
    ├── comidas.csv                 22 106 recetas preparadas
    └── mediciones/AAAA-MM-DD/HH.jsonl.gz
                                    1 449 archivos (116 MB comprimidos, ≈ 2,3 GB descomprimidos),
                                    15,5 M mediciones agrupadas por día y hora de RECEPCIÓN
```

Todas las fechas del wearable están en UTC; `zona_horaria` de `dispositivos.csv` permite pasar a
hora local. El período cubierto por el wearable es del 16-dic-2007 al 14-feb-2008 (61 días).

Los dos modelos de reloj usan nombres distintos en los lotes de mediciones:

| Pulso S | FitBand 2 |
|---|---|
| `device_id`, `ts_medicion` (ISO 8601), `ts_recepcion`, `frecuencia_cardiaca`, `pasos`, `calorias` | `dev`, `timestamp` (epoch ms), `received_at`, `fc`, `steps`, `kcal` |


