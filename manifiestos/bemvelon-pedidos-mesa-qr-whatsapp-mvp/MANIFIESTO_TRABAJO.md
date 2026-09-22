# Manifiesto de trabajo

WORK_ID: bemvelon-pedidos-mesa-qr-whatsapp-mvp

## Objetivo y motivo

Construir una primera versión simple del circuito digital complementario de pedidos de mesa de Bemvelon.

La atención presencial mediante moza continúa siendo el canal normal de servicio y no será sustituida por el sistema digital.

Cuando una moza abre una mesa en la operación de Bemvelon, queda asociada como responsable de esa atención según la información disponible en Fudo.

La moza puede tomar directamente el primer pedido y cualquier pedido posterior de la mesa mediante el circuito habitual.

Cuando los clientes estén efectivamente en condiciones de realizar un pedido, la moza podrá además habilitar una sesión digital temporal correspondiente a esa mesa y entregarles un código QR.

Desde ese momento, los clientes dispondrán simultáneamente de dos alternativas:

- realizar pedidos directamente a la moza;
- realizar pedidos mediante el circuito digital de carta y WhatsApp de Bemvelon.

El canal digital no será obligatorio ni sustituirá la relación entre la mesa y la moza responsable.

Los pedidos recibidos mediante WhatsApp serán revisados y procesados por la cajera, mientras que los pedidos realizados directamente a la moza continuarán siendo procesados por ella mediante la operación habitual de Fudo.

El objetivo de esta primera versión es ofrecer a los clientes una vía adicional para pedir cuando lo deseen, sin obligarlos a esperar a la moza y sin modificar innecesariamente el funcionamiento actual del salón.

## Resultado observable y éxito

El trabajo se considerará conseguido cuando pueda realizarse de extremo a extremo un circuito real como el siguiente:

1. Una moza abre una mesa mediante la operación habitual de Bemvelon y queda asociada como responsable cuando Fudo permita obtener esa relación.
2. La moza puede tomar directamente un pedido de esa mesa sin necesidad de activar ningún circuito digital.
3. Cuando corresponda, la moza habilita una sesión digital temporal para esa mesa.
4. El sistema genera una autorización correspondiente a esa sesión y un código QR asociado.
5. Los clientes reciben el QR y pueden acceder al circuito digital de Bemvelon.
6. Desde ese momento, la mesa conserva simultáneamente la posibilidad de pedir directamente a la moza o utilizar el canal digital.
7. Mediante el canal digital, el cliente puede acceder a una carta web de Bemvelon.
8. La carta obtiene de Fudo los datos utilizables de productos y precios sin exponer credenciales de Fudo al navegador.
9. El cliente puede seleccionar productos, cantidades y agregar observaciones cuando corresponda.
10. El sistema compone un pedido legible identificado con la mesa y la sesión autorizada.
11. El cliente envía ese pedido al WhatsApp de Bemvelon.
12. La cajera puede identificar a qué mesa pertenece el pedido y revisar su contenido.
13. La cajera carga o procesa manualmente en Fudo el pedido recibido por WhatsApp.
14. La cajera confirma al cliente que el pedido digital fue efectivamente tomado mediante una confirmación inequívoca equivalente a `PEDIDO TOMADO ✅`.
15. La activación del canal digital no impide que esa misma mesa continúe realizando otros pedidos directamente a su moza.

La prueba de éxito deberá demostrar al menos:

- una mesa operada únicamente mediante atención tradicional;
- una mesa con sesión digital habilitada;
- un pedido tomado directamente por la moza;
- un pedido realizado mediante la carta y enviado por WhatsApp;
- convivencia de ambos canales dentro de una misma sesión de mesa.

## Alcance y exclusiones

Incluye:

- preservación del circuito tradicional de atención por moza;
- identificación, cuando sea técnicamente disponible, de la moza responsable de la mesa;
- habilitación voluntaria del canal digital por parte del personal;
- generación de una sesión temporal autorizada para una mesa;
- generación del código QR correspondiente;
- identificación segura de la mesa sin confiar únicamente en un número modificable por el cliente;
- acceso al WhatsApp de Bemvelon;
- carta web para clientes alojada bajo `estudioautomatizacion.com`;
- lectura de la información necesaria de productos y precios desde Fudo;
- selección de productos y cantidades;
- observaciones de pedido cuando corresponda;
- composición del pedido para WhatsApp;
- identificación de mesa y sesión en el pedido recibido;
- operación compatible con múltiples clientes de una misma mesa;
- coexistencia de pedidos presenciales y pedidos digitales;
- procesamiento humano de los pedidos digitales por parte de la cajera;
- confirmación humana de recepción del pedido digital;
- mecanismo para impedir la reutilización indefinida de autorizaciones antiguas.

Quedan fuera de esta primera versión:

- obligación de utilizar WhatsApp para realizar pedidos;
- sustitución de la moza por el sistema digital;
- creación automática del pedido dentro de Fudo;
- modificación automática de comandas Fudo;
- respuestas automáticas de WhatsApp que requieran WhatsApp Business Platform;
- chatbot o agente conversacional autónomo;
- cobro o pago desde la carta;
- cierre automático de mesa;
- eliminación de la cajera del circuito digital;
- recomendaciones mediante IA;
- reservas;
- pedidos externos que no estén asociados a una sesión autorizada de mesa;
- automatizaciones de stock y reposición pertenecientes a otros trabajos.

La arquitectura no deberá impedir que posteriormente se automaticen algunos de estos pasos mediante trabajos independientes.

## Restricciones, riesgos y decisiones humanas

El canal digital será complementario. Su activación nunca deberá convertirlo en el único canal disponible para una mesa.

La moza conserva la capacidad de tomar pedidos directamente antes y después de habilitar el QR.

La habilitación digital deberá ser una acción deliberada asociada a una mesa en atención y no una consecuencia automática de que la mesa exista o haya sido abierta.

La autorización de mesa deberá representar una sesión concreta y no consistir únicamente en un número fácilmente falsificable.

Las credenciales de Fudo no deberán exponerse en código cliente, URLs, códigos QR ni conversaciones de WhatsApp.

La primera versión priorizará simplicidad operacional y verificabilidad sobre automatización.

La fuente de productos y precios deberá aprovechar Fudo cuando sus capacidades verificadas sean suficientes. Cualquier dato adicional propio deberá distinguirse de los datos cuya autoridad corresponde a Fudo.

Una autorización de mesa deberá poder expirar o invalidarse para evitar que un QR o enlace conservado permita efectuar pedidos indefinidamente después de terminada la atención.

La existencia de una sesión autorizada no implica que cualquier mensaje recibido deba convertirse automáticamente en una comanda.

La aceptación efectiva de los pedidos digitales continúa siendo humana y se materializa mediante la confirmación de la cajera.

Los pedidos realizados directamente a la moza quedan dentro del circuito operativo presencial existente y no requieren confirmación digital.

El diseño técnico concreto del mecanismo de firma, almacenamiento de sesiones, sincronización de productos, interfaz de carta y generación de QR corresponde al constructor y deberá ser verificable por el auditor.

Quedan reservadas al humano las decisiones que cambien el alcance operativo, especialmente:

- hacer obligatorio el canal digital;
- eliminar o reducir el papel operativo de la moza;
- eliminar a la cajera del circuito digital;
- permitir creación automática de pedidos en Fudo;
- habilitar pedidos externos sin mesa autorizada;
- habilitar pagos;
- adoptar automatización de WhatsApp que envíe mensajes en representación de Bemvelon;
- cambiar la autoridad sobre precios o productos respecto de Fudo.
