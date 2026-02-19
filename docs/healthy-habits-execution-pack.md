# Paquete de ejecución 12 semanas + arquitectura + regulación + cuadro de mando

> Documento de continuación del plan maestro 2026–2032.
>
> Objetivo: convertir la estrategia en ejecución operativa inmediata con criterios medibles.
>
> **Aviso**: contenido orientativo para diseño de producto/negocio clínico. Validar con asesoría legal y regulatoria local antes de operar.

---

## 1) Backlog detallado de 12 semanas

## 1.1 Supuestos de trabajo
- Segmento inicial: adultos 35–55 con riesgo cardiometabólico incipiente.
- Modalidad de servicio: programa clínico de 12 semanas con seguimiento híbrido (digital + médico).
- Alcance MVP: onboarding clínico, plan personalizado, integración wearable básica, asistente con escalado médico y panel clínico.

## 1.2 Estructura del backlog

### Épicas
- **E1. Fundamentos clínicos y compliance**
- **E2. Producto paciente (app móvil/web app responsive)**
- **E3. Plataforma clínica (panel profesionales)**
- **E4. Integraciones de datos (wearables/lab)**
- **E5. Motor de alertas y personalización**
- **E6. Analítica, observabilidad y operación**

### Semanas 1–2: Discovery cerrado + arquitectura base

**Objetivos**
- Congelar alcance MVP, riesgos clínicos y estructura de datos.

**Historias clave**
1. Como médico líder, quiero una plantilla estandarizada de evaluación inicial para todos los pacientes.
2. Como producto, quiero definir outcomes primarios/secundarios del piloto.
3. Como legal/compliance, quiero una matriz inicial de consentimientos y tratamiento de datos por país.
4. Como ingeniería, quiero arquitectura base con entornos dev/staging/prod.

**Entregables**
- Plantilla clínica v1 + protocolo de escalamiento.
- Diccionario de datos v1 (eventos, señales, planes, alertas).
- Decisión de stack (cloud, DB, colas, observabilidad).
- Documento de riesgos y controles mínimos.

**Criterios de aceptación**
- 100% de campos clínicos obligatorios definidos.
- 2 outcomes primarios y 4 secundarios aprobados.
- Checklist legal mínimo firmado por responsable.

### Semanas 3–4: Onboarding clínico + perfilado + consentimientos

**Objetivos**
- Habilitar alta de pacientes con base clínica sólida.

**Historias clave**
1. Como paciente, quiero completar onboarding clínico guiado en <20 minutos.
2. Como médico, quiero ver baseline clínico y hábitos en un resumen único.
3. Como compliance, quiero trazabilidad de consentimiento por versión y fecha.

**Entregables**
- Flujo de onboarding (datos personales, antecedentes, hábitos, objetivos).
- Motor de formularios versionado.
- Gestión de consentimiento (aceptación, revocación, exportación).

**Criterios de aceptación**
- Tasa de onboarding completado >80% en test interno.
- Consentimiento auditable (quién, cuándo, qué versión).
- Errores críticos de formulario = 0 en QA funcional.

### Semanas 5–6: Plan personalizado + tareas + mensajería

**Objetivos**
- Activar intervención inicial y adherencia semanal.

**Historias clave**
1. Como médico, quiero crear un plan de 12 semanas con objetivos semanales.
2. Como paciente, quiero tareas diarias claras con recordatorios configurables.
3. Como equipo clínico, quiero mensajería segura paciente-profesional.

**Entregables**
- Constructor de plan (nutrición/sueño/actividad/estrés).
- Sistema de tareas y check-ins.
- Mensajería segura con SLA de respuesta.

**Criterios de aceptación**
- 100% de pacientes piloto con plan activo <48 h tras onboarding.
- Notificaciones con entrega >95% (push/email).
- Mensajes con trazabilidad y cifrado en tránsito.

### Semanas 7–8: Integraciones wearables + normalización

**Objetivos**
- Incorporar señales continuas con calidad suficiente para toma de decisiones.

**Historias clave**
1. Como paciente, quiero conectar mi wearable en <5 minutos.
2. Como data engineer, quiero normalizar unidades, zonas horarias y frecuencia de muestreo.
3. Como médico, quiero ver tendencias semanales y variabilidad relevante.

