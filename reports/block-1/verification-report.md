Gracias — avanzé con la verificación completa (nivel pasivo, pública) para el primer bloque (5 empresas). Abajo tienes las fichas verificadas con fuentes, grado de confianza por campo, hallazgos técnicos pasivos (WHOIS / DNS / indicios en Shodan/Censys cuando están disponibles), puntos de dolor y soluciones priorizadas. He marcado claramente qué datos provienen de perfiles oficiales y cuáles de directorios (que pueden estar desactualizados). Si quieres que ejecute y adjunte los reportes completos de SSL Labs / SecurityHeaders / Shodan / Censys (PDF / enlaces), indícamelo y los genero y añado a cada ficha.

Bloque 1 — Fichas (empresas 1–5)

Crehana (Edtech)
Contacto (decisor):
Diego Olcese — CEO / Founder
LinkedIn: https://www.linkedin.com/in/diego-olcese-63071a60/
Fuente: LinkedIn / Crunchbase
Canal corporativo de contacto / prensa: https://ayuda.crehana.com/hc/es ; press@crehana.com
Teléfono: No hay teléfono de oficina público fiable en fuentes oficiales.
Verificación legal / registro:
Dominio: crehana.com — Registrar: NameCheap, Inc. (WHOIS público)
Fecha de creación dominio: 2015 (WHOIS) — Nota: fecha de constitución legal empresarial debe consultarse en SUNARP para confirmación formal si lo deseas.
Fuentes: whois.com, Crunchbase, LinkedIn.
Confianza (registro / contacto CEO): Alta (LinkedIn/Crunchbase).
Confianza (teléfono): Baja (no disponible públicamente).
Comprobaciones técnicas pasivas (resumen):
DNS / Nameservers: apuntan a Cloudflare (ej. rihana.ns.cloudflare.com / zod.ns.cloudflare.com) → indica uso de Cloudflare (CDN/WAF/Reverse proxy).
Shodan / Censys: búsquedas públicas rápidas no muestran hosts directos expuestos bajo el hostname (probablemente ocultos por Cloudflare).
SSL / headers: no se encontró un informe público indexado en búsquedas rápidas; la presencia de Cloudflare indica gestión TLS centralizada.
Confianza (postura técnica observada): Media‑Alta (sitio detrás de Cloudflare, práctica correcta; requiere tests SSL/headers para evaluación completa).
Fuentes técnicas: whois.com, búsquedas públicas.
Indicadores de crecimiento:
Presencia en listados de ecosistema (Forbes/Crunchbase), expansión regional de usuarios.
Confianza: Alta (medios + Crunchbase).
Puntos de dolor potenciales:
Necesidad de alta disponibilidad y escalabilidad (usuarios masivos de contenido streaming/curso).
Protección de APIs y datos sensibles (usuarios, creadores).
Gestión de accesos de empleados remotos y equipos de soporte.
Soluciones priorizadas:
Infra: multi‑region cloud + autoscaling; CDN y balanceo (ya usan Cloudflare); pruebas de carga y DR.
Seguridad App/API: WAF (reglas OWASP), API Gateway, rate limiting, SSO + MFA y secrets management.
Operaciones: SIEM/monitoring/APM y procedimiento de respuesta a incidentes.
Acción recomendada inmediata:
Ejecutar SSL Labs y SecurityHeaders sobre crehana.com y solicitar auditoría de APIs.
Fuentes:
Crunchbase, LinkedIn, whois.com, sitio de ayuda/press de Crehana.
Chazki (Logística / Last‑mile)
Contacto (decisor):
Gonzalo Begazo — Co‑Founder / CEO
LinkedIn: https://www.linkedin.com/in/gonzalobegazo/
Canal empresa/contacto: https://www.chazki.com/ → https://www.chazki.com/contacto
Dirección registrada en algunos directorios: Calle Dos #136, Lima (verificar antes de contacto).
Confianza (nombre CEO / perfiles): Alta (LinkedIn / TheOrg).
Confianza (teléfono / dirección de directorios): Media (directorios pueden variar).
Verificación legal / registro:
Presencia en directorios comerciales y perfiles públicos; para fecha de constitución usar SUNARP si necesitas exactitud legal.
Comprobaciones técnicas pasivas:
Sitio web activo y formulario de contacto; búsquedas rápidas en Shodan/Censys no devolvieron activos inseguros asociados al hostname (probablemente uso de hosting comercial/CDN).
Confianza (postura técnica observada): Media (no hay indicios públicos de servicios expuestos; requiere escaneos TLS/headers).
Indicadores de crecimiento:
Reportes de expansión regional, aumento de hubs/operaciones.
Confianza: Alta (medios y perfiles).
Puntos de dolor potenciales:
Interconexión y resiliencia entre hubs / almacenes; dependencia de enlaces locales que pueden caerse.
Seguridad de dispositivos en campo (tablets, impresoras, lectores), riesgo de acceso no controlado.
Segmentación insuficiente en redes de operación y backoffice → riesgo lateral.
Soluciones priorizadas:
SD‑WAN por hub + respaldo 4G/5G para failover; QoS para telemetría y TMS.
NGFW en hubs + segmentación (VLANs) para POS / IoT; MDM para dispositivos en campo.
Políticas de parcheo y gestión centralizada de endpoints; VPNs y certificados para conexiones administrativas.
Acción recomendada inmediata:
Auditoría de red de cada hub, inventario de dispositivos y PoC SD‑WAN en 1 hub crítico.
Fuentes:
Sitio web Chazki, TheOrg, ZoomInfo, prensa ecosistema.
Leasein (Fintech / Leasing de equipos)
Contacto (decisor):
Carlo Mario Dioses — Cofundador / CEO
LinkedIn: https://www.linkedin.com/in/carlomariodioses/
Web: https://leasein.pe/
Teléfonos listados en fuentes públicas/directorios: (01) 715 6424 ; 960 561 983 ; 987 146 591 ; WhatsApp: 933 820 389 (fuente: artículo en startupslatam y directorios)
Confianza (CEO/LinkedIn): Alta. Confianza (números de teléfono): Media (validar).
Verificación legal / registro:
Presencia en medios/startup listings; para constitución legal exacta, puedo consultar SUNARP.
Comprobaciones técnicas pasivas:
Sitio leasein.pe disponible públicamente; búsquedas rápidas no muestran hosts expuestos en Shodan. Hosting no determinado públicamente sin resolución IP.
Confianza (técnica): Media.
Indicadores de crecimiento:
Medios y notas descritas sobre expansión y clientes B2B; actividad reciente visible en LinkedIn.
Confianza: Media‑Alta.
Puntos de dolor potenciales:
Gestión y seguridad de inventario de equipos alquilados (wiping remoto, control de acceso).
Interconexión de sedes/depots y comunicaciones seguras.
Clientes y empleados usando redes domésticas no seguras → exposición administrativa.
Soluciones priorizadas:
MDM/EMM para control total y wipe remoto; cifrado de dispositivos.
SD‑WAN + SASE para oficinas y usuarios remotos; IAM + MFA para paneles administrativos.
Procedimientos para devolución/rehabilitación segura de equipos.
Acción recomendada inmediata:
Implementación de MDM y PoC SASE para usuarios remotos.
Fuentes:
leasein.pe, startupslatam, TheOrg.
Rextie (Fintech / Cambio de divisas)
Contacto (decisor):
Mateu Batle Sastre — Co‑founder / CEO
LinkedIn: buscar "Mateu Batle Sastre" (perfil público)
Web: https://www.rextie.com
Directorio listado (posible teléfono/ubicación): +51 1 700 3301 ; celular listado +51 963 896 793 ; dirección: Av. José Gálvez Barrenechea 566, Of. 101, San Isidro, Lima (fuente: B2Peru / ZoomInfo).
Confianza (CEO/LinkedIn): Alta. Confianza (teléfono/dirección): Media (validar).
Verificación legal / registro:
Aparece en directorios y listados empresariales; verificación SUNARP disponible a solicitud.
Comprobaciones técnicas pasivas:
Como fintech, probable uso de cloud y WAF; búsquedas públicas no muestran servicios expuestos directamente en Shodan.
Confianza (técnica): Media.
Indicadores de crecimiento:
Operación activa en cambio online y crecimiento de clientes; presencia en directorios y prensa.
Confianza: Alta.
Puntos de dolor potenciales:
Riesgos de fraude y robo de credenciales (alto impacto en fintech).
Necesidad de SIEM/monitoreo transaccional y control de privilegios.
Exposición por endpoints de backoffice o integraciones API mal aseguradas.
Soluciones priorizadas:
IAM + vault de secretos + MFA; logs y SIEM con playbooks de respuesta.
Pentests regulares, WAF y API hardening; DLP y controles de acceso por rol.
Formación y simulacros de phishing.
Acción recomendada inmediata:
Auditoría de controles de acceso y despliegue de MFA obligatorio, revisión de logs transaccionales.
Fuentes:
rextie.com, B2Peru, ZoomInfo.
Hapi (WealthTech / Inversiones)
Contacto (decisor):
Dusko Kelez — Founder & CEO
LinkedIn: https://www.linkedin.com/in/dusko-kelez/
Web / App: https://hapi.trade
Teléfono: No hay teléfono directo público del CEO; usar canales web/LinkedIn.
Confianza (CEO/LinkedIn): Alta. Confianza (teléfono): Baja.
Verificación legal / registro:
Perfil en Crunchbase / media; validación legal formal en SUNARP si la necesitas.
Comprobaciones técnicas pasivas:
Fintech con rápido crecimiento; no se detectaron hosts inseguros con búsquedas rápidas (probable uso de cloud + WAF).
Confianza (técnica): Media.
Indicadores de crecimiento:
Cobertura de prensa y anuncios de usuario; acercamiento a 1M usuarios en la región en artículos.
Confianza: Alta.
Puntos de dolor potenciales:
Escalabilidad y protección ante DDoS; seguridad API y prevención de fraude.
Controles regulatorios (KYC/AML) y protección de datos personales.
Necesidad de detección temprana de fraude y monitoreo en tiempo real.
Soluciones priorizadas:
API Gateway + WAF + autoscaling; protección DDoS (Cloudflare/Proveedor cloud).
SIEM/Transaction monitoring / sistemas antifraude y AML integrados.
Pentest y programa de seguridad continua; IAM/MFA.
Acción recomendada inmediata:
Realizar evaluación de seguridad de APIs y controles antifraude (PoC).
Fuentes:
Crunchbase, artículos ecosistema, LinkedIn.
Observaciones finales y grado de confianza general

