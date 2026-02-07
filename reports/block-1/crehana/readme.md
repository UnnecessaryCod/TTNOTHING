# Crehana — Reporte pasivo de conectividad y seguridad

Contacto y decisión:
- CEO: Diego Olcese — https://www.linkedin.com/in/diego-olcese-63071a60/
- Canal prensa/soporte: https://ayuda.crehana.com/hc/es ; press@crehana.com

Verificación legal / registro:
- Dominio: crehana.com
- Registrar WHOIS público: NameCheap, Inc.
- Fecha registro dominio (WHOIS): 2015
- Nota: Verificación formal de constitución (SUNARP) no realizada aún.

Comprobaciones técnicas pasivas:
- DNS / Nameservers: apuntan a Cloudflare (ej. rihana.ns.cloudflare.com / zod.ns.cloudflare.com) — indica uso de CDN/WAF/Reverse Proxy.
- Shodan / Censys: búsquedas públicas no retornaron hosts expuestos directamente bajo el hostname (probablemente protegido por Cloudflare).
- TLS / Headers: no se generó informe SSL Labs/ SecurityHeaders todavía. Recomendado ejecutar escaneo público y adjuntar PDF.

Indicadores de crecimiento:
- Presencia en Crunchbase y listados de ecosistema; expansión regional y gran base de usuarios.

Puntos de dolor identificados:
1. Disponibilidad y escalabilidad para contenido multimedia (alto tráfico simultáneo).
2. Protección de APIs y datos sensibles de usuarios y creadores.
3. Gestión segura de accesos de empleados y equipos de soporte.

Soluciones priorizadas (resumen):
1. Arquitectura y conectividad: multi-region cloud + autoscaling; CDN (Cloudflare ya presente); pruebas de carga y DR.
2. Seguridad de aplicaciones: WAF (Cloudflare rules + reglas OWASP), API Gateway con rate limiting, IAM/SSO + MFA.
3. Operaciones y respuesta: SIEM/APM, logging centralizado, runbooks y ejercicios DR.

Acciones inmediatas recomendadas:
- Ejecutar SSL Labs y SecurityHeaders y remediar hallazgos.
- Programar auditoría de APIs (pentest) y revisar reglas WAF en Cloudflare.

Grado de confianza (datos públicos):
- Contactos y URLs: Alta
- Teléfonos / direcciones: Baja/No disponibles
- Postura técnica (observada pasivamente): Media - uso de Cloudflare reduce exposición pero requiere verificación por tests.

Fuentes:
- https://www.crunchbase.com/organization/crehana
- WHOIS público: https://www.whois.com/whois/crehana.com
- Soporte: https://ayuda.crehana.com/hc/es
