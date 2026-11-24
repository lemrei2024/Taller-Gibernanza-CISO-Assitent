# Estructura del documento PDF único de entrega

> Esta plantilla muestra la estructura obligatoria del documento. El contenido, la redacción y las decisiones son del estudiante. El documento se entrega en un solo archivo PDF, con la norma IEEE y con los anexos incluidos.

---

## Portada

- Nombre del estudiante
- Curso: Gobernanza en Seguridad de la Información
- Taller 2. Actividad autónoma: gobierno, activos, riesgos y cumplimiento ISO/IEC 27001 con CISO Assistant
- Fecha
- Repositorio de GitHub: `https://github.com/usuario/gobernanza-si-taller2-ciso-assistant-apellido`
- Video de YouTube: `https://www.youtube.com/watch?v=...`

---

## Contenido

_Tabla de contenido con números de página._

## 1. Introducción

Propósito del documento y descripción breve de CISO Assistant [n].

**Versión de CISO Assistant:** _X.Y.Z_

## 2. Entorno de trabajo

- Versión de CISO Assistant y de Kali Linux.
- Referencia al Taller 1 (instalación).

Fig. 1. _Terminal de Kali con usuario, fecha, versiones de Docker y estado de los contenedores._

Fig. 2. _Pantalla de inicio de CISO Assistant con el nombre del estudiante en el menú lateral._

## 3. Supuestos

_Lista de supuestos agregados al caso._

## 4. Fase 1. Configuración inicial

### 4.1 Uso de la herramienta

_Explicación con palabras propias de los módulos y funciones usados, con citas a la documentación [n]._

### 4.2 Evidencia del desarrollo

_Capturas numeradas (Fig. n) y tablas (TABLA n) con los resultados mínimos de la fase._

### 4.3 Análisis y decisiones

_Justificación de las decisiones y respuesta a las preguntas de la fase._

## 5. Fase 2. Gobernanza

### 5.1 Uso de la herramienta
### 5.2 Evidencia del desarrollo
### 5.3 Análisis y decisiones

## 6. Fase 3. Gestión de activos

### 6.1 Uso de la herramienta
### 6.2 Evidencia del desarrollo
### 6.3 Análisis y decisiones

## 7. Fase 4. Gestión de riesgos

### 7.1 Uso de la herramienta
### 7.2 Evidencia del desarrollo
### 7.3 Análisis y decisiones

## 8. Fase 5. Marco de trabajo ISO/IEC 27001:2022

### 8.1 Uso de la herramienta
### 8.2 Evidencia del desarrollo
### 8.3 Análisis y decisiones

## 9. Fase 6. Integración

### 9.1 Uso de la herramienta
### 9.2 Evidencia del desarrollo

## 10. Informe ejecutivo para la junta directiva

_Máximo dos páginas, sin lenguaje técnico._

## 11. Análisis crítico

_400 a 500 palabras._

## 12. Conclusiones

---

## Referencias

[1] _..._

[2] _..._

_(mínimo ocho referencias en formato IEEE, en orden de aparición)_

---

## Anexos

- Anexo A. Evaluación de riesgos exportada desde CISO Assistant.
- Anexo B. Plan de acción exportado desde CISO Assistant.
- Anexo C. Auditoría ISO/IEC 27001:2022 exportada desde CISO Assistant.
- Anexo D. Declaración de Aplicabilidad generada desde CISO Assistant.

---

## Recomendaciones para generar el PDF único

- Redactar el documento en un procesador de texto (Word, LibreOffice Writer o Google Docs) y exportarlo a PDF.
- Unir al final los anexos exportados en PDF. En Kali Linux se puede hacer con el comando `pdfunite documento.pdf anexoA.pdf anexoB.pdf anexoC.pdf anexoD.pdf Taller2_Gobernanza_CISO_Assistant_Apellido_Nombre.pdf` (paquete `poppler-utils`).
- Verificar que las capturas sean legibles al 100 % de zoom y que la fecha y el nombre del estudiante se distingan.
