# Matriz de correspondencia con OWASP MASVS

La presente matriz relaciona las vulnerabilidades identificadas durante el análisis de las aplicaciones Android con las categorías de verificación definidas por **OWASP Mobile Application Security Verification Standard (MASVS)**. Esta correspondencia permitió fundamentar técnicamente las medidas de mitigación propuestas y asegurar que las recomendaciones se encuentran alineadas con buenas prácticas internacionales para el desarrollo seguro de aplicaciones móviles.

| Categoría           | Vulnerabilidad identificada                     | Dominio OWASP MASVS | Justificación                                                                                                                                      |
| ------------------- | ----------------------------------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| Gestión de permisos | Uso de permisos sensibles                       | MASVS-PLATFORM      | La aplicación debe solicitar únicamente los permisos estrictamente necesarios para su funcionamiento, siguiendo el principio de mínimo privilegio. |
| AndroidManifest.xml | Componentes exportados                          | MASVS-PLATFORM      | Los componentes deben configurarse adecuadamente para evitar accesos no autorizados desde otras aplicaciones.                                      |
| AndroidManifest.xml | `allowBackup` habilitado                        | MASVS-STORAGE       | La información almacenada por la aplicación debe protegerse frente a procesos de extracción o restauración no autorizados.                         |
| AndroidManifest.xml | Tráfico en texto plano habilitado               | MASVS-NETWORK       | Todas las comunicaciones sensibles deben realizarse mediante canales cifrados utilizando protocolos seguros como HTTPS/TLS.                        |
| Código fuente       | Uso de SHA-1 y MD5                              | MASVS-CRYPTO        | Los algoritmos criptográficos deben cumplir estándares vigentes que garanticen la confidencialidad e integridad de la información.                 |
| Código fuente       | AES/CBC con PKCS5/PKCS7                         | MASVS-CRYPTO        | La implementación criptográfica debe utilizar configuraciones resistentes frente a ataques conocidos.                                              |
| Código fuente       | SharedPreferences con información sensible      | MASVS-STORAGE       | Los datos almacenados localmente deben protegerse mediante mecanismos de cifrado y almacenamiento seguro.                                          |
| Código fuente       | Consultas SQL con potencial de riesgo           | MASVS-CODE          | El código debe implementar mecanismos de validación que reduzcan riesgos asociados al procesamiento de datos.                                      |
| Certificados        | Uso exclusivo del esquema de firma V1           | MASVS-RESILIENCE    | La aplicación debe utilizar mecanismos modernos de firma que garanticen la autenticidad e integridad del APK.                                      |
| Protección del APK  | Protección limitada frente a ingeniería inversa | MASVS-RESILIENCE    | La aplicación debe incorporar mecanismos de ofuscación y protección contra técnicas de ingeniería inversa y manipulación.                          |

---

## Conclusiones

- Las vulnerabilidades identificadas presentan correspondencia con múltiples dominios de verificación definidos por OWASP MASVS.
- Los dominios **MASVS-PLATFORM**, **MASVS-STORAGE**, **MASVS-NETWORK**, **MASVS-CRYPTO**, **MASVS-CODE** y **MASVS-RESILIENCE** respaldan técnicamente las medidas de mitigación propuestas.
- La utilización de OWASP MASVS complementa la interpretación realizada mediante la ISO/IEC 27032, proporcionando controles específicos para fortalecer la seguridad de aplicaciones Android.