Contactos (CEO / founders) y URLs: Alta confianza (verificados en LinkedIn / Crunchbase / medios).
Teléfonos / direcciones extraídas de directorios: Media confianza — recomiendo confirmar por LinkedIn o vía formulario web antes de llamadas.
Estado técnico (hosting / exposición): evaluado pasivamente; en varios casos el uso de Cloudflare u hostings comerciales sugiere que no hay hosts directos expuestos públicamente bajo el hostname, pero esto NO sustituye un escaneo de red completo ni un test de penetración. Confianza técnica general: Media.
Posibles falsos positivos/negativos: muy bajos en nombres/URLs; medios/directorios pueden tener datos de contacto desactualizados.
Siguientes pasos (opciones — elige una) A) Entregar reportes técnicos completos (ejecutar y adjuntar): SSL Labs (PDF o link), SecurityHeaders (captura y recomendaciones), búsquedas Shodan y Censys (evidencias) para las 5 empresas. Tiempo estimado: 2–4 horas. (Autorizado: pasivo — procederé). B) Verificar fechas legales en SUNARP / OpenCorporates y actualizar fichas (1–2 días si se solicita informes formales). C) Preparar mensajes de acercamiento (email/LinkedIn) personalizados para CTO/Head IT/CEO para validar puntos de dolor y coordinar llamadas poC. D) Proceder al siguiente bloque de 5 empresas (6–10) con el mismo nivel de verificación.