**Entregables**
- Conectores iniciales (Apple Health/Google Fit + 1 proveedor extra).
- Pipeline de ingestión/normalización con controles de calidad.
- Vista clínica de tendencias (sueño, actividad, FC/HRV si disponible).

**Criterios de aceptación**
- >70% de pacientes piloto con wearable conectado.
- Latencia ingestión p95 < 15 min para señales diarias.
- Tasa de dato inválido < 5% tras normalización.

### Semanas 9–10: Alertas clínicas + asistente IA con guardrails

**Objetivos**
- Habilitar detección de riesgo y soporte conversacional seguro.

**Historias clave**
1. Como clínico, quiero alertas por niveles (0–3) priorizadas por riesgo.
2. Como paciente, quiero recomendaciones conductuales no ambiguas.
3. Como compliance clínico, quiero auditoría completa de prompts y respuestas.

**Entregables**
- Motor de reglas clínicas con umbrales por paciente.
- Asistente IA con políticas de seguridad (sin diagnóstico ni cambios farmacológicos).
- Flujo de escalado humano automático cuando aplica red flag.

**Criterios de aceptación**
- Tiempo de escalado nivel 2 < 24 h.
- 100% de respuestas IA trazables.
- 0 respuestas IA que violen políticas críticas en set de pruebas.

### Semanas 11–12: Cuadro de mando + piloto operativo + retrospectiva

**Objetivos**
- Operar cohorte piloto y cerrar ciclo de aprendizaje.

**Historias clave**
1. Como fundador, quiero un dashboard único con KPI clínicos/producto/negocio.
2. Como equipo clínico, quiero revisión semanal de seguridad y decisiones.
3. Como producto, quiero priorizar backlog post-piloto por impacto medible.

**Entregables**
- Dashboard ejecutivo con umbrales semaforizados.
- Informe de resultados del piloto (operación, seguridad, outcomes).
- Backlog de fase 2 priorizado (impacto/esfuerzo/riesgo).

**Criterios de aceptación**
- 1 informe de piloto con decisiones go/no-go.
- KPI críticos con captura automática diaria.
- Lista de 10 mejoras priorizadas para siguiente trimestre.

## 1.3 Definición de Done (DoD) transversal
- Seguridad: sin vulnerabilidades críticas conocidas abiertas.
- Legal: consentimiento y política de privacidad vigentes y versionadas.
- Clínica: regla de escalamiento documentada y testeada.
- Data: calidad mínima (completitud >90% en campos críticos).
- Observabilidad: logs, métricas y trazas activas en endpoints core.

---

## 2) Arquitectura técnica concreta

## 2.1 Stack recomendado (pragmático 2026)

### Frontend
- App móvil: **React Native** (time-to-market y equipo unificado).
- Panel clínico web: **Next.js**.

### Backend
- API principal: **TypeScript + NestJS** (modularidad, validación, testing).
- Servicio de reglas/alertas: microservicio dedicado (NestJS o Python FastAPI si ML temprano).
- Orquestación IA: servicio propio con políticas, versionado y auditoría.

### Datos
- OLTP: **PostgreSQL** (entidades clínicas, planes, usuarios, consentimientos).
- Time-series: **TimescaleDB** (extensión Postgres) o InfluxDB si carga masiva.
- Cache: **Redis**.
- Data warehouse: **BigQuery** o **Snowflake** (según presupuesto/equipo).
- Object storage: S3/GCS para artefactos y backups cifrados.

### Mensajería/colas
- Event bus: **Kafka** (si escala prevista alta) o **RabbitMQ/SQS** (MVP rápido).
- Jobs asíncronos: **BullMQ** (si Node), colas separadas por criticidad.

### Observabilidad
- Métricas: **Prometheus + Grafana**.
- Logs: **OpenSearch/ELK** o proveedor gestionado.
- Trazas: **OpenTelemetry + Jaeger/Tempo**.
- Alerting técnico: PagerDuty/Opsgenie.

### Seguridad
- AuthN/AuthZ: OIDC + JWT, RBAC por rol clínico.
- Secret management: Vault/Secrets Manager.
- Cifrado: TLS 1.2+ en tránsito y AES-256 en reposo.

