# Matriz de vulnerabilidades identificadas

Esta matriz resume las principales vulnerabilidades identificadas durante el análisis estático de las aplicaciones Android mediante **Mobile Security Framework (MobSF)**. Los hallazgos fueron posteriormente interpretados conforme a los principios de la **ISO/IEC 27032** y utilizados como base para la propuesta de mitigación presentada en esta investigación.

| ID  | Aplicación        | Categoría           | Vulnerabilidad identificada                                                           | Severidad | Módulo MobSF         |
| :-: | ----------------- | ------------------- | ------------------------------------------------------------------------------------- | :-------: | -------------------- |
|  1  | IPTV Smarters Pro | Gestión de permisos | Uso de permisos sensibles para almacenamiento, micrófono y superposición de pantalla. |   High    | Permissions          |
|  2  | IPTV Smarters Pro | AndroidManifest.xml | Tráfico en texto plano habilitado (`usesCleartextTraffic=true`).                      |   High    | Manifest Analysis    |
|  3  | IPTV Smarters Pro | AndroidManifest.xml | Componentes exportados accesibles desde otras aplicaciones.                           |  Warning  | Manifest Analysis    |
|  4  | IPTV Smarters Pro | Código fuente       | Uso de cifrado AES/CBC con PKCS5/PKCS7 susceptible a ataques conocidos.               |   High    | Code Analysis        |
|  5  | IPTV Smarters Pro | Código fuente       | SharedPreferences con permisos inseguros de lectura/escritura.                        |   High    | Code Analysis        |
|  6  | Facebook          | Gestión de permisos | Uso de permisos sensibles relacionados con ubicación, cámara, contactos y telefonía.  |   High    | Permissions          |
|  7  | Facebook          | AndroidManifest.xml | Gran cantidad de componentes exportados.                                              |  Warning  | Manifest Analysis    |
|  8  | Facebook          | AndroidManifest.xml | `allowBackup` habilitado.                                                             |  Warning  | Manifest Analysis    |
|  9  | Facebook          | Código fuente       | Uso de algoritmos criptográficos SHA-1 y MD5.                                         |  Warning  | Code Analysis        |
| 10  | Facebook          | Certificados        | Uso del esquema de firma V1 susceptible a la vulnerabilidad Janus.                    |  Warning  | Certificate Analysis |
| 11  | Facebook          | Protección del APK  | Mecanismos de protección del APK limitados frente a ingeniería inversa.               |   Info    | APKiD                |

---

## Resumen

- Aplicaciones analizadas: **2**
- Herramienta utilizada: **Mobile Security Framework (MobSF)**
- Categorías evaluadas:
  - Gestión de permisos
  - AndroidManifest.xml
  - Código fuente
  - Certificados
  - Protección del APK (APKiD)

Los resultados de esta matriz constituyen la base para la elaboración de la propuesta de mitigación y su posterior validación documental.
