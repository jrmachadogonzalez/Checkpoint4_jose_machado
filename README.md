# Checkpoint 4 - Sincronización del Cerebro Agéntico con Ecosistemas de Negocio

Workflow de n8n que integra Gmail, HubSpot (CRM) y Slack mediante conectores OAuth2, con controles de seguridad no-code:

- **IF anti auto-reply**: corta el bucle infinito de respuestas automáticas.
- **Lookup previo a Create en CRM**: evita duplicados de contactos (Error 409).
- **Create Draft (HITL)**: la respuesta generada por IA queda como borrador, requiere aprobación humana antes de enviarse.
- **Set de limpieza de payload**: valida y limpia los datos antes de enviarlos a Slack.

**Nota técnica**: Gmail y Slack usan autenticación OAuth2 nativa. HubSpot usa autenticación por Service Key (token), ya que la plataforma migró la creación de apps OAuth2 públicas a un flujo exclusivo vía CLI.

Archivo: `checkpoint4_machado_jose.json` — importable directamente en n8n.