## 2.2 Servicios (bounded contexts)
1. **identity-service**: cuentas, roles, sesiones, MFA.
2. **consent-service**: versionado y evidencia legal de consentimientos.
3. **patient-profile-service**: historia clínica y baseline.
4. **plan-service**: creación y seguimiento del plan personalizado.
5. **task-adherence-service**: tareas, check-ins, recordatorios.
6. **wearable-ingestion-service**: conexión y recolección de señales.
7. **data-normalization-service**: validación y estandarización.
8. **risk-scoring-service**: score diario de riesgo/adherencia.
9. **alert-service**: generación/priorización/escalado de alertas.
10. **assistant-orchestrator-service**: chatbot, guardrails, auditoría.
11. **clinical-console-service**: vistas agregadas para profesionales.
12. **analytics-service**: KPI, cohortes y reportes.

## 2.3 Modelo de datos mínimo (tablas core)
- `users`, `roles`, `organizations`
- `patients`, `clinical_baseline`, `medical_history`
- `consents`, `consent_versions`, `consent_events`
- `plans`, `plan_modules`, `plan_revisions`
- `tasks`, `task_logs`, `adherence_scores`
- `wearable_sources`, `raw_observations`, `normalized_observations`
- `risk_scores`, `alerts`, `alert_actions`
- `chat_sessions`, `chat_messages`, `assistant_audit`
- `appointments`, `clinical_notes`, `outcomes`

## 2.4 Contratos de eventos (ejemplos)
- `patient.onboarded`
- `wearable.data_ingested`
- `wearable.data_normalized`
- `risk.score_computed`
- `alert.triggered`
- `alert.escalated`
- `assistant.response_generated`
- `clinical.intervention_recorded`

## 2.5 SLO iniciales (servicio)
- API paciente: disponibilidad mensual >= 99.5%.
- Ingestión wearable: p95 latencia < 15 min.
- Panel clínico: p95 respuesta < 2.5 s.
- Escalado alerta nivel 2: confirmación operativa < 24 h.

## 2.6 Estrategia de despliegue
- Infra IaC (Terraform).
- CI/CD con pruebas automáticas (unit + contract + smoke).
- Entornos separados dev/staging/prod.
- Feature flags para despliegue progresivo.
- Backups diarios + prueba de restauración mensual.

---

## 3) Matriz de riesgos regulatorios por país objetivo

> Países objetivo sugeridos para fase inicial hispanohablante + expansión: **España, México, Colombia**, con ruta opcional a **EE. UU.**.

## 3.1 Tabla resumida

| País | Marco de datos/salud (referencia general) | Riesgo principal | Prob. | Impacto | Mitigación prioritaria |
|---|---|---|---|---|---|
| España | GDPR + LOPDGDD | Tratamiento de datos de salud sin base jurídica robusta | Media | Muy alto | DPIA, consentimiento explícito, DPO, minimización y registro de actividades |
| España | Marco sanitario/publicidad sanitaria | Claims de prevención/antiaging no sustentados | Media | Alto | Comité científico, revisión legal de claims, evidencia interna auditada |
| México | LFPDPPP + regulación sanitaria aplicable | Transferencias internacionales sin controles contractuales | Media | Alto | Contratos y cláusulas, política de transferencias, segregación de datos sensibles |
| México | Telemedicina/acto médico | Ambigüedad en alcance del chatbot vs acto médico | Alta | Alto | Protocolos de escalado, disclaimers claros, supervisión médica obligatoria |
| Colombia | Ley de protección de datos + habeas data | Gestión deficiente de autorización y revocatoria | Media | Alto | Gestión de consentimiento granular, portal de derechos ARCO local equivalente |
| Colombia | Habilitación de servicios de salud digitales | Operación sin adecuación documental | Media | Muy alto | Due diligence regulatorio previo, auditoría de habilitación por servicio |
| EE. UU. (opcional) | HIPAA (si aplica), leyes estatales de privacidad | Riesgo contractual y técnico con PHI/ePHI | Media | Muy alto | BAA con proveedores, segregación de PHI, controles y auditoría técnica |
| Multi-país | Transferencia transfronteriza | Arquitectura no preparada para residencia de datos | Alta | Alto | Estrategia de data residency por región y cifrado con llaves por jurisdicción |

## 3.2 Riesgos transversales críticos
1. **Clasificación regulatoria del producto**: wellness vs dispositivo/software médico.
2. **Gobernanza de IA clínica**: explicabilidad, trazabilidad y supervisión humana.
3. **Ciberseguridad**: exposición de credenciales, fuga de datos, ransomware.
4. **Publicidad y claims**: prometer resultados clínicos sin evidencia suficiente.

