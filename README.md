# Excell
Exportación e Importación a Excell

# Instalamos la libreria
```
pip install openpyxl

```

# Creamos save.py
```
# -*- coding: utf-8 -*-

from openpyxl import Workbook

wb = Workbook()

# grab the active worksheet
ws = wb.active

# Data can be assigned directly to cells
ws['A1'] = 42
ws['A2'] = 142

# Utilizando formulas
ws["B1"] = "=SUM(A1,A2)"

# Rows can also be appended
ws.append([1, 2, 3])

# Python types will automatically be converted
import datetime
ws['A3'] = datetime.datetime.now()

# Save the file
wb.save("sample.xlsx")
```
