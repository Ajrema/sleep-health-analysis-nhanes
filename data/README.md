# Data

This folder contains the original public-use SAS Transport files used in the project **Sleep Duration and Health Indicators Analysis**.

## Source

The data come from the **National Health and Nutrition Examination Survey (NHANES) 2017–2018**, produced by the National Center for Health Statistics, part of the U.S. Centers for Disease Control and Prevention (CDC).

Official documentation: [NHANES 2017–2018](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?BeginYear=2017)

The files are redistributed in their original `.xpt` format to make the analysis reproducible offline. They were not created or modified by the project author.

## Included modules

| File | NHANES module | Content used in the project |
|---|---|---|
| `DEMO_J.xpt` | Demographics | Age, gender, race/ethnicity, education, marital status, poverty index |
| `SLQ_J.xpt` | Sleep Disorders | Workday/weekend sleep, snoring, breathing interruptions, sleep trouble, daytime sleepiness |
| `BMX_J.xpt` | Body Measures | BMI and waist circumference |
| `GHB_J.xpt` | Glycohemoglobin | HbA1c |
| `BPX_J.xpt` | Blood Pressure | Systolic and diastolic blood pressure |
| `HDL_J.xpt` | HDL Cholesterol | HDL cholesterol |
| `PAQ_J.xpt` | Physical Activity | Recreation, transport activity, and sedentary time |
| `SMQ_J.xpt` | Smoking | Smoking history and status |
| `ALQ_J.xpt` | Alcohol Use | Alcohol-consumption frequency |

## Joining the files

All modules are merged using `SEQN`, NHANES's unique participant identifier.

```python
df = demo.merge(sleep, on="SEQN", how="left")
```

## Portable loading

The notebooks are stored in `notebooks/` and the data are stored in the sibling directory `data/`. The loading block supports execution either from the repository root or from inside `notebooks/`:

```python
from pathlib import Path
import pandas as pd

if Path("data").is_dir():
    DATA_DIR = Path("data")
elif Path("../data").is_dir():
    DATA_DIR = Path("../data")
else:
    raise FileNotFoundError("The data directory could not be found.")

demo = pd.read_sas(DATA_DIR / "DEMO_J.xpt")
sleep = pd.read_sas(DATA_DIR / "SLQ_J.xpt")
```

This avoids private absolute paths such as `C:\\Users\\...\\data` and allows another user to clone and run the project without editing the file locations.

## Usage note

NHANES data are public-use research data. Consult the official CDC/NCHS documentation for questionnaires, codebooks, variable definitions, and analytical guidance.
