# Taller 2. Actividad autónoma: gobierno, activos, riesgos y cumplimiento ISO/IEC 27001 con CISO Assistant

**Curso:** Gobernanza en Seguridad de la Información  
**Tipo:** Actividad autónoma  
**Caso:** Café Andino S.A.S.  

| Modalidad | Dedicación estimada | Puntaje | Herramienta | Productos |
|---|---|---|---|---|
| Individual y autónoma | 10 a 12 horas | 100 puntos | CISO Assistant Community Edition (código abierto, AGPLv3) sobre Kali Linux | Un documento PDF único con norma IEEE, repositorio en GitHub y video en YouTube |

## Contenido

- [Presentación](#presentación)
- [Competencias que se evalúan](#competencias-que-se-evalúan)
- [Situación](#situación)
- [Reglas de la actividad](#reglas-de-la-actividad)
- [Fase 1. Configuración inicial de la organización](#fase-1-configuración-inicial-de-la-organización)
- [Fase 2. Gobernanza](#fase-2-gobernanza)
- [Fase 3. Gestión de activos](#fase-3-gestión-de-activos)
- [Fase 4. Gestión de riesgos](#fase-4-gestión-de-riesgos)
- [Fase 5. Marco de trabajo ISO/IEC 27001:2022](#fase-5-marco-de-trabajo-isoiec-270012022)
- [Fase 6. Integración y presentación a la dirección](#fase-6-integración-y-presentación-a-la-dirección)
- [Productos y condiciones de entrega](#productos-y-condiciones-de-entrega)
- [Norma IEEE](#norma-ieee)
- [Criterios de evaluación](#criterios-de-evaluación-100-puntos)
- [Recursos](#recursos)

## Presentación

Esta es una actividad autónoma de aplicación. No incluye instrucciones paso a paso: plantea una situación profesional y un conjunto de resultados que el estudiante debe lograr por su cuenta con CISO Assistant, una plataforma de gobierno, riesgo y cumplimiento (GRC) de código abierto.

Para cada fase se indican el propósito, los resultados mínimos esperados y el módulo de la herramienta donde se trabaja. La forma de llegar a esos resultados, las decisiones de diseño y su justificación son responsabilidad del estudiante. Para resolver dudas de uso, el estudiante debe consultar la [documentación oficial de CISO Assistant](https://intuitem.gitbook.io/ciso-assistant) y las normas de referencia.

**Prerrequisito:** haber completado el **Taller 1. Instalación de CISO Assistant en Kali Linux**, con la herramienta funcionando y el usuario administrador creado. Para iniciar la herramienta en cada sesión de trabajo:

```bash
cd ~/ciso-assistant-community
docker compose up -d
docker compose ps
```

y luego ingresar desde Firefox a `https://localhost:8443/`. Si se presentan problemas con la herramienta, el estudiante debe consultar la sección de solución de problemas del Taller 1.

## Competencias que se evalúan

1. Modelar una organización en una plataforma GRC con una estructura de dominios, perímetros y responsables coherente.
2. Diseñar elementos de gobernanza alineados con ISO/IEC 27001:2022: cuestiones del contexto, objetivos de seguridad, políticas y responsabilidades.
3. Construir un inventario de activos con dependencias, propiedades de seguridad y objetivos de recuperación.
4. Valorar y tratar riesgos con un método consistente y criterios de aceptación definidos por la dirección.
5. Evaluar el cumplimiento de ISO/IEC 27001:2022 y elaborar una Declaración de Aplicabilidad coherente con los riesgos.
6. Documentar el uso de la herramienta y comunicar los resultados a la alta dirección, sustentando las decisiones con fuentes y aplicando la norma IEEE.

## Situación

La junta directiva de **Café Andino S.A.S.** decidió implementar un sistema de gestión de seguridad de la información (SGSI) basado en ISO/IEC 27001:2022, con la meta de obtener la certificación en 18 meses. Como primer paso, encargó al estudiante, en su rol de responsable de seguridad de la información (CISO), montar el SGSI en una plataforma GRC y presentar en un mes un diagnóstico que permita tomar decisiones.

La información de la organización está en el archivo [`datos/CASO_CAFE_ANDINO.md`](datos/CASO_CAFE_ANDINO.md). El estudiante puede complementar el caso con supuestos razonables, siempre que los declare de forma explícita en el documento.

> Caso ficticio con fines académicos. Las personas y empresas mencionadas no existen.

## Reglas de la actividad

1. **Trabajo individual y propio.** Cada estudiante trabaja en su propia instancia de CISO Assistant.
2. **Identificación de autoría.** Para que el trabajo sea verificable:
   - El dominio principal debe llamarse `Café Andino S.A.S. - Apellido Nombre`.
   - El usuario administrador debe tener el correo institucional, el nombre y el apellido del estudiante, de modo que aparezcan en el menú lateral de la herramienta. Estos datos se registran en *Organización > Usuarios*, editando el usuario administrador.
   - Todas las capturas deben mostrar el nombre del estudiante o del dominio, y la fecha y hora del sistema.
   - El documento debe registrar la versión de CISO Assistant (menú de usuario, opción *Acerca de CISO Assistant*).
3. **Decisiones justificadas.** Toda decisión (un nivel de riesgo, una exclusión, un responsable) debe tener una justificación basada en el caso, en una norma o en un criterio definido por el estudiante. Una decisión sin justificación se considera incompleta.
4. **Coherencia entre fases.** Los resultados de cada fase deben usarse en las siguientes: las cuestiones y los objetivos alimentan los riesgos, los activos se vinculan a los escenarios y los controles se reutilizan en la auditoría de ISO/IEC 27001. La coherencia entre fases es un criterio de evaluación.
5. **Uso de inteligencia artificial generativa.** No está permitido para producir el análisis, las decisiones ni los textos del documento. Si se usa para consultar el funcionamiento de la herramienta, debe declararse en el documento.

## Fase 1. Configuración inicial de la organización

**Propósito:** estructurar la organización en la herramienta de manera que refleje el alcance del SGSI y permita asignar responsabilidades.

**Módulos de la herramienta:** *Organización* (Dominios, Perímetros, Usuarios, Equipos) y el menú de usuario (idioma, perfil).

**Resultados mínimos esperados:**

| N.º | Resultado |
|---|---|
| 1.1 | Interfaz configurada en español y perfil del administrador con los datos del estudiante. |
| 1.2 | Dominio principal de la organización, con una descripción que resuma el negocio. |
| 1.3 | Al menos **dos perímetros**, definidos por el estudiante a partir del caso, uno de los cuales corresponde al alcance del SGSI. Cada perímetro debe tener una descripción de lo que incluye y lo que excluye. |
| 1.4 | Al menos **tres usuarios** adicionales que representen roles del caso (por ejemplo, gerente general, jefe de TI, dueño de la información de clientes), con un rol en la herramienta acorde con su responsabilidad. |
| 1.5 | Declaración de alcance del SGSI (80 a 150 palabras) en el documento, coherente con los perímetros creados. |

**Preguntas que el documento debe responder:**

- ¿Por qué se eligieron esos perímetros y no otros?
- ¿Qué rol de la herramienta se asignó a cada usuario y por qué ese rol respeta la separación de funciones?

## Fase 2. Gobernanza

**Propósito:** registrar los elementos de gobierno que exige ISO/IEC 27001:2022 y que dan dirección al SGSI.

**Módulos de la herramienta:** *Gobernanza* (Problemas (ISO), Objetivos (ISO), Políticas) y, de forma opcional, *Gestión de proyectos* (Matrices de responsabilidades).

**Resultados mínimos esperados:**

| N.º | Resultado | Referencia ISO/IEC 27001:2022 |
|---|---|---|
| 2.1 | Al menos **seis cuestiones** del contexto (tres internas y tres externas), clasificadas por categoría. Debe incluirse un pronunciamiento sobre si el cambio climático es una cuestión pertinente. | Cláusula 4.1 y enmienda 1 de 2024 |
| 2.2 | Al menos **tres objetivos de seguridad de la información** medibles, con responsable y fecha, vinculados a cuestiones del contexto. | Cláusula 6.2 |
| 2.3 | Al menos **cuatro políticas** registradas en la herramienta, con propósito, responsable y estado. Una debe ser la política general de seguridad de la información. | Cláusula 5.2 y control A.5.1 |
| 2.4 | Una tabla de **partes interesadas** con sus requisitos (en el documento). | Cláusula 4.2 |
| 2.5 | Una **matriz de responsabilidades (RACI)** para al menos ocho actividades del SGSI, en la herramienta o en el documento. | Cláusula 5.3 y control A.5.2 |

**Criterio de calidad:** un objetivo como "mejorar la seguridad" no es medible. Un objetivo válido indica qué se mide, la meta, el plazo y el responsable.

## Fase 3. Gestión de activos

**Propósito:** identificar lo que la organización debe proteger y entender sus dependencias.

**Módulos de la herramienta:** *Gestión de activos* (Activos) y, de forma opcional, *Análisis de Impacto al Negocio*.

**Resultados mínimos esperados:**

| N.º | Resultado |
|---|---|
| 3.1 | Al menos **cuatro activos primarios** (información y procesos de negocio) y **seis activos de soporte** (sistemas, servicios, personas, instalaciones) identificados por el estudiante a partir del caso. |
| 3.2 | Relaciones de dependencia entre activos de soporte y activos primarios registradas en la herramienta. |
| 3.3 | Propiedades de seguridad (confidencialidad, integridad y disponibilidad, como mínimo) valoradas para cada activo primario, con justificación. |
| 3.4 | Objetivos de recuperación (RTO y RPO) definidos para al menos dos activos primarios críticos, con justificación de negocio. |
| 3.5 | Titular (dueño) asignado a cada activo, coherente con los roles de la Fase 1. |

**Preguntas que el documento debe responder:**

- ¿Qué activo de soporte tiene más activos primarios dependiendo de él y qué implica eso para el riesgo?
- ¿Por qué se asignaron esos valores de disponibilidad y esos tiempos de recuperación?

## Fase 4. Gestión de riesgos

**Propósito:** valorar y tratar los riesgos de seguridad de la información del alcance del SGSI con un método consistente.

**Módulos de la herramienta:** *Catálogo* (Bibliotecas, Matrices de riesgo, Amenazas), *Riesgo* (Evaluaciones de riesgos, Escenarios de riesgo), *Operaciones* (Controles aplicados) y *Gobernanza* (Aceptaciones de riesgo).

**Resultados mínimos esperados:**

| N.º | Resultado | Referencia |
|---|---|---|
| 4.1 | Criterios de riesgo definidos en el documento: escalas de probabilidad e impacto, niveles de riesgo y **criterios de aceptación con el cargo que puede aceptar cada nivel**. La matriz elegida en la herramienta debe ser coherente con esos criterios. | ISO/IEC 27001:2022, 6.1.2 a); ISO/IEC 27005:2022 |
| 4.2 | Una evaluación de riesgos sobre el perímetro del SGSI. | ISO/IEC 27001:2022, 6.1.2 |
| 4.3 | Al menos **ocho escenarios de riesgo** identificados por el estudiante, cada uno con activos afectados, amenaza, vulnerabilidad (en la descripción) y dueño del riesgo. Al menos dos deben derivarse de las cuestiones del contexto de la Fase 2. | 6.1.2 c) |
| 4.4 | Para cada escenario: controles existentes, riesgo actual, controles adicionales planificados (con responsable y fecha), riesgo residual y opción de tratamiento. | 6.1.2 d) y e); 6.1.3 |
| 4.5 | Al menos **una aceptación de riesgo** registrada en la herramienta, aprobada por el cargo que corresponde según los criterios de 4.1. | 6.1.3 f) |
| 4.6 | Plan de acción exportado desde la herramienta e incorporado como anexo del documento. | 6.1.3 e) |

**Criterio de calidad:** el riesgo residual debe ser coherente con los controles planificados. Un escenario cuyo riesgo residual no baja necesita una explicación, y uno que baja sin controles adicionales es un error de valoración.

## Fase 5. Marco de trabajo ISO/IEC 27001:2022

**Propósito:** evaluar el estado de cumplimiento frente a ISO/IEC 27001:2022 y construir la Declaración de Aplicabilidad a partir de los riesgos.

**Módulos de la herramienta:** *Catálogo* (Bibliotecas, Marcos), *Cumplimiento* (Auditorías, Evidencias, Resumen) e *Informes* (Declaración de aplicabilidad).

**Resultados mínimos esperados:**

| N.º | Resultado |
|---|---|
| 5.1 | Una auditoría del perímetro del SGSI frente a ISO/IEC 27001:2022 que incluya las cláusulas y la Declaración de aplicabilidad. |
| 5.2 | Evaluación justificada de **al menos ocho requisitos de las cláusulas 4 a 10**, entre ellos 4.3, 5.2, 6.1.2 y 6.1.3. |
| 5.3 | Evaluación justificada de **al menos veinte controles del Anexo A**, elegidos por el estudiante a partir de los riesgos de la Fase 4, que incluya **al menos tres controles no aplicables** con una justificación válida basada en el alcance. |
| 5.4 | Reutilización de los controles aplicados y las políticas de las fases 2 y 4 como respaldo de los requisitos de la auditoría, sin duplicarlos. |
| 5.5 | Al menos **tres evidencias** registradas y vinculadas a requisitos o controles. |
| 5.6 | Declaración de Aplicabilidad generada desde *Informes*, enriquecida con la evaluación de riesgos de la Fase 4 e incorporada como anexo del documento. |

**Criterio de calidad:** todo control del Anexo A vinculado a un riesgo debe aparecer como aplicable. Un control excluido no puede justificarse por falta de presupuesto o de tiempo.

## Fase 6. Integración y presentación a la dirección

**Propósito:** traducir el trabajo en la herramienta en decisiones para la junta directiva.

**Módulos de la herramienta:** *Visión general* (Analíticas, Informes) y *Cumplimiento* (Resumen).

**Resultados mínimos esperados:**

1. **Informe ejecutivo para la junta** (máximo dos páginas, sin lenguaje técnico): estado de cumplimiento de ISO/IEC 27001:2022, los cinco riesgos principales con su nivel actual y residual, el avance de los objetivos de seguridad, las acciones prioritarias y las decisiones que se solicitan a la junta.
2. **Análisis crítico** (400 a 500 palabras):
   - ¿Qué aporta una plataforma GRC frente a gestionar el SGSI en documentos y hojas de cálculo?
   - ¿Qué aspectos de la gobernanza no puede resolver la herramienta por sí sola?
   - ¿Qué implica para Café Andino mantener una herramienta de código abierto autoalojada (soporte, actualizaciones, protección de los datos registrados en ella y Ley 1581 de 2012)?
   - ¿Qué cambiaría el estudiante en su propio diseño después de terminar la actividad?

## Productos y condiciones de entrega

### 1. Documento de evidencias de la actividad (un solo archivo PDF)

Todo el trabajo se entrega en **un único documento PDF**. Este documento debe permitir que un lector que no conoce la herramienta entienda qué se hizo, cómo se hizo en CISO Assistant y por qué se tomó cada decisión. No se reciben archivos sueltos: las exportaciones de la herramienta se incorporan como anexos dentro del mismo PDF.

**Nombre del archivo:** `Taller2_Gobernanza_CISO_Assistant_Apellido_Nombre.pdf`  
**Extensión máxima:** 30 páginas, sin contar portada, referencias ni anexos.

**Estructura obligatoria del documento:**

| Sección | Contenido |
|---|---|
| Portada | Nombre del estudiante, curso, título de la actividad, fecha, enlace al repositorio de GitHub y enlace al video de YouTube. |
| 1. Introducción | Propósito del documento, descripción breve de CISO Assistant [n] y versión instalada. |
| 2. Entorno de trabajo | Versión de CISO Assistant y evidencia de la instancia propia en funcionamiento (terminal con `docker compose ps` y pantalla de inicio con el nombre del estudiante). |
| 3. Supuestos | Supuestos agregados al caso por el estudiante. |
| 4 a 9. Desarrollo de las fases 1 a 6 | Una sección por fase con tres partes obligatorias (ver abajo). |
| 10. Informe ejecutivo para la junta | Resultado de la Fase 6. |
| 11. Análisis crítico | Resultado de la Fase 6. |
| 12. Conclusiones | Conclusiones del estudiante. |
| Referencias | Lista en formato IEEE. |
| Anexos | Exportaciones de la herramienta incorporadas al PDF: evaluación de riesgos, plan de acción, auditoría ISO/IEC 27001:2022 y Declaración de Aplicabilidad. |

**Cada sección de fase (4 a 9) debe tener tres partes:**

1. **Uso de la herramienta:** qué módulos y funciones de CISO Assistant se usaron y cómo se usaron, explicado con palabras propias y con apoyo en la documentación oficial citada en formato IEEE. No se trata de copiar la documentación, sino de explicar el procedimiento seguido.
2. **Evidencia del desarrollo:** capturas de pantalla numeradas como figuras (Fig. n) y tablas (TABLA n) que muestren los resultados mínimos de la fase en la instancia propia, con el nombre del estudiante o del dominio y la fecha visibles.
3. **Análisis y decisiones:** justificación de las decisiones tomadas y respuesta a las preguntas de la fase, con citas a las normas y al caso.

**Incorporación de las exportaciones como anexos:** los archivos exportados en PDF se unen al final del documento; los exportados en Excel, CSV o HTML se incluyen como tablas o capturas legibles. Cada anexo debe tener título y referencia desde el texto (por ejemplo, "ver Anexo C").

### 2. Repositorio en GitHub

Repositorio **público** llamado `gobernanza-si-taller2-ciso-assistant-apellido`, con esta estructura:

```text
gobernanza-si-taller2-ciso-assistant-apellido/
├── README.md                                   (basado en plantillas/README_ESTUDIANTE.md)
└── Taller2_Gobernanza_CISO_Assistant_Apellido_Nombre.pdf   (documento único de entrega)
```

No deben subirse contraseñas, archivos de configuración ni la carpeta de instalación de la herramienta.

### 3. Video en YouTube

- Duración: entre 8 y 10 minutos.
- El estudiante aparece en cámara al inicio y luego comparte la pantalla.
- Debe mostrar **en vivo** la instancia propia de CISO Assistant y recorrer las seis fases, explicando las decisiones más importantes, no solo las pantallas.
- Visibilidad: **No listado** o **Público**.
- Título: `Taller 2 Gobernanza CISO Assistant - Apellido Nombre`.

### 4. Entrega en Blackboard

1. Adjuntar el documento PDF.
2. Escribir en el cuadro de texto el enlace al repositorio de GitHub y el enlace al video de YouTube (los mismos que aparecen en la portada del PDF).

Enlaces que no abran, repositorios privados o videos privados se calificarán como no entregados en el criterio correspondiente.

## Norma IEEE

El documento PDF debe aplicar la norma IEEE en su totalidad. Es un criterio de evaluación independiente con peso de 15 puntos.

- **Citas en el texto:** numéricas entre corchetes, en orden de aparición: [1], [2]. Para varias fuentes: [1], [3] o [2]-[4]. Para citar una cláusula o un control: [1, cl. 6.1.3] o [1, Anexo A, A.5.19].
- **Lista de referencias:** al final, con el título **Referencias**, numerada en orden de aparición y no en orden alfabético. Mínimo **ocho (8) referencias**, que incluyan ISO/IEC 27001:2022, ISO/IEC 27005:2022, la documentación de CISO Assistant y al menos dos normas o modelos colombianos.
- **Figuras:** "Fig. 1", "Fig. 2", con el título **debajo** de la imagen y mencionadas en el texto antes de aparecer.
- **Tablas:** "TABLA I", "TABLA II", con el título **encima** de la tabla.

**Ejemplos de referencias:**

[1] *Information Security, Cybersecurity and Privacy Protection - Information Security Management Systems - Requirements*, ISO/IEC 27001:2022, International Organization for Standardization, Ginebra, Suiza, 2022.

[2] *Information Security, Cybersecurity and Privacy Protection - Guidance on Managing Information Security Risks*, ISO/IEC 27005:2022, International Organization for Standardization, Ginebra, Suiza, 2022.

[3] intuitem, "CISO Assistant Community Edition," versión X.Y.Z, software de código abierto, licencia AGPLv3, 2026. [En línea]. Disponible: https://github.com/intuitem/ciso-assistant-community

[4] intuitem, "CISO Assistant documentation," 2026. [En línea]. Disponible: https://intuitem.gitbook.io/ciso-assistant

[5] Congreso de la República de Colombia, "Ley Estatutaria 1581 de 2012, por la cual se dictan disposiciones generales para la protección de datos personales," *Diario Oficial*, no. 48.587, oct. 2012.

[6] Ministerio de Tecnologías de la Información y las Comunicaciones, "Resolución 02277 de 2025, por la cual se actualiza el Modelo de Seguridad y Privacidad de la Información," Bogotá, Colombia, jun. 2025.

## Criterios de evaluación (100 puntos)

| Criterio | Puntos | Nivel alto | Nivel medio | Nivel bajo |
|---|:---:|---|---|---|
| Fase 1. Configuración inicial | 5 | Estructura de dominio, perímetros y usuarios coherente con el caso y con separación de funciones; alcance claro (5) | Estructura incompleta o alcance ambiguo (3-4) | Sin estructura propia (0-2) |
| Fase 2. Gobernanza | 15 | Cuestiones, partes interesadas, objetivos medibles, políticas y RACI completos y vinculados entre sí (13-15) | Elementos incompletos o objetivos no medibles (8-12) | Elementos genéricos o ausentes (0-7) |
| Fase 3. Gestión de activos | 10 | Inventario completo con dependencias, propiedades de seguridad, RTO y RPO justificados y titulares coherentes (9-10) | Inventario incompleto o sin justificación (5-8) | Inventario mínimo sin relaciones (0-4) |
| Fase 4. Gestión de riesgos | 20 | Criterios con niveles de autoridad; ocho o más escenarios completos y coherentes; residual consistente con los controles; aceptación registrada por el cargo correcto (17-20) | Escenarios incompletos, valoraciones poco consistentes o aceptación sin autoridad definida (10-16) | Menos de cinco escenarios o valoraciones sin sustento (0-9) |
| Fase 5. ISO/IEC 27001:2022 | 15 | Cláusulas y veinte o más controles evaluados con justificación; exclusiones válidas; controles reutilizados; evidencias; Declaración de Aplicabilidad coherente con los riesgos (13-15) | Justificaciones genéricas, exclusiones débiles o controles duplicados (8-12) | Auditoría incompleta o incoherente con los riesgos (0-7) |
| Fase 6. Informe ejecutivo y análisis crítico | 5 | Informe sin tecnicismos con decisiones concretas; análisis crítico argumentado (5) | Informe técnico o análisis descriptivo (3-4) | Ausente (0-2) |
| Norma IEEE | 15 | Citas correctas, incluidas citas a cláusulas y controles; ocho o más referencias completas en orden de aparición; figuras y tablas según IEEE (13-15) | Errores menores o referencias incompletas (8-12) | Formato distinto a IEEE o menos de cinco referencias (0-7) |
| Repositorio en GitHub | 5 | Público, con README completo y el documento PDF único (5) | README incompleto (3-4) | Inaccesible o vacío (0-2) |
| Video en YouTube | 10 | Recorre las seis fases en vivo en la instancia propia y explica las decisiones (9-10) | Omite fases o solo muestra pantallas (5-8) | Inaccesible o sin demostración (0-4) |

**Condición transversal del documento PDF:** en cada fase, el puntaje se asigna considerando las tres partes exigidas (uso de la herramienta, evidencia del desarrollo y análisis). Una fase sin evidencia en capturas de la instancia propia se califica en el nivel bajo, aunque el texto esté completo.

## Recursos

- intuitem, repositorio de CISO Assistant: https://github.com/intuitem/ciso-assistant-community
- intuitem, documentación oficial de CISO Assistant: https://intuitem.gitbook.io/ciso-assistant
- ISO, ISO/IEC 27001:2022 (ficha oficial y vista previa): https://www.iso.org/standard/27001
- ISO, ISO/IEC 27001:2022/Amd 1:2024 (acceso gratuito): https://www.iso.org/standard/88435.html
- ISO, ISO/IEC 27005:2022 (ficha oficial y vista previa): https://www.iso.org/standard/80585.html
- MinTIC, Resolución 02277 de 2025, actualización del MSPI: https://mintic.gov.co/portal/inicio/Sala-de-prensa/Noticias/403045:A-traves-de-la-Resolucion-02277-de-2025-el-Ministerio-TIC-actualiza-el-Modelo-de-Seguridad-y-Privacidad-de-la-Informacion
- Función Pública, Guía para la Gestión Integral del Riesgo en Entidades Públicas, versión 7: https://www.funcionpublica.gov.co/eva_/publicaciones
- NIST, El Marco de Seguridad Cibernética (CSF) 2.0, traducción oficial al español: https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.spa.pdf
- Ley 1581 de 2012: https://www.funcionpublica.gov.co/eva/gestornormativo/norma.php?i=49981

## Archivos del repositorio

| Archivo | Uso |
|---|---|
| [`datos/CASO_CAFE_ANDINO.md`](datos/CASO_CAFE_ANDINO.md) | Información del caso. |
| [`plantillas/PLANTILLA_INFORME.md`](plantillas/PLANTILLA_INFORME.md) | Estructura del documento PDF único de entrega. |
| [`plantillas/README_ESTUDIANTE.md`](plantillas/README_ESTUDIANTE.md) | Modelo del README del repositorio del estudiante. |