## 3.3 Controles mínimos antes de producción
- DPIA/PIA por país objetivo.
- Mapa de tratamiento de datos y base legal por flujo.
- Política de retención/eliminación por tipo de dato.
- Proceso de respuesta a incidentes (RACI + simulacros).
- Auditoría legal de términos, consentimiento y claims comerciales.

---

## 4) Cuadro de mando con KPI y umbrales de decisión

## 4.1 Diseño de dashboard (4 capas)
- **Capa clínica**: seguridad y outcomes.
- **Capa producto**: activación, adherencia, retención.
- **Capa operativa**: SLA clínico y rendimiento técnico.
- **Capa negocio**: unidad económica y crecimiento sostenible.

## 4.2 KPI propuestos (con umbrales)

| KPI | Definición | Verde | Ámbar | Rojo | Cadencia |
|---|---|---:|---:|---:|---|
| Adherencia semanal | % tareas planificadas completadas por paciente/semana | >= 70% | 50–69% | < 50% | Semanal |
| Retención semana 12 | % cohorte activa al final del programa | >= 65% | 45–64% | < 45% | Quincenal |
| Escalado alerta N2 en tiempo | % alertas nivel 2 contactadas <24 h | >= 95% | 85–94% | < 85% | Diario |
| Falsos positivos de alerta | % alertas sin acción clínica relevante | <= 20% | 21–35% | > 35% | Semanal |
| Tiempo respuesta panel clínico p95 | Latencia p95 de vistas críticas | <= 2.5 s | 2.6–4 s | > 4 s | Diario |
| Latencia ingestión wearable p95 | Tiempo evento->dato utilizable | <= 15 min | 16–30 min | > 30 min | Diario |
| Incidentes de privacidad severos | Nº incidentes severidad alta/mes | 0 | 1 | >=2 | Mensual |
| Margen bruto por paciente activo | Ingreso - coste directo por paciente | >= 55% | 35–54% | < 35% | Mensual |
| LTV/CAC | Ratio de valor vida cliente / coste adquisición | >= 3.0 | 1.8–2.9 | < 1.8 | Mensual |
| NPS clínico percibido | Satisfacción neta del programa | >= 45 | 20–44 | < 20 | Mensual |

## 4.3 Reglas de decisión automática
- Si **retención semana 12** entra en rojo 2 ciclos seguidos: congelar adquisición y priorizar adherencia/experiencia.
- Si **falsos positivos** >35% durante 3 semanas: recalibrar reglas y revisar umbrales por subcohorte.
- Si **escalado N2** <85%: activar protocolo de contingencia operativa clínica.
- Si **margen bruto** <35% por 2 meses: revisar pricing, coste asistencial y alcance del servicio.

## 4.4 Ritual de gobierno de datos/KPI
- Comité operativo semanal (producto + clínica + data).
- Comité de seguridad/compliance mensual.
- Comité estratégico trimestral (go/no-go y expansión).

---

## 5) Plan de implementación inmediato (próximos 14 días)

1. Nombrar responsables por frente: clínico, técnico, compliance, operaciones.
2. Congelar definición de KPI y diccionario de métricas (single source of truth).
3. Montar arquitectura base y observabilidad mínima en staging.
4. Configurar motor de consentimientos y auditoría como requisito de salida.
5. Seleccionar 1 país primario y 1 secundario para no fragmentar ejecución.

---

## 6) Criterio final de éxito de este paquete

Este documento será útil solo si termina en:
- tickets ejecutables por sprint,
- responsables con fecha,
- umbrales que disparen decisiones,
- evidencia auditable en clínica, dato y negocio.

Sin esto, seguirá siendo una estrategia “bonita” sin valor operativo.

---

## 7) Definiciones matemáticas de KPI (para evitar ambigüedad)

## 7.1 Fórmulas canónicas

1. **Adherencia semanal (%)**
   `adherencia = (tareas_completadas / tareas_planificadas) * 100`

2. **Retención semana 12 (%)**
   `retencion_w12 = (pacientes_activos_semana_12 / pacientes_iniciados_cohorte) * 100`

3. **Falsos positivos de alerta (%)**
   `fp_alertas = (alertas_sin_accion_clinica / alertas_totales) * 100`

