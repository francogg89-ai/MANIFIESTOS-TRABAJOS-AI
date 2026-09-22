# Vinculación con el proyecto

PROJECT_ID: bemvelon-operaciones-inteligentes
WORK_ID: bemvelon-pedidos-mesa-qr-whatsapp-mvp

## Fuentes

- Sistema objetivo: `francogg89-ai/Bemvelon-automatizado@2882025761bf630251d54e7431b1ee93d6ef76fb`.
  - Publica `https://estudioautomatizacion.com/` y la carta de Bemvelon en `https://estudioautomatizacion.com/carta`.
  - Vercel publica `public/`.
  - `public/carta/` contiene la carta digital existente.
- Evidencia técnica previa de Fudo, sólo lectura: `francogg89-ai/work-claude-e@10373bec01f8637c96bf816ab252297aef06debf`.
  - Contiene discovery material de la API real de Bemvelon, incluyendo productos, precios, categorías, mesas y demás capacidades relevadas.
- Auditoría previa del discovery de Fudo, sólo lectura: `francogg89-ai/audit-chatgpt-e@34d90206c2a14827408d42eaad6fdc4d454803ac`.

Las fuentes históricas del carril E se reutilizan únicamente como evidencia y contexto técnico. No convierten este trabajo en continuación de aquel WORK_ID.

## Perímetro

El constructor desarrolla únicamente en `francogg89-ai/work-claude-y`. El auditor escribe únicamente en `francogg89-ai/audit-chatgpt-y`.

`francogg89-ai/Bemvelon-automatizado` es el destino de integración del resultado aceptado y se trata como sólo lectura durante la construcción y auditoría ordinarias.

Superficie prevista de integración en el sistema objetivo:

- `public/carta/**`: interfaz pública de la carta y circuito digital de mesa;
- nuevos paths de backend estrictamente necesarios para sesión de mesa, autorización, QR y acceso server-side a Fudo, por ejemplo `api/**`, si el diseño aprobado los requiere;
- `vercel.json` únicamente cuando sea necesario para publicar o enrutar el circuito aprobado;
- `dist/**` sólo si sigue cumpliendo función real como copia de origen de la carta y el plan conserva esa relación;
- documentación del repositorio únicamente cuando deba reflejar el sistema construido.

Ruta pública canónica inicial del MVP: `https://estudioautomatizacion.com/carta`.

Paths protegidos frente a cambios incidentales:

- `public/index.html`;
- `public/privacidad.html`;
- `MANIFIESTO_TRABAJO.md` histórico del trabajo anterior;
- cualquier secreto, token o credencial;
- contenido ajeno al circuito de carta/pedidos salvo necesidad técnica explícita, verificada y auditada.

No se crea otro proyecto Vercel ni se cambian DNS como parte del alcance ordinario.

Las credenciales de Fudo permanecen fuera de Git y sólo pueden utilizarse en superficies server-side o pruebas controladas autorizadas. Nunca se exponen al navegador, QR, URL pública ni WhatsApp.

## Concurrencia e integración

El baseline del sistema objetivo es el commit `2882025761bf630251d54e7431b1ee93d6ef76fb`. Antes de integrar deberá comprobarse el estado real de `Bemvelon-automatizado`; si avanzó, se re-deriva el impacto y se preservan los cambios ajenos.

No se fuerza historia ni se sobreescriben cambios concurrentes.

La separación work/audit se mantiene durante todo el trabajo. La aceptación de una entrega en `work-claude-y` no modifica por sí sola el repositorio objetivo.

La integración a `Bemvelon-automatizado` deberá ocurrir como acción identificada y verificable después de auditoría suficiente del candidato, respetando el perímetro anterior y comprobando nuevamente el estado del destino.

Conflictos entre el nuevo circuito y cambios concurrentes del sitio, despliegue o carta se devuelven al auditor para re-derivación. Las decisiones de dominio reservadas por el manifiesto siguen perteneciendo al humano.
