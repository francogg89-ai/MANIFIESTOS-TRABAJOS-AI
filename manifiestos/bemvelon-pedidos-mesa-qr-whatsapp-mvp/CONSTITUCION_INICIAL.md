# Constitución inicial

WORK_ID: bemvelon-pedidos-mesa-qr-whatsapp-mvp
CARRIL: Y
METHOD_REPO: francogg89-ai/METODO-AI
METHOD_SHA: 0f5fd48ae57752419e9e63faa6b69071df966377
MANIFEST_REPO: francogg89-ai/MANIFIESTOS-TRABAJOS-AI
MANIFEST_PATH: manifiestos/bemvelon-pedidos-mesa-qr-whatsapp-mvp/MANIFIESTO_TRABAJO.md
MANIFEST_SHA: 5f479829ab8f4704000048344666f45923e1ddef
PROJECT_REPO: francogg89-ai/MANIFIESTOS-TRABAJOS-AI
PROJECT_PATH: manifiestos/bemvelon-pedidos-mesa-qr-whatsapp-mvp/PROJECT.md
PROJECT_SHA: e3fb4947c61d6455b8e8f8cad6ad6f11f04395ca
WORK_REPO: francogg89-ai/work-claude-y
AUDIT_REPO: francogg89-ai/audit-chatgpt-y

## Entorno y acceso

Runtime del auditor: ChatGPT web.

Runtime del constructor: Claude Code local en Windows.

Raíz local declarada por el humano:

`C:/Franco_Bemvelon`

Clones esperados bajo esa raíz:

- `C:/Franco_Bemvelon/work-claude-y`
- `C:/Franco_Bemvelon/audit-chatgpt-y`
- `C:/Franco_Bemvelon/Bemvelon-automatizado`
- `C:/Franco_Bemvelon/METODO-AI`
- `C:/Franco_Bemvelon/MANIFIESTOS-TRABAJOS-AI`

Fuentes auxiliares esperadas, si están materializadas localmente:

- `C:/Franco_Bemvelon/work-claude-e`
- `C:/Franco_Bemvelon/audit-chatgpt-e`

Las rutas locales son superficies de trabajo, no autoridad documental. Antes de depender de ellas se comprueba que correspondan a los repositorios e identidades declarados.

El constructor escribe únicamente en el clone de `work-claude-y`. El auditor escribe únicamente en `audit-chatgpt-y`.

`Bemvelon-automatizado`, los repositorios del método, manifiestos y las fuentes del carril E son sólo lectura para los roles ordinarios.

Credenciales y tokens de Fudo permanecen fuera de Git. Este documento no contiene ni fija su valor ni una ruta secreta. Antes de un probe autenticado deberá comprobarse una referencia local segura y disponible; si no existe, el constructor registra la necesidad por la vía del auditor. Ninguna credencial se copia a work, audit, prompts, QR, navegador o WhatsApp.

## Capacidades iniciales

### Constructor

Entorno: Claude Code local, Windows, bajo `C:/Franco_Bemvelon`.

Puede:

- leer METHOD_SHA, manifiesto, PROJECT y fuentes auxiliares a identidades exactas;
- leer el sistema objetivo `Bemvelon-automatizado`;
- escribir y commitear únicamente en `work-claude-y`;
- diseñar e implementar el candidato del MVP dentro de work;
- ejecutar pruebas locales no destructivas;
- usar documentación pública necesaria para resolver el diseño;
- reutilizar como evidencia, sin modificar, el discovery de Fudo del carril E;
- realizar probes autenticados de Fudo únicamente de lectura cuando exista referencia segura a credenciales y la acción respete el alcance aprobado.

No puede:

- escribir en `audit-chatgpt-y`;
- escribir directamente en `Bemvelon-automatizado`;
- desplegar a producción;
- modificar DNS, proyecto Vercel o configuración externa real;
- crear, rotar o ampliar credenciales;
- escribir pedidos, ventas, mesas u otros datos mutativos en Fudo;
- enviar mensajes automáticos por WhatsApp;
- ampliar el alcance reservado al humano.

### Auditor