4. **SLA escalado N2 (%)**
   `sla_n2 = (alertas_n2_contactadas_<24h / alertas_n2_totales) * 100`

5. **Margen bruto por paciente activo (%)**
   `margen_bruto = ((ingreso_paciente - coste_directo_paciente) / ingreso_paciente) * 100`

6. **LTV/CAC**
   `ltv = arpu_mensual * margen_bruto_% * vida_media_meses`
   `ratio_ltv_cac = ltv / cac`

## 7.2 Reglas de cómputo
- Toda métrica debe tener timestamp de corte (`as_of_date`) y versión de cálculo (`metric_version`).
- Todo KPI operativo debe poder recalcularse desde datos crudos.
- Cambios de definición deben registrarse en changelog y aplicarse desde una fecha efectiva.

---

## 8) Supuestos financieros mínimos y sensibilidad (escenario base)

> Importante: cifras orientativas para modelado inicial. Ajustar con tus costes reales de operación y estructura salarial.

## 8.1 Escenario base de cohorte (12 semanas)
- Cohorte inicial: **100 pacientes**.
- Precio programa medio: **EUR 120–220/mes equivalente**.
- Coste clínico directo mensual por paciente: **EUR 45–90**.
- Coste tecnológico + soporte mensual por paciente: **EUR 15–35**.
- Coste total directo mensual estimado: **EUR 60–125**.

## 8.2 Umbrales de sostenibilidad
- Si precio medio < coste total directo + 25% margen de seguridad: modelo no sostenible.
- Si retención <45% en semana 12: pausar crecimiento y corregir propuesta de valor.
- Si LTV/CAC <1.8 durante 2 meses: recortar canales de adquisición no rentables.

## 8.3 Prueba de estrés (obligatoria mensual)
Ejecutar 3 escenarios:
1. **Optimista**: +20% retención, -10% coste clínico.
2. **Base**: supuestos actuales.
3. **Adverso**: -20% retención, +15% coste clínico, +10% CAC.

Decisión: mantener, ajustar pricing, o reducir alcance clínico-operativo.

---

## 9) Plan de validación empírica por fases (con evidencia trazable)

## 9.1 Fase de factibilidad (0–3 meses)
- Validar flujo onboarding -> plan -> adherencia -> revisión clínica.
- Salida mínima: >70% onboarding completo, >60% adherencia media semana 4.

## 9.2 Fase de efectividad operativa (4–9 meses)
- Comparar cohorte activa vs cohorte histórica interna.
- Ajustar por edad, sexo, baseline de riesgo y adherencia.
- Salida mínima: mejora estadística en al menos 1 outcome primario predefinido.

## 9.3 Fase de robustez (9–18 meses)
- Diseños prospectivos pragmáticos por subpoblaciones.
- Auditoría externa de metodología y reproducibilidad.
- Salida mínima: consistencia de resultados en 2 cohortes independientes.

## 9.4 Criterios anti-sesgo
- Registrar abandonos como desenlace relevante, no excluirlos del análisis central.
- Separar análisis de eficacia clínica y satisfacción percibida.
- No modificar outcome primario después de ver resultados (evitar p-hacking operativo).

---

## 10) Registro de decisiones críticas (template operativo)

Usar una tabla de control con estos campos:
- `decision_id`
- `fecha`
- `owner`
- `hipotesis`
- `kpi_impactados`
- `riesgo_asociado`
- `evidencia`
- `resultado_esperado`
- `fecha_revision`
- `estado` (abierta/cerrada/revertida)

Regla: ninguna decisión de producto clínico entra en producción sin `owner`, `evidencia` y `fecha_revision`.

---

## 11) Qué haría mañana a las 08:00 (ejecución extrema, realista)

1. Congelar ICP y outcomes primarios en 1 página firmada por liderazgo clínico y producto.
2. Asignar responsables únicos por cada épica (sin ownership compartido ambiguo).
3. Activar dashboard mínimo con 5 KPI diarios: adherencia, SLA N2, falsos positivos, latencia p95, incidentes.
4. Ejecutar revisión legal de claims comerciales y textos del asistente IA.
5. Abrir piloto de 20 pacientes controlados antes de llegar a 100.
6. Programar comité semanal fijo (60 min, agenda cerrada, decisiones registradas).

Resultado esperado en 30 días: claridad operativa, menos ruido, y primera señal objetiva de tracción o necesidad de pivot.
