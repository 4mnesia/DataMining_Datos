# DataMining_Datos

Repositorio liviano para usar el dataset de precipitaciones en Colab y VSCode.

## Archivos

- `dataset_precipitaciones_diarias_chile_COMPLETO.csv`: serie diaria de precipitaciones por estacion.
- `getEstacionesRedEma.json`: metadata de estaciones meteorologicas.

## Uso en VSCode

```python
from pathlib import Path
import json
import pandas as pd

base_path = Path(".")

df = pd.read_csv(
    base_path / "dataset_precipitaciones_diarias_chile_COMPLETO.csv",
    parse_dates=["fecha"],
)

meta_json = json.loads(
    (base_path / "getEstacionesRedEma.json").read_text(encoding="utf-8")
)
```

## Uso en Colab

```python
!git clone https://github.com/TU_USUARIO/DataMining_Datos.git
%cd DataMining_Datos
```

Luego puedes usar el mismo codigo de carga de VSCode.