Entorno: ChatGPT web.

Puede:

- leer método, manifiesto, PROJECT, work, sistema objetivo y fuentes auxiliares;
- verificar evidencias, diffs, pruebas y referencias exactas;
- escribir y commitear únicamente en `audit-chatgpt-y`;
- emitir veredictos, necesidades humanas, transiciones y relevos conforme al método.

No puede:

- modificar `work-claude-y`;
- modificar `Bemvelon-automatizado`;
- desplegar;
- operar credenciales secretas;
- convertir una decisión técnica en una decisión humana salvo que realmente cambie intención, riesgo o capacidad reservada.

### Integración al sistema objetivo

La integración final hacia `francogg89-ai/Bemvelon-automatizado` no pertenece a la escritura ordinaria del constructor ni del auditor.

Antes de integrar se requiere:

- candidato auditado;
- comprobación del HEAD real del sistema objetivo y de cualquier drift respecto de `2882025761bf630251d54e7431b1ee93d6ef76fb`;
- operación de integración identificada, trazable y limitada al perímetro de PROJECT;
- verificación posterior de que el sitio principal continúa funcionando y que el circuito de carta/pedidos funciona en la ruta pública aprobada.

## Política de ejecución

La política de relevo inicial es manual: el auditor aplica un relevo cuando lo exige el humano o cuando el método determina que la instancia vigente no debe continuar. No se fija una cadencia artificial de intervenciones.

El transporte admite como máximo dos reintentos seguros adicionales conforme al METHOD_SHA.

Las decisiones reservadas al humano son las enumeradas en el manifiesto. No existe gate humano automático entre unidades después de un PLAN aprobado, salvo necesidad humana material conforme al método.

### Estado de la integración de adaptadores

El METHOD_SHA fijado incluye el host local y los adaptadores descritos en `transporte/LOCAL.md`.
La prueba de referencia completó un intercambio real ChatGPT web ↔ Claude Code y recuperó
su respuesta final sin reenviar el mensaje. Eso acredita el mecanismo ensayado, no todas
las capacidades de la versión reutilizable ni los permisos actuales del carril Y.

Antes del arranque, el agente local debe verificar:
- conexión del módulo browser.mjs con las fábricas de pestañas del runtime CUA autorizado;
- fresh y recuperación current de ambos roles con identidades distintas y explícitas;
- fidelidad UTF-8, saltos, comillas, rutas Windows y texto largo;
- captura completa ligada al mensaje esperado y detención ante envío incierto;
- cwd y origin correctos de work, acceso del auditor a GitHub y permisos de construcción.

La configuración y el prompt de arranque se preparan en CONTINUIDAD-AI bajo
`Y/bemvelon-pedidos-mesa-qr-whatsapp-mvp/`. Son instrucciones de transporte, no una
nueva autoridad sobre el alcance. Los registros runtime permanecen locales fuera de work/audit.

Estado: trabajo constituido; arranque preparado; comprobación local de la versión reutilizable
pendiente. No se ha iniciado Y. El orquestador no crea BOOTSTRAP ni declara aprobadas capacidades
no verificadas. Las facultades de constructor y auditor definidas arriba permanecen vigentes.

El guardado para renovar coordinadamente los tres agentes no forma parte de esta entrega.
La recuperación técnica conserva las identidades existentes y no autoriza repetir entregas.

## Fuentes auxiliares

SOURCE_REPOS:

- `francogg89-ai/Bemvelon-automatizado@2882025761bf630251d54e7431b1ee93d6ef76fb` — baseline del sistema objetivo; sólo lectura durante construcción y auditoría ordinarias.
- `francogg89-ai/work-claude-e@10373bec01f8637c96bf816ab252297aef06debf` — evidencia técnica previa de Fudo sobre la cuenta real de Bemvelon; sólo lectura.
- `francogg89-ai/audit-chatgpt-e@34d90206c2a14827408d42eaad6fdc4d454803ac` — auditoría histórica asociada al discovery; sólo lectura.

Estas fuentes no sustituyen las comprobaciones del estado real cuando una propiedad pueda haber cambiado.
