# Geografía de la Informalidad Laboral en el Perú (2020–2024) y Caso de Estudio: Gamarra

Este proyecto realiza un análisis espacial y temporal de la evolución de la informalidad laboral en el Perú a nivel regional durante el periodo de pandemia y recuperación económica (2020–2024). Asimismo, incluye un caso de estudio focalizado en el emporio comercial de **Gamarra**, donde se contrasta la distribución de locales comerciales registrados frente a las zonas de calor de comercio informal ambulatorio.

> [!IMPORTANTE]
> **Mapas Interactivos Web en Tiempo Real (GitHub Pages):**
> * 🗺️ [Mapa de Calor Temporal Regional (2020-2024)](https://melany-vega.github.io/Tasa-de-empleo-informal-/informalidad_heatmap_temporal.html)
> * 📊 [Mapa de Intensidad por Círculos (2020-2024)](https://melany-vega.github.io/Tasa-de-empleo-informal-/informalidad_intensidad_temporal.html)
> * 🏢 [Gamarra: Infraestructura Comercial y Locales Registrados](<https://melany-vega.github.io/Tasa-de-empleo-informal-/Gamarra_Infraestructura Comercial y Locales Registrados.html>)
> * 🛍️ [Gamarra: Concentración de Comercio Informal Ambulatorio](<https://melany-vega.github.io/Tasa-de-empleo-informal-/Gamarra_Concentración de Comercio Informal en Vía Pública.html>)

---

## 🎯 Objetivos del Proyecto

1. **Evolución Regional:** Analizar y representar geográficamente cómo fluctuó la tasa de empleo informal en las tres regiones naturales (Costa, Sierra y Selva) tras el choque de la COVID-19.
2. **Análisis Micro-Espacial (Gamarra):** Evaluar de manera espacial la relación de coexistencia y tensión entre la infraestructura comercial formal (locales registrados) y el despliegue del comercio informal en la vía pública (comercio ambulatorio).

---

## 📊 Hallazgos y Conclusiones del Estudio

### 1. ¿Por qué analizar la informalidad con mapas interactivos?
Una tabla tradicional dificulta identificar patrones de comportamiento. La visualización espacial temporal permite:
* **Identificar clusters de manera inmediata:** Es evidente a simple vista cómo el "calor" de la informalidad se concentra con mayor fuerza en el bloque sur y oriente del país.
* **Evaluar dinámicas de cambio:** Permite observar de forma interactiva qué regiones lograron mitigar la informalidad tras la pandemia y cuáles quedaron estancadas.

### 2. Conclusiones del Análisis Regional (2020–2024)
* **La Brecha Costa-Sierra/Selva:** El mapa revela una marcada división. Mientras que la **Costa** registra las tasas más bajas (Lima Metrop./Callao ~56%, Moquegua ~60%, Arequipa ~58% e Ica ~62%), la **Sierra y Selva alta** muestran una realidad crítica, con departamentos como **Huancavelica (93.2%)**, **Cajamarca (88.6%)** y **Apurímac (88.2%)** superando consistentemente el 80% y 90% de empleo informal.
* **El efecto distorsionador de la Pandemia (2020):** Los mapas muestran una "reducción" artificial de la informalidad en el 2020 en algunas zonas. Esto no se debió a una formalización del empleo, sino a que los trabajadores informales perdieron sus puestos de trabajo y salieron temporalmente de la Población Económicamente Activa (PEA).
* **Implicancia de Política Pública:** Los datos demuestran que una política nacional única de formalización es ineficaz. Se requieren estrategias diferenciadas: incentivos tributarios en la Costa, y desarrollo de infraestructura productiva y conectividad en la Sierra y Selva.

### 3. Conclusiones del Caso de Estudio: Emporio Comercial de Gamarra
* **Atracción por el flujo de clientes:** La superposición de los mapas demuestra que el comercio informal ambulatorio no se distribuye al azar. Se concentra de manera masiva en las vías públicas colindantes a las zonas con mayor densidad de galerías y locales registrados (Avenidas Aviación, Huánuco, y los accesos a los Dameros A y B). El comercio informal "sigue" al flujo de clientes que genera la infraestructura formal.
* **Presión sobre el espacio público:** El mapa de calor del comercio informal ambulatorio muestra cuellos de botella críticos en las zonas de acceso. Esto no solo refleja un problema laboral, sino un desafío de **planificación urbana y seguridad** (rutas de evacuación bloqueadas y congestión vehicular).

---

## 📈 Metodología y Fuentes de Datos

* **Datos Regionales:** INEI - Encuesta Nacional de Hogares (ENAHO) y Cuenta Satélite de la Economía Informal.
* **Procesamiento:** Consolidación de tablas de empleo informal en formato *Tidy Data* utilizando Pandas.
* **Georreferenciación:** Cálculo de centroides oficiales por departamento mediante la proyección UTM 18S de los límites departamentales oficiales GeoJSON: ("https://raw.githubusercontent.com/juaneladio/"
               "peru-geojson/master/peru_departamental_simple.geojson")
* **Datos de Gamarra:** Geolocalización de galerías comerciales formalmente registradas vs. censos locales y reportes de comercio ambulatorio en la vía pública por OpenStreetMap: https://umap.openstreetmap.fr/en/map/mapa-digital-de-la-municipalidad-de-la-victoria_951373#15/-12.070063/-77.021241

---

## 🛠️ Tecnologías Utilizadas

| Categoría | Herramientas / Librerías |
|---|---|
| **Lenguaje** | Python 3 |
| **Procesamiento de Datos** | `pandas`, `numpy`, `openpyxl` |
| **Georreferenciación** | `geopandas` |
| **Visualización Mapa** | `folium` (Plugins: `HeatMapWithTime`, `TimestampedGeoJson`, `Fullscreen`, `MiniMap`, `DivIcon`) |


