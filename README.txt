# Nexans Cable Calculator (Excel-backed)

Files:
- `index.html` - calculator UI that reads workbook data
- `cable_data.xlsx` - editable data source
- `PowerCableCatalogue2019.pdf` - original uploaded catalogue (not included in the zip unless you want it)
- `README.txt` - this file

How it works:
1. Put `index.html` and `cable_data.xlsx` in the same folder.
2. Open `index.html` locally or publish both files to GitHub Pages.
3. The app loads `cable_data.xlsx` automatically.
4. You can also upload a replacement workbook from the UI.

Workbook structure:
- `LV_CalcData` - normalized LV rows used by the app
- `MV_CalcData` - normalized MV rows used by the app
- `HV_CalcData` - empty template for future HV rows
- helper sheets for short-circuit, resistance, reactance, and config

Important:
- Keep the column names the same if you edit the workbook.
- For LV, the app uses the selected `ampacity_col_n_A` column.
- For MV/HV, the app uses `ampacity_air_A`, `ampacity_direct_buried_A`, or `ampacity_duct_A`.

Notes:
- The uploaded catalogue provides LV data and MV data up to 33 kV.
- `HV_CalcData` is left as a template for future extension.
