# Power BI aplicado a la gestión pública · Cartagena

Datos de práctica del curso **Power BI aplicado a la gestión pública** (Plan Institucional de Capacitación de la Alcaldía de Cartagena · UNICOLOMBO, octubre de 2026). Docente: Heyder Medrano Olier.

> Ejercicio académico con datos públicos (Ley 1712 de 2014). No es una evaluación oficial; las cifras oficiales del Plan de Desarrollo son las de la Secretaría de Planeación.

## Tutoriales

- [Encuentro 1 · Tutorial del estudiante (PDF)](tutoriales/E1_Tutorial_Estudiante.pdf): inteligencia de negocios, Power BI, la ventana y sus vistas, tipos de datos y primeras visualizaciones. *Nota:* allí las fuentes se cargan desde una carpeta del computador (`Fuentes_E1`); desde el Encuentro 2 se cargan **por la web** desde este repositorio (Parte A del tutorial del Encuentro 2).
- [Encuentro 2 · Tutorial del estudiante (PDF)](tutoriales/E2_Tutorial_Estudiante.pdf): el problema a resolver, conexión a las fuentes, Power Query, limpieza, transformación del PDD y relaciones (partes A a G).

## Diapositivas

- [Encuentro 1 (PDF)](diapositivas/E1_Diapositivas_PowerBI_Gestion_Publica.pdf)
- [Encuentro 2 (PDF)](diapositivas/E2_Diapositivas_PowerBI_Gestion_Publica.pdf)

## Cómo conectarse desde Power BI (ubicación web)

0. Antes de cargar la primera fuente (una vez por archivo): **Archivo → Opciones y configuración → Opciones → Archivo actual → Carga de datos** → en Relaciones desmarque **Detectar automáticamente nuevas relaciones después de cargar los datos** → Aceptar. (Evita esperas en "Detectando relaciones…"; las relaciones se crean a mano en la Parte F.)
1. Abra la carpeta [`fuentes`](fuentes) y haga clic en el nombre del archivo.
2. En la página del archivo, haga **clic derecho sobre el botón Raw → Copiar dirección del enlace**. (No haga clic normal: un .xlsx no es texto y el navegador lo descarga; es normal.)
3. En Power BI Desktop use el conector **del tipo de archivo** y pegue la dirección en **Ruta de acceso al archivo** (no pulse Examinar):
   - Archivos **.xlsx** (01, 02 y 05): **Inicio → Libro de Excel**.
   - Archivos **.csv** (03 y 04): **Inicio → Obtener datos → Texto o CSV**.
4. En **Credenciales de origen de datos** deje **Anónima** → **Siguiente**.
5. En **Elegir datos** marque la hoja (en los Excel) → **Load**.
6. En el panel **Datos**: clic derecho sobre la consulta nueva → **Cambiar nombre** → escriba el nombre de la tabla de abajo, igual (sin tildes ni espacios).

La dirección copiada tiene `/raw/` en la mitad: `https://github.com/hmotecnologico-create/PowerBI-Gestion-Publica-Cartagena/raw/refs/heads/main/fuentes/ARCHIVO`.

> **Si sale "Los datos descargados son HTML, que no es el tipo esperado"**: se copió la dirección de la página del archivo (la que tiene `/blob/`). Vuelva a la página del archivo y copie con **clic derecho en Raw → Copiar dirección del enlace**.

> **No use Obtener datos → Web**: en Power BI Desktop actual abre el conector "Página web", que sirve para páginas HTML y da el error "No se ha podido recuperar el contenido de la página web".

Respaldo (solo si no logra copiarla desde Raw): las mismas direcciones.

