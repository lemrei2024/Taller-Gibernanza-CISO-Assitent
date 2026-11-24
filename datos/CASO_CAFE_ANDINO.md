# Caso Café Andino S.A.S.

> Caso ficticio con fines académicos. Las personas y empresas mencionadas no existen.
> El estudiante debe identificar por su cuenta las cuestiones del contexto, las partes interesadas, los activos, los riesgos y los controles a partir de esta información. Los supuestos adicionales deben declararse en el documento de entrega.

## 1. La organización

Café Andino S.A.S. es una empresa colombiana de café especial fundada en 2012, con sede principal en Medellín. Compra café a 60 familias caficultoras de Antioquia y Huila, lo tuesta en su planta de Rionegro y lo vende en tres tiendas físicas (Medellín, Bogotá y Cali), en una tienda en línea y a cafeterías y hoteles bajo contratos corporativos. Tiene 120 empleados.

La tienda en línea tiene 45.000 clientes registrados y concentra el 40 % de las ventas. Las ventas de fin de año (noviembre y diciembre) representan el 30 % de los ingresos anuales.

## 2. Dirección estratégica 2026-2027

La junta directiva aprobó estos objetivos:

1. Duplicar las ventas en línea en dos años.
2. Abrir un canal de venta por WhatsApp atendido por un asistente automatizado.
3. Exportar café a Estados Unidos y Europa a partir de 2027; los compradores internacionales ya solicitaron evidencia de buenas prácticas de seguridad de la información.
4. Obtener la certificación ISO/IEC 27001 en 18 meses.
5. Recuperar la confianza de los clientes después del incidente de 2026.

## 3. Estructura y personas

| Cargo | Responsabilidades relacionadas con la información |
|---|---|
| Junta directiva (5 miembros) | Aprueba la estrategia y el presupuesto. Hasta ahora no ha recibido informes de seguridad. |
| Gerente general | Representante legal. Responde ante la junta por la operación. |
| Gerente financiera | Contabilidad, nómina, pagos, contrato con la pasarela de pagos. De ella depende el área de TI. |
| Directora comercial | Tienda en línea, mercadeo, base de clientes y relación con la agencia de marketing. |
| Jefe de TI (equipo de 3 personas) | Correo, equipos, consola del proveedor de nube, respaldos y soporte. |
| Coordinadora de talento humano | Ingreso y retiro de personal, formación. |
| Jefe de planta | Tostión, empaque, inventario y equipos de control de la tostadora. |
| Responsable de seguridad de la información (CISO) | Cargo creado en 2026, con reporte a la gerencia general. Es el rol del estudiante. |
| Auditora interna | Reporta a la junta directiva. |

## 4. Procesos

| Proceso | Descripción |
|---|---|
| Comercio electrónico | Venta, pago y despacho de pedidos en línea. |
| Ventas corporativas | Contratos con cafeterías y hoteles, con precios y condiciones confidenciales. |
| Mercadeo | Campañas y comunicación con clientes; parte del trabajo lo hace una agencia externa. |
| Atención al cliente | Peticiones, quejas, reclamos y solicitudes de los titulares de datos personales. |
| Producción y tostión | Compra de café, tostión, empaque e inventario en la planta de Rionegro. |
| Gestión financiera | Contabilidad, nómina y pagos a proveedores y caficultores. |
| Talento humano | Vinculación, retiro y formación de empleados. |

## 5. Tecnología y proveedores

- La **tienda en línea** funciona sobre una plataforma de comercio electrónico contratada como servicio (SaaS). Café Andino configura el catálogo y el diseño, pero no desarrolla software propio; las personalizaciones menores las contrata con una agencia externa.
- La **base de datos de clientes** (nombre, cédula, teléfono, dirección, correo e historial de compras) y sus respaldos están alojados en un **proveedor de nube** con centros de datos fuera de Colombia. El contrato es el estándar del proveedor, aceptado en línea, sin cláusulas específicas de seguridad.
- Los pagos se procesan en una **pasarela de pagos** externa; Café Andino no almacena datos de tarjetas.
- El **correo corporativo** es un servicio en la nube; las cuentas tienen contraseña individual, sin autenticación multifactor.
- El **software contable y de nómina** es un servicio en la nube de un proveedor colombiano.
- La **planta de Rionegro** tiene un equipo que controla la tostadora conectado a la red de la planta, que comparte conexión a internet con la oficina administrativa.
- Los empleados de las tiendas usan computadores compartidos y algunos usan su celular personal para consultar pedidos.
- Se hacen copias de respaldo nocturnas de la base de datos de clientes; nunca se ha probado su restauración.
- Hay antivirus en los equipos de las tiendas y la oficina.
- La planta tiene cámaras de seguridad y control de ingreso; la oficina de Medellín no tiene control de ingreso.

## 6. Hechos recientes

- **Agosto de 2026:** una asistente de mercadeo respondió un correo falso que suplantaba al proveedor de nube. Los atacantes accedieron a su cuenta y descargaron una hoja de cálculo con 2.300 registros de clientes. Un cliente se quejó en redes sociales tras recibir llamadas fraudulentas. La empresa no tenía procedimiento de respuesta a incidentes y tardó nueve días en determinar qué información se había expuesto.
- **Septiembre de 2026:** se descubrió que un analista de TI que se había retirado tres semanas antes conservaba una cuenta activa en la consola del proveedor de nube.
- **Octubre de 2026:** las lluvias intensas causaron dos cortes de energía en la planta de Rionegro; uno de ellos detuvo la tostión durante 14 horas.
- **Octubre de 2026:** el área de innovación propuso cargar el historial de compras de los clientes en una herramienta de inteligencia artificial en línea para entrenar el asistente de WhatsApp.
- **Noviembre de 2026:** el jefe de TI aplazó un parche crítico de la tienda en línea hasta enero, para no afectar la temporada alta.

## 7. Marco normativo y obligaciones

- Ley 1581 de 2012 y sus decretos reglamentarios: Café Andino es responsable del tratamiento de los datos personales de clientes, empleados y caficultores.
- Ley 1273 de 2009 sobre delitos informáticos.
- Obligaciones contractuales con la pasarela de pagos y con los clientes corporativos, que exigen confidencialidad de precios y condiciones.
- Requisitos de seguridad de la información de los futuros compradores internacionales.

## 8. Recursos disponibles

- Presupuesto de seguridad aprobado para 2027: equivalente al 2 % del presupuesto de tecnología.
- Equipo de seguridad: el CISO y el apoyo parcial de una persona del área de TI.
- La gerencia general está dispuesta a crear un comité de seguridad si el CISO lo justifica.
