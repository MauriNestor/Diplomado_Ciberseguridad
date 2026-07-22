# Matriz de análisis basada en los lineamientos de la ISO/IEC 27032

La presente matriz establece la correspondencia entre las vulnerabilidades identificadas durante el análisis de las aplicaciones Android y los principios de ciberseguridad definidos en la norma **ISO/IEC 27032**. Su propósito es demostrar cómo los hallazgos obtenidos mediante MobSF fueron interpretados dentro del marco de la ciberseguridad y utilizados como base para la propuesta de mitigación.

| Categoría           | Vulnerabilidad identificada                     | Principio ISO/IEC 27032 relacionado  | Justificación                                                                                                      |
| ------------------- | ----------------------------------------------- | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| Gestión de permisos | Uso de permisos sensibles                       | Protección de la información         | El acceso a recursos sensibles debe limitarse al mínimo necesario para reducir el riesgo de acceso no autorizado.  |
| AndroidManifest.xml | Componentes exportados                          | Reducción de la superficie de ataque | La exposición innecesaria de componentes incrementa las posibilidades de explotación por aplicaciones maliciosas.  |
| AndroidManifest.xml | `allowBackup` habilitado                        | Protección de activos de información | Permitir respaldos sin restricciones puede facilitar la extracción de información sensible del dispositivo.        |
| AndroidManifest.xml | Tráfico HTTP habilitado                         | Seguridad de las comunicaciones      | La transmisión de información sin cifrado compromete la confidencialidad e integridad de los datos.                |
| Código fuente       | Uso de SHA-1 y MD5                              | Protección de la información         | Los algoritmos criptográficos obsoletos reducen la resistencia frente a ataques criptográficos conocidos.          |
| Código fuente       | AES/CBC con PKCS5/PKCS7                         | Gestión del riesgo                   | El uso de modos de cifrado susceptibles a ataques requiere mecanismos criptográficos más robustos.                 |
| Código fuente       | SharedPreferences inseguro                      | Protección de activos de información | El almacenamiento local de información sensible debe implementar mecanismos adecuados de protección.               |
| Certificados        | Uso exclusivo del esquema de firma V1           | Autenticidad del software            | Los mecanismos de firma deben garantizar la autenticidad e integridad de la aplicación distribuida.                |
| Protección del APK  | Protección limitada frente a ingeniería inversa | Protección del software              | La implementación de mecanismos de protección incrementa la resiliencia frente al análisis y modificación del APK. |

---

## Conclusiones

- Las vulnerabilidades identificadas afectan distintos principios de ciberseguridad contemplados en la ISO/IEC 27032.
- La mayor parte de los hallazgos se relacionan con la protección de la información, la reducción de la superficie de ataque y la seguridad de las comunicaciones.
- La interpretación basada en la ISO/IEC 27032 permitió fundamentar técnicamente las medidas de mitigación propuestas en la investigación.
