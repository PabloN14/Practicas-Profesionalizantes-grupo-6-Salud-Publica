# Practicas-Profesionalizantes-grupo-6-Salud-Publica 
Este repositorio se utilizará con el objetivo de organizar y documentar los archivos relevantes desarrollados por el equipo.

Nombre del Proyecto: Infecciones respiratorias agudas en Argentina: prepandemia vs. pospandemia


## Integrantes del equipo

**Equipo 6**

- Maria Silvana Sosa
- Pablo Nuñez
- Estela Gomez
- Pablo Velázquez

---

## Descripción del proyecto

Las infecciones respiratorias agudas (IRA) son una de las principales causas de consulta e internación en Argentina, sobre todo en los meses fríos. La pandemia de COVID-19 (2020-2022) alteró la circulación de los virus respiratorios, la forma de consultar y los sistemas de vigilancia.

Este proyecto analiza los casos de IRA notificados al Sistema Nacional de Vigilancia de la Salud para **describir cómo cambiaron entre la etapa prepandemia (2019) y la pospandemia (2025-2026)**: qué eventos aumentaron o disminuyeron, en qué semanas del año se concentran y qué provincias tienen mayor incidencia en relación con su población.

El análisis es **descriptivo**: muestra cambios, pero no los atribuye exclusivamente a la pandemia.

---

## Fuente de datos

| Dataset | Fuente | Registros | Período |
|---|---|---|---|
| Vigilancia de IRA 2018-2019 | Ministerio de Salud – SNVS ([datos.salud.gob.ar](https://datos.salud.gob.ar/dataset/vigilancia-de-infecciones-respiratorias-agudas)) | 790.773 | 2018 SE 18 – 2019 SE 52 |
| Vigilancia de IRA 2025-2026 | Ministerio de Salud – SNVS 2.0 ([datos.salud.gob.ar](https://datos.salud.gob.ar/dataset/vigilancia-de-infecciones-respiratorias-agudas)) | 422.868 | 2025 SE 1 – 2026 SE 36 |
| Población por jurisdicción | INDEC – Censo 2022 | 25 | 2022 |

- **Tipo de datos:** salud pública – vigilancia epidemiológica.
- **Contenido:** casos notificados de enfermedad tipo influenza (ETI), neumonía y bronquiolitis en menores de 2 años, por departamento, provincia, año, semana epidemiológica y grupo de edad. Son datos agregados y anonimizados.
- El detalle de cada variable está en el diccionario de datos (`docs/`).

---

## Objetivos del análisis

**Objetivo general:** describir los cambios en las infecciones respiratorias agudas en Argentina entre 2019 y 2025-2026.

**Preguntas de análisis:**

1. **(Principal)** ¿Qué eventos (ETI, neumonía y bronquiolitis) aumentaron y cuáles disminuyeron entre 2019 y 2025?
2. ¿Cambió la estacionalidad? ¿El pico de casos ocurre en las mismas semanas en 2019, 2025 y 2026?
3. ¿Qué provincias presentan mayor incidencia relativa de casos respiratorios en relación a su población, y cómo cambió entre 2019 y 2025?

---

## Herramientas utilizadas

- Python
- Excel / CSV
- Google Drive · Trello · GitHub · Google Meet

---

## Proceso de análisis

**Sprint 1 – Comprensión del problema y de los datos**

- Ficha de conocimiento del dominio
- Diccionario de datos de los 3 datasets
- Unificación de datasets: nombres de columnas, categorías de evento agrupadas (ETI, Neumonía, Bronquiolitis) y cruce por código de provincia INDEC
- Limpieza: suma de filas con la misma clave en 2018-2019, exclusión de filas de 2020 y con 0 casos, comparación en las mismas semanas epidemiológicas
- Análisis exploratorio (EDA) con 4 visualizaciones
- Formulación de 10 preguntas y selección de 3


## Resultados principales (Sprint 1 – EDA inicial)

- **Más casos, pero no de todo:** entre 2019 y 2025 los casos aumentaron un 24,2%. La ETI creció un 45,5%, la neumonía se mantuvo estable (+5,6%) y la bronquiolitis bajó un 36,7%.
- **La temporada llega antes:** el pico pasó de la semana 26 (2019) a la 24 (2025) y a la 21 (2026), con picos semanales un 42% más altos.
- **Cambia la edad de los casos:** los menores de 2 años pasaron del 31,3% al 18,7% de los casos; crecieron los grupos de 5 a 14 y de 45 a 64 años.
- **El mapa cambia al ajustar por población:** Buenos Aires tiene más casos, pero Catamarca, La Rioja y Jujuy tienen la mayor incidencia.
- **Calidad de datos:** caídas como las de Santa Fe (−90%) y CABA (−66%) sugieren cambios en la notificación.



## Conclusiones

*Sprint 1:* los datos muestran que las infecciones respiratorias cambiaron después de la pandemia en cantidad, composición, calendario y edades afectadas. Estos resultados son preliminares y se profundizarán en los próximos Sprints.

- **Limitaciones:** casos notificados ≠ casos reales; cambios en los sistemas de notificación; sin datos de 2020-2022; población del Censo 2022 para todos los años.
- **Líneas futuras:** relación entre la baja de bronquiolitis y la vacuna contra el VSR en gestantes (desde 2024); incorporar los años de pandemia; validar los casos de Santa Fe y CABA.



