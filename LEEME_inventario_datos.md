# Inventario de datos – Heladas Paipa-Duitama
Descarga: 13-14 nov 2026. Fuentes: IDEAM (radicado 20269910177444, respuesta 20262010187481) y Portal de Datos Abiertos (datos.gov.co, IDEAM).

## 1. IDEAM_radicado_20269910177444/ (respuesta oficial a la solicitud; formato .data, separador |)
| Archivo | Estación | Variable | Periodo |
|---|---|---|---|
| TSSM_MN_D@24035120 | Surbatá Bonza (conv.) | Tmín diaria | 2015-01 a 2026-10 (3 801 días) |
| TSSM_MX_D@24035120 | Surbatá Bonza | Tmáx diaria | 2015-2026 |
| TSSM_MEDIA_D@24035120 | Surbatá Bonza | T media diaria | 2015-2026 |
| HR_CAL@24035120 | Surbatá Bonza | Humedad relativa 7/13/19 h | 2015-2026 |
| PTPM_CON@24035120 | Surbatá Bonza | Precipitación diaria | 2015-2026 |
| BSHG_CON@24035120 | Surbatá Bonza | Brillo solar horario | 2015-2024 |
| TSSM_MN_D@24035430 | Tunguavita (conv.) | Tmín diaria | 2015-03 a 2026-10 (4 104 días) |
| BSHG_CON@24035430 | Tunguavita (conv.) | Brillo solar horario | 2015-2025 |
| PTPM_CON@24030350 | Duitama (pluviográfica) | Precipitación diaria | 2000-2026 |
| PTPM_CON@24030410 | Tibasosa (pluviométrica) | Precipitación diaria | 2000-2025 |
Además: Glosario de variables, Catálogo Nacional de Estaciones (CNE), formato M-SC-F005 e instructivos.
No entregado por el IDEAM: evaporación (EVTE) ni viento de Surbatá.

## 2. datos_abiertos_horarios/ (datos.gov.co, datos preliminares sin validar)
| Estación | Variables | Periodo |
|---|---|---|
| Tunguavita AUT (0024035430) | tmin, temp, tmax, hr (horario); vv, dv, prec, pres (10 min) | 2005-2026 (sin 2024) |
| Duitama AUT (2403500041) | las mismas | 2019-03 a 2026-11 |

## 3. Pendiente
- Corpoboyacá: Vía Pantano de Vargas AUT (2403500369) y Vereda Aguatendida AUT (2403500370). El IDEAM remitió la petición por competencia (radicado 20262010185321, 3 nov 2026). Sin respuesta aún. No están en datos.gov.co.

## 4. Hallazgos de calidad (para el control de calidad del OE1)
- Ceros como código de error: Tmín Duitama AUT tiene 1 222 registros en 0,0 (cientos de días en 2024-2026) y Temp Aire Tunguavita 6 596; aparecen a cualquier hora, así que no son heladas.
- El conjunto "Temp Aire 2 m" no contiene ningún valor negativo en 20 años: los negativos solo aparecen en el conjunto de Tmín. Etiquetar heladas con Tmín, no con la temperatura horaria.
- Atípicos: Tmín Tunguavita -14,9 °C, Tmáx 49,9 °C, presión 600-1183 hPa, viento hasta 79,6 m/s.
- Cobertura baja: Duitama AUT 2023 (16 %) y 2024 (19 %); Tunguavita AUT sin datos en 2024 y 33 % en 2017 y 2023.
- Tunguavita AUT marca 31 noches bajo 0 °C en 2014, varias en julio-septiembre (fuera de temporada); en 2015 marca 6 donde la convencional marca 0. Posible deriva del sensor.

## 5. Noches de helada (Tmín < 0 °C, tras quitar ceros y atípicos)
| Estación | Noches con dato | Heladas | Tmín ≤ 2 °C |
|---|---|---|---|
| Tunguavita AUT (2005-2026) | 6 360 | 68 | 422 |
| Tunguavita conv. (2015-2026) | 4 104 | 6 | 34 |
| Surbatá conv. (2015-2026) | 3 801 | 2 | 24 |
| Duitama AUT (2019-2026) | 1 920 | 5 | 24 |
Fechas confirmadas por dos instrumentos: 2016-01-15, 2017-02-07, 2020-01-10, 2020-02-06.
Detalle por año: resumen_heladas_por_estacion_anio.csv
