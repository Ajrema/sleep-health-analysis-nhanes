# Datos del proyecto

Esta carpeta contiene los archivos originales utilizados en el proyecto:

**Asociación entre la duración del sueño, las características demográficas, los indicadores de salud y los factores del estilo de vida: un análisis transversal utilizando datos de NHANES 2017–2018.**

## Fuente de los datos

Los datos proceden de la encuesta pública **National Health and Nutrition Examination Survey (NHANES) 2017–2018**, desarrollada por el National Center for Health Statistics de los Centers for Disease Control and Prevention (CDC) de Estados Unidos.

Los archivos se distribuyen originalmente en formato SAS Transport (`.xpt`).

Fuente oficial:  
https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2017

## Archivos incluidos

| Archivo | Contenido |
|---|---|
| `DEMO_J.xpt` | Datos demográficos |
| `SLQ_J.xpt` | Duración y hábitos del sueño |
| `PAQ_J.xpt` | Actividad física |
| `SMQ_J.xpt` | Consumo de tabaco |
| `ALQ_J.xpt` | Consumo de alcohol |
| `BMX_J.xpt` | Mediciones corporales y antropometría |
| `GHB_J.xpt` | Hemoglobina glucosilada (HbA1c) |
| `BPX_J.xpt` | Mediciones de presión arterial |
| `HDL_J.xpt` | Colesterol HDL |

## Uso de los datos

Los archivos se cargan en el notebook mediante rutas relativas, permitiendo que el proyecto pueda ejecutarse en diferentes ordenadores y sistemas operativos.

Ejemplo:

```python
from pathlib import Path
import pandas as pd

DATA_DIR = Path("data")

demo = pd.read_sas(DATA_DIR / "DEMO_J.xpt")
sleep = pd.read_sas(DATA_DIR / "SLQ_J.xpt")
body = pd.read_sas(DATA_DIR / "BMX_J.xpt")
