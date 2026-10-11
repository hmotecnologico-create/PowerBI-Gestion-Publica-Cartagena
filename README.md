# Power BI aplicado a la gestión pública · Cartagena

Datos de práctica del curso **Power BI aplicado a la gestión pública** (Plan Institucional de Capacitación de la Alcaldía de Cartagena · UNICOLOMBO, octubre de 2026). Docente: Heyder Medrano Olier.

> Ejercicio académico con datos públicos (Ley 1712 de 2014). No es una evaluación oficial; las cifras oficiales del Plan de Desarrollo son las de la Secretaría de Planeación.

## Cómo conectarse desde Power BI (ubicación web)

En Power BI Desktop: **Inicio → Obtener datos → Web** → pegar la dirección de la columna "Dirección para Power BI" → Aceptar.

| N.° | Tabla | Archivo | Dirección para Power BI (Obtener datos → Web) |
|---|---|---|---|
| 01 | Matriz de seguimiento del PDD | `01_PDD_Matriz_Seguimiento_dic2025.xlsx` | https://raw.githubusercontent.com/hmotecnologico-create/PowerBI-Gestion-Publica-Cartagena/main/fuentes/01_PDD_Matriz_Seguimiento_dic2025.xlsx |
| 02 | F11 – Programas y proyectos de inversión | `02_F11_Programas_Proyectos_dic2025.xlsx` | https://raw.githubusercontent.com/hmotecnologico-create/PowerBI-Gestion-Publica-Cartagena/main/fuentes/02_F11_Programas_Proyectos_dic2025.xlsx |
| 03 | Ejecución presupuestal de gastos | `03_Ejecucion_Presupuestal_Gastos_ny6j-ysx3.csv` | https://raw.githubusercontent.com/hmotecnologico-create/PowerBI-Gestion-Publica-Cartagena/main/fuentes/03_Ejecucion_Presupuestal_Gastos_ny6j-ysx3.csv |
| 04 | SECOP II – BPIN por proceso | `04_SECOPII_BPIN_por_Proceso_Cartagena_2024-2025_d9na-abhe.csv` | https://raw.githubusercontent.com/hmotecnologico-create/PowerBI-Gestion-Publica-Cartagena/main/fuentes/04_SECOPII_BPIN_por_Proceso_Cartagena_2024-2025_d9na-abhe.csv |
| 05 | SECOP II – Contratos electrónicos 2025 | `05_SECOPII_Contratos_Alcaldia_2025_jbjy-vk9h.xlsx` | https://raw.githubusercontent.com/hmotecnologico-create/PowerBI-Gestion-Publica-Cartagena/main/fuentes/05_SECOPII_Contratos_Alcaldia_2025_jbjy-vk9h.xlsx |

## De dónde salen las tablas (fuente oficial)

| N.° | Publica | Página oficial | Corte | Descargado |
|---|---|---|---|---|
| 01 | Secretaría de Planeación Distrital | [cartagena.gov.co – Seguimiento planes de acción a 31-dic-2025](https://www.cartagena.gov.co/transparencia/4planeacion-presupuesto-informes/43-plan-accion/seguimiento-planes-acciones-institucionales-corte-31-diciembre-2025) | 31-dic-2025 | 05-10-2026 |
| 02 | Alcaldía de Cartagena (Banco de Programas y Proyectos) | [cartagena.gov.co – F11 diciembre 2025](https://www.cartagena.gov.co/transparencia/4planeacion-presupuesto-informes/informacion-ejecucion-presupuestal-contractual-contable-financiera-programas-proyectos-diciembre-2025) | dic-2025 | 05-10-2026 |
| 03 | Alcaldía de Cartagena, en datos.gov.co | [ny6j-ysx3](https://www.datos.gov.co/Hacienda-y-Cr-dito-P-blico/Ejecuci-n-Presupuestal-de-gastos-Distrito-de-Carta/ny6j-ysx3) | 2025 (dic) y 2026 (ago) | 06-10-2026 |
| 04 | Colombia Compra Eficiente, en datos.gov.co | [d9na-abhe](https://www.datos.gov.co/d/d9na-abhe) (filtro: BPIN de Cartagena, vigencias 2024 y 2025) | Diario | 06-10-2026 |
| 05 | Colombia Compra Eficiente, en datos.gov.co | [jbjy-vk9h](https://www.datos.gov.co/d/jbjy-vk9h) (filtro: Alcaldía NIT 890480184, firmados en 2025; pasado a Excel) | Diario | 06-10-2026 |

El detalle de cada fuente (cómo se descargó, qué representa una fila, qué hoja cargar y número de filas) está en [`fuentes/00_Ficha_Procedencia.xlsx`](fuentes/00_Ficha_Procedencia.xlsx).

**Las tablas se publican tal como se descargaron**, sin limpiar: la limpieza y el modelo se hacen en clase con Power Query. Los contratos no incluyen nombres, documentos ni cuentas bancarias de personas (minimización de datos).
