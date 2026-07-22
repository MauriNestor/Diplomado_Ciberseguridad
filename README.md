# Evaluación de la seguridad de aplicaciones Android distribuidas fuera de Google Play mediante MobSF conforme a la ISO/IEC 27032

## Descripción

Este repositorio contiene el material de apoyo correspondiente a la monografía titulada:

> **Evaluación de la seguridad de aplicaciones Android distribuidas fuera de Google Play en el marco de la ciberseguridad según la ISO/IEC 27032.**

La investigación tiene como objetivo evaluar la seguridad de aplicaciones Android distribuidas fuera de Google Play mediante la herramienta **Mobile Security Framework (MobSF)**, interpretar los hallazgos utilizando la **ISO/IEC 27032** y las buenas prácticas de **OWASP MASVS**, y proponer lineamientos de mitigación para reducir los riesgos identificados.

---

# Objetivos de la investigación

- Evaluar la seguridad de aplicaciones Android distribuidas fuera de Google Play utilizando MobSF.
- Identificar vulnerabilidades presentes en las aplicaciones analizadas.
- Interpretar los resultados conforme a la ISO/IEC 27032.
- Proponer medidas de mitigación alineadas con OWASP MASVS.

---

# Aplicaciones analizadas

Durante la investigación se analizaron las siguientes aplicaciones:

| Aplicación        | Estado    |
| ----------------- | --------- |
| IPTV Smarters Pro | Analizada |
| Facebook APK      | Analizada |

**Nota:** Los archivos APK no se incluyen en este repositorio por tratarse de software propietario distribuido por terceros.

---

# Tecnologías y herramientas utilizadas

- Mobile Security Framework (MobSF)
- Docker
- Python 3
- Java
- Android SDK
- OWASP MASVS
- ISO/IEC 27032

---

# Estructura del repositorio

```text
01-apks/
02-mobsf-reports/
03-analysis/
04-images/
05-monograph/
```

---

# Requisitos

Antes de ejecutar MobSF se requiere:

- Docker Desktop instalado
- Git
- Navegador web moderno

---

# Instalación de MobSF

## 1. Clonar MobSF

```bash
git clone https://github.com/MobSF/Mobile-Security-Framework-MobSF.git
```

## 2. Ingresar al proyecto

```bash
cd Mobile-Security-Framework-MobSF
```

## 3. Ejecutar MobSF mediante Docker

```bash
docker pull opensecurity/mobile-security-framework-mobsf

docker run -it --rm \
-p 8000:8000 \
opensecurity/mobile-security-framework-mobsf
```

## 4. Abrir MobSF

```
http://localhost:8000
```

---

# Procedimiento utilizado durante la investigación

El proceso seguido fue el siguiente:

1. Selección de aplicaciones Android.
2. Obtención de los archivos APK.
3. Análisis estático mediante MobSF.
4. Identificación de vulnerabilidades.
5. Clasificación de resultados.
6. Interpretación conforme a ISO/IEC 27032.
7. Relación con OWASP MASVS.
8. Elaboración de lineamientos de mitigación.
9. Validación documental de la propuesta.

---

# Contenido del repositorio

## 01-apks

Información de las aplicaciones evaluadas.

## 02-mobsf-reports

Reportes PDF generados por MobSF.

## 03-analysis

Matrices utilizadas durante la investigación:

- Vulnerabilidades
- ISO/IEC 27032
- OWASP MASVS
- Medidas de mitigación

## 04-images

Capturas utilizadas en la monografía.

## 05-monograph

Versión final del documento.

---

# Resultados principales

Los análisis realizados permitieron identificar vulnerabilidades relacionadas con:

- Gestión de permisos.
- Configuración del AndroidManifest.xml.
- Calidad del código fuente.
- Protección del APK.
- Certificados y comunicaciones.

Estos resultados sirvieron como base para la elaboración de una propuesta de mitigación alineada con la ISO/IEC 27032 y OWASP MASVS.

---

# Autor

Mauricio Apaza Callapa

Universidad Mayor de San Simón

Facultad de Ciencias y Tecnología

Cochabamba – Bolivia

2026