| N.° | Tabla | Archivo | Conector | Nombre de la consulta | Dirección (pegar en Ruta de acceso al archivo) |
|---|---|---|---|---|---|
| 01 | Matriz de seguimiento del PDD | [01_PDD_Matriz_Seguimiento_dic2025.xlsx](fuentes/01_PDD_Matriz_Seguimiento_dic2025.xlsx) | Libro de Excel · hoja “Seguridad Humana” | **PDD_SeguridadHumana** | https://github.com/hmotecnologico-create/PowerBI-Gestion-Publica-Cartagena/raw/refs/heads/main/fuentes/01_PDD_Matriz_Seguimiento_dic2025.xlsx |
| 02 | F11 – Programas y proyectos de inversión | [02_F11_Programas_Proyectos_dic2025.xlsx](fuentes/02_F11_Programas_Proyectos_dic2025.xlsx) | Libro de Excel · hoja “Hoja1” | **F11** | https://github.com/hmotecnologico-create/PowerBI-Gestion-Publica-Cartagena/raw/refs/heads/main/fuentes/02_F11_Programas_Proyectos_dic2025.xlsx |
| 03 | Ejecución presupuestal de gastos | [03_Ejecucion_Presupuestal_Gastos_ny6j-ysx3.csv](fuentes/03_Ejecucion_Presupuestal_Gastos_ny6j-ysx3.csv) | Texto o CSV | **Ejecucion** | https://github.com/hmotecnologico-create/PowerBI-Gestion-Publica-Cartagena/raw/refs/heads/main/fuentes/03_Ejecucion_Presupuestal_Gastos_ny6j-ysx3.csv |
| 04 | SECOP II – BPIN por proceso | [04_SECOPII_BPIN_por_Proceso_Cartagena_2024-2025_d9na-abhe.csv](fuentes/04_SECOPII_BPIN_por_Proceso_Cartagena_2024-2025_d9na-abhe.csv) | Texto o CSV | **BPIN_Proceso** | https://github.com/hmotecnologico-create/PowerBI-Gestion-Publica-Cartagena/raw/refs/heads/main/fuentes/04_SECOPII_BPIN_por_Proceso_Cartagena_2024-2025_d9na-abhe.csv |
| 05 | SECOP II – Contratos electrónicos 2025 | [05_SECOPII_Contratos_Alcaldia_2025_jbjy-vk9h.xlsx](fuentes/05_SECOPII_Contratos_Alcaldia_2025_jbjy-vk9h.xlsx) | Libro de Excel · hoja “Contratos” | **Contratos** | https://github.com/hmotecnologico-create/PowerBI-Gestion-Publica-Cartagena/raw/refs/heads/main/fuentes/05_SECOPII_Contratos_Alcaldia_2025_jbjy-vk9h.xlsx |

## De dónde salen las tablas (fuente oficial)

> **Nota de preparación (13-10-2026):** en `03_Ejecucion_Presupuestal_Gastos_ny6j-ysx3.csv` se reemplazaron por un espacio 6 saltos de línea que venían dentro de la columna `descripci_n_rubro` (texto de la descripción de rubros). Ningún valor cambió; así Power BI lee las 2.564 filas sin errores.

| N.° | Publica | Página oficial | Corte | Descargado |
|---|---|---|---|---|
| 01 | Secretaría de Planeación Distrital | [cartagena.gov.co – Seguimiento planes de acción a 31-dic-2025](https://www.cartagena.gov.co/transparencia/4planeacion-presupuesto-informes/43-plan-accion/seguimiento-planes-acciones-institucionales-corte-31-diciembre-2025) | 31-dic-2025 | 05-10-2026 |
| 02 | Alcaldía de Cartagena (Banco de Programas y Proyectos) | [cartagena.gov.co – F11 diciembre 2025](https://www.cartagena.gov.co/transparencia/4planeacion-presupuesto-informes/informacion-ejecucion-presupuestal-contractual-contable-financiera-programas-proyectos-diciembre-2025) | dic-2025 | 05-10-2026 |
| 03 | Alcaldía de Cartagena, en datos.gov.co | [ny6j-ysx3](https://www.datos.gov.co/Hacienda-y-Cr-dito-P-blico/Ejecuci-n-Presupuestal-de-gastos-Distrito-de-Carta/ny6j-ysx3) | 2025 (dic) y 2026 (ago) | 06-10-2026 |
| 04 | Colombia Compra Eficiente, en datos.gov.co | [d9na-abhe](https://www.datos.gov.co/d/d9na-abhe) (filtro: BPIN de Cartagena, vigencias 2024 y 2025) | Diario | 06-10-2026 |
| 05 | Colombia Compra Eficiente, en datos.gov.co | [jbjy-vk9h](https://www.datos.gov.co/d/jbjy-vk9h) (filtro: Alcaldía NIT 890480184, firmados en 2025; pasado a Excel) | Diario | 06-10-2026 |

El detalle de cada fuente (cómo se descargó, qué representa una fila, qué hoja cargar y número de filas) está en [`fuentes/00_Ficha_Procedencia.xlsx`](fuentes/00_Ficha_Procedencia.xlsx).

**Las tablas se publican tal como se descargaron**, sin limpiar: la limpieza y el modelo se hacen en clase con Power Query. Los contratos no incluyen nombres, documentos ni cuentas bancarias de personas (minimización de datos).
