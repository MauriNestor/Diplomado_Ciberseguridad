# Análisis de resultados

Esta carpeta reúne las matrices elaboradas durante el proceso de análisis e interpretación de los resultados obtenidos mediante **Mobile Security Framework (MobSF)**. Su finalidad es documentar de forma estructurada el proceso seguido para identificar las vulnerabilidades presentes en las aplicaciones Android analizadas, interpretarlas conforme a la **ISO/IEC 27032**, relacionarlas con los controles técnicos definidos por **OWASP MASVS** y establecer las medidas de mitigación propuestas.

Las matrices constituyen la evidencia metodológica que respalda los resultados presentados en la monografía y permiten comprender la transición desde el diagnóstico inicial hasta la propuesta de mitigación.

---

## Flujo de análisis

```text
Evaluación de seguridad (MobSF)
                │
                ▼
01. Matriz de vulnerabilidades
                │
                ▼
02. Análisis conforme a ISO/IEC 27032
                │
                ▼
03. Correspondencia con OWASP MASVS
                │
                ▼
04. Matriz de medidas de mitigación
```

---

## Contenido

### 01_matriz_vulnerabilidades.md

Resume las vulnerabilidades identificadas durante el análisis de las aplicaciones Android mediante MobSF, indicando la categoría afectada, el nivel de severidad y el módulo del reporte donde fueron detectadas.

---

### 02_matriz_analisis_iso_27032.md

Relaciona cada vulnerabilidad con los principios de ciberseguridad establecidos en la **ISO/IEC 27032**, proporcionando una interpretación de los hallazgos desde una perspectiva de gestión de riesgos y protección de la información.

---

### 03_matriz_owasp_masvs.md

Establece la correspondencia entre las vulnerabilidades identificadas y los dominios de verificación definidos por **OWASP MASVS**, justificando técnicamente las recomendaciones propuestas para fortalecer la seguridad de aplicaciones Android.

---

### 04_matriz_mitigacion.md

Presenta las medidas de mitigación propuestas para cada vulnerabilidad identificada, indicando el beneficio esperado de su implementación. Esta matriz constituye la síntesis de la propuesta desarrollada en la investigación.

---

## Relación con la investigación

Las matrices documentadas en esta carpeta respaldan los resultados presentados en los Capítulos III, IV y V de la monografía:

- **Capítulo III:** Diagnóstico de seguridad de las aplicaciones Android.
- **Capítulo IV:** Propuesta de mitigación basada en la ISO/IEC 27032 y OWASP MASVS.
- **Capítulo V:** Validación documental de la propuesta.

En conjunto, estas matrices evidencian el proceso metodológico seguido para transformar los resultados obtenidos mediante MobSF en una propuesta de mitigación técnicamente fundamentada y alineada con estándares internacionales de ciberseguridad.
