Actúa como ejecutor documental del repositorio Legalbreto.

NO CREES NUEVOS DOCUMENTOS TODAVÍA.

Debes auditar exhaustivamente la estructura que acabas de crear para:

EXPEDIENTE_MAESTRO_MIGRATORIO_LUIS_BRETO/

OBJETIVO

Determinar si el expediente creado cumple realmente con el STANDARD MIGRACION definido para este proyecto y si su arquitectura documental es suficiente para presentar posteriormente el caso a un abogado.

REGLA FUNDAMENTAL

No debes asumir que un archivo está correctamente construido simplemente porque existe.

Debes abrir y revisar el contenido real de cada archivo.

==================================================
1. VALIDACIÓN DE METADATA
==================================================

Cada documento Markdown debe contener exactamente, como mínimo, estos campos YAML:

document_id:
title:
subtitle:
version:
status:
document_type:
classification:
owner:
jurisdiction:
language:
created:
last_updated:
review_status:
parent_document:
previous_document:
next_document:
case_type:
primary_authority:
related_authorities:
critical_pending_evidence:
integrity_rule:

Verifica:

- existencia;
- sintaxis YAML válida;
- consistencia;
- idioma español;
- coherencia entre documentos;
- referencias correctas;
- navegación anterior/siguiente;
- ausencia de metadata inventada.

Reporta cualquier incumplimiento.

==================================================
2. VALIDACIÓN DEL STANDARD MIGRACION
==================================================

Todos los documentos deberán cumplir esta estructura visual mínima:

YAML FRONT MATTER

# TÍTULO PRINCIPAL

## SUBTÍTULO

> **ESTADO DEL DOCUMENTO**

---

## SECCIÓN PRINCIPAL

### Subsección

---

## OTRA SECCIÓN

Las secciones deberán utilizar jerarquía Markdown real.

No aceptes:

- títulos escritos solamente como texto;
- separadores usados como sustituto de títulos;
- numeración plana sin jerarquía;
- tablas sin encabezados Markdown;
- metadata escrita fuera del YAML;
- documentos sin estructura visual.

==================================================
3. VALIDACIÓN DE ARQUITECTURA
==================================================

Determina si cada uno de los siguientes dominios contiene suficiente documentación para cumplir su propósito:

00_INDICE_EXPEDIENTE_MIGRATORIO

01_RESUMEN_EJECUTIVO_CASO_MIGRATORIO

02_LINEA_TIEMPO_CASO_MIGRATORIO

03_IDENTIFICACION_Y_DOCUMENTOS_PERSONALES

04_INGRESO_A_CHILE_Y_PROCEDIMIENTO_INICIAL

05_PROCEDIMIENTO_SANCIONATORIO_EXPULSION

06_ANTECEDENTES_REGULARIZACION_PDI

07_VINCULO_FAMILIAR_ACUERDO_UNION_CIVIL

08_SOLICITUD_RESIDENCIA_TEMPORAL_ID75098336

09_RESOLUCION_INADMISIBILIDAD_2600100434997

10_ANALISIS_JURIDICO_PARA_REVISION

11_COMUNICACIONES_Y_GESTIONES

12_ANEXOS

No consideres suficiente que un directorio contenga solamente README.md.

Determina qué documentación adicional requiere cada dominio.

==================================================
4. VALIDACIÓN DE TRAZABILIDAD
==================================================

Para cada hecho relevante determina si existe una relación trazable:

HECHO
→ DOCUMENTO
→ DIRECTORIO
→ REFERENCIA EN LÍNEA DE TIEMPO
→ REFERENCIA EN RESUMEN
→ POSIBLE RELEVANCIA JURÍDICA

Identifica:

- hechos sin documento;
- documentos sin relación con hechos;
- referencias rotas;
- documentos mencionados pero inexistentes;
- información pendiente de obtener;
- información que no debe afirmarse como hecho probado.

==================================================
5. VALIDACIÓN DE EVIDENCIA
==================================================

Clasifica cada antecedente relevante como:

A — DOCUMENTADO DIRECTAMENTE

B — DOCUMENTADO INDIRECTAMENTE

C — DECLARADO POR EL TITULAR

D — PENDIENTE DE OBTENCIÓN

E — REQUIERE REVISIÓN JURÍDICA

No conviertas nunca B, C, D o E en evidencia A.

==================================================
6. VALIDACIÓN DE INFORMACIÓN CRÍTICA
==================================================

Comprueba específicamente:

- Acta PDI de Colchane 11-05-2024.
- Carta de descargos.
- Parte Policial N°16177.
- Procedimiento sancionatorio iniciado en 2024.
- Resultado del procedimiento sancionatorio.
- Eventual decreto de expulsión.
- Declaración voluntaria N°33763535.
- Citación PDI febrero 2026.
- Declaración voluntaria N°34103883.
- Acuerdo de Unión Civil.
- Solicitud ID 75098336.
- Validación del vínculo chileno.
- Resolución Exenta N°2600100434997.
- Notificación de 28-07-2026.

Determina cuáles están disponibles y cuáles solamente están referenciados.

==================================================
7. VALIDACIÓN DE INTEGRIDAD
==================================================

No inventes:

- documentos;
- fechas;
- números de expediente;
- resoluciones;
- actuaciones administrativas;
- resultados;
- fundamentos jurídicos;
- estados procesales.

Cuando falte información escribe:

"PENDIENTE DE OBTENCIÓN"

Cuando exista una afirmación del titular sin respaldo documental escribe:

"ANTECEDENTE DECLARADO — PENDIENTE DE CORROBORACIÓN"

Cuando un documento solamente sea conocido porque otra autoridad lo cita escribe:

"ANTECEDENTE DOCUMENTALMENTE REFERENCIADO — COPIA PENDIENTE"

==================================================
8. VALIDACIÓN DE NAVEGACIÓN
==================================================

Verifica que:

00 → 01 → 02 → 03 → ... → 12

tenga navegación coherente.

Verifica también que los documentos secundarios indiquen correctamente:

parent_document:
previous_document:
next_document:

No permitas referencias a archivos inexistentes.

==================================================
9. VALIDACIÓN PARA EXPORTACIÓN PDF
==================================================

Determina si los documentos actuales pueden convertirse posteriormente a PDF sin perder:

- jerarquía;
- títulos;
- tablas;
- advertencias;
- metadata;
- referencias;
- numeración;
- navegación.

Identifica problemas que deban corregirse antes de la exportación.

==================================================
10. ENTREGABLE

NO MODIFIQUES ARCHIVOS TODAVÍA.

Genera únicamente un informe:

AUDITORIA_ESTRUCTURAL_EXPEDIENTE_MIGRATORIO.md

Debe contener:

# AUDITORÍA ESTRUCTURAL DEL EXPEDIENTE MAESTRO MIGRATORIO

## 1. Resultado general

## 2. Archivos auditados

## 3. Cumplimiento del Standard Migración

## 4. Cumplimiento de metadata

## 5. Cumplimiento de arquitectura documental

## 6. Problemas encontrados

## 7. Referencias rotas

## 8. Evidencia faltante

## 9. Documentos que deben crearse

## 10. Documentos que deben corregirse

## 11. Riesgos documentales

## 12. Recomendaciones

## 13. Gate de aprobación

El informe deberá finalizar con uno de estos estados:

PASS
PASS_WITH_FIXES
BLOCKED

No realices cambios adicionales hasta que el resultado de esta auditoría sea revisado y aprobado.
