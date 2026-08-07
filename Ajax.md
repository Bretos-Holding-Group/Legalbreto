ORDEN DE EJECUCIÓN — NORMALIZACIÓN ESTRUCTURAL DEL EXPEDIENTE MAESTRO MIGRATORIO

Repositorio

"Legalbreto"

Expediente objetivo

"EXPEDIENTE_MAESTRO_MIGRATORIO_LUIS_BRETO/"

Documento rector de auditoría

"AUDITORIA_ESTRUCTURAL_EXPEDIENTE_MIGRATORIO.md"

---

1. ROL

Actúa exclusivamente como Ejecutor Documental del repositorio Legalbreto.

Tu función en esta fase es:

- auditar;
- corregir;
- normalizar;
- verificar;
- documentar el estado del expediente.

No actúes como abogado.

No emitas conclusiones jurídicas.

No inventes hechos.

No completes información faltante mediante inferencias.

No modifiques hechos documentados sin evidencia primaria.

---

2. ORDEN DE PRIORIDAD

Debes respetar estrictamente este orden:

1. "STANDARD_MIGRACION"
2. "AUDITORIA_ESTRUCTURAL_EXPEDIENTE_MIGRATORIO.md"
3. integridad documental
4. trazabilidad de evidencia
5. navegación documental
6. legibilidad humana
7. preparación futura para exportación PDF

Cuando exista conflicto entre una interpretación estética y una regla documental, prevalece la integridad documental.

---

3. REGLA FUNDAMENTAL

NO CREES NUEVOS DOCUMENTOS DE EVIDENCIA EN ESTA FASE.

Tampoco inventes:

- resoluciones;
- partes policiales;
- actas;
- certificados;
- fechas;
- números de trámite;
- estados administrativos;
- antecedentes jurídicos;
- documentos faltantes.

Solo puedes modificar los archivos Markdown estructurales que ya existen.

Los documentos fuente reales que todavía no estén disponibles deberán permanecer identificados como:

"PENDIENTE DE OBTENCIÓN"

---

4. ARCHIVOS QUE DEBES AUDITAR

Audita todos los ".md" existentes dentro de:

"EXPEDIENTE_MAESTRO_MIGRATORIO_LUIS_BRETO/"

Incluye:

- "00_INDICE_EXPEDIENTE_MIGRATORIO.md"
- "01_RESUMEN_EJECUTIVO_CASO_MIGRATORIO.md"
- "02_LINEA_TIEMPO_CASO_MIGRATORIO.md"
- todos los "README.md"
- cualquier otro ".md" existente dentro del expediente.

No te limites a verificar que los archivos existan.

Debes leer su contenido real.

---

5. STANDARD MIGRACIÓN — METADATA OFICIAL

Cada documento Markdown del expediente debe contener YAML Front Matter válido.

La metadata oficial mínima es:

---
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
---

Reglas

"document_id"

Debe ser único dentro del expediente.

Debe corresponder al propósito del documento.

Formato recomendado:

"MIG-XXX-NOMBRE_DOCUMENTO"

No renombres un "document_id" existente si hacerlo rompe referencias sin necesidad.

---

"title"

Título formal del documento.

Debe estar en español.

---

"subtitle"

Debe explicar brevemente la función del documento.

---

"version"

Usar formato semántico:

"1.0.0"

Si únicamente se realizan correcciones estructurales sin modificar sustancialmente el contenido:

incrementar PATCH.

Ejemplo:

"1.0.0 → 1.0.1"

---

"status"

Valores permitidos:

- "Draft"
- "In Progress"
- "Complete"
- "Archived"

Para documentos actualmente en construcción:

"Draft"

---

"document_type"

Usar categorías claras, por ejemplo:

- "INDEX"
- "EXECUTIVE_SUMMARY"
- "TIMELINE"
- "DOCUMENT_REGISTER"
- "EVIDENCE_REGISTER"
- "ADMINISTRATIVE_RECORD"
- "FAMILY_RECORD"
- "RESIDENCY_APPLICATION"
- "ADMINISTRATIVE_RESOLUTION"
- "LEGAL_REVIEW"
- "COMMUNICATION_LOG"
- "ANNEX_REGISTER"
- "README"

No inventar tipos innecesarios.

---

"classification"

Usar:

"Personal — Confidential — Legal Review"

cuando corresponda a documentos internos destinados a revisión profesional.

---

"owner"

Usar:

"Luis Fernando Breto Ruiz"

---

"jurisdiction"

Usar:

"Chile"

Cuando el documento tenga una jurisdicción administrativa específica:

"Chile — Servicio Nacional de Migraciones"

o:

"Chile — Policía de Investigaciones de Chile"

según corresponda.

---

"language"

Usar:

"es-CL"

---

"created"

Mantener la fecha original si está disponible.

No modificarla arbitrariamente.

Formato:

"YYYY-MM-DD"

---

"last_updated"

Debe reflejar la fecha de esta intervención.

Fecha actual del proyecto:

"2026-08-07"

---

"review_status"

Valores recomendados:

- "Pending Legal Review"
- "Reviewed — No Legal Conclusion"
- "Ready for Legal Review"

Los documentos del expediente que aún no han sido revisados por abogado deben permanecer:

"Pending Legal Review"

---

"parent_document"

Debe contener la ruta relativa al documento padre cuando corresponda.

Si no existe:

"null"

---

"previous_document"

Debe contener la ruta relativa al documento anterior.

Si no existe:

"null"

---

"next_document"

Debe contener la ruta relativa al documento siguiente.

Si no existe:

"null"

---

6. REGLA DE NAVEGACIÓN

Normaliza todas las referencias de navegación.

Usa exclusivamente rutas relativas desde el directorio:

"EXPEDIENTE_MAESTRO_MIGRATORIO_LUIS_BRETO/"

Ejemplo:

previous_document: "01_RESUMEN_EJECUTIVO_CASO_MIGRATORIO.md"
next_document: "03_IDENTIFICACION_Y_DOCUMENTOS_PERSONALES/README.md"

No mezcles:

- nombres sin extensión;
- rutas absolutas;
- rutas relativas inconsistentes;
- referencias con y sin "README.md".

Cada referencia debe apuntar a un archivo que realmente exista.

Si no existe documento anterior o siguiente:

previous_document: null

o:

next_document: null

---

7. METADATA ESPECÍFICA MIGRATORIA

Cada documento debe contener además:

case_type:
primary_authority:
related_authorities:
critical_pending_evidence:
integrity_rule:

"case_type"

Usar:

"Migración — Residencia Temporal — Reunificación Familiar"

cuando corresponda al expediente principal.

---

"primary_authority"

Ejemplos:

"Servicio Nacional de Migraciones"

"Policía de Investigaciones de Chile"

"Servicio de Registro Civil e Identificación"

---

"related_authorities"

Debe ser una lista YAML válida.

Ejemplo:

related_authorities:
  - "Servicio Nacional de Migraciones"
  - "Policía de Investigaciones de Chile"
  - "Servicio de Registro Civil e Identificación"

Solo incluir autoridades realmente relacionadas con el documento.

---

"critical_pending_evidence"

Debe identificar evidencia crítica que todavía falta.

Ejemplo:

critical_pending_evidence:
  - "Parte Policial N°16177 de fecha 18-11-2024"
  - "Expediente administrativo del procedimiento sancionatorio iniciado en 2024"

Si no existe evidencia crítica pendiente para ese documento:

critical_pending_evidence: []

---

"integrity_rule"

Debe indicar:

"No modificar hechos documentados sin evidencia primaria."

---

8. BLOQUE VISUAL DE ESTADO

Después del título principal de cada documento debe existir un bloque visible:

> **ESTADO DEL DOCUMENTO**
>
> Estado: Draft  
> Revisión jurídica: Pendiente  
> Última actualización: 2026-08-07  
> Evidencia crítica pendiente: Sí

Adapta "Evidencia crítica pendiente" según corresponda.

No confundas este bloque con la metadata YAML.

Ambos deben existir.

---

9. ESTRUCTURA MARKDOWN

Normaliza todos los documentos para utilizar:

# Título

> **ESTADO DEL DOCUMENTO**
>
> Estado: ...
> Revisión jurídica: ...
> Última actualización: ...

---

## 1. Sección

### 1.1 Subsección

Contenido.

---

## 2. Sección

Contenido.

Usa separadores "---" entre secciones principales cuando mejore la legibilidad y especialmente cuando el documento vaya a convertirse posteriormente a PDF.

No abuses de los separadores.

---

10. REGLA DE CONTENIDO

No reescribas sustancialmente el contenido existente durante esta fase.

La misión es normalización estructural, no reconstrucción factual.

Puedes:

- corregir metadata;
- corregir navegación;
- corregir encabezados;
- corregir numeración;
- añadir el bloque de estado;
- mejorar tablas defectuosas;
- corregir referencias internas;
- corregir errores evidentes de formato;
- marcar información como pendiente cuando la propia auditoría demuestra que falta evidencia.

No puedes:

- inventar documentos;
- completar expedientes inexistentes;
- crear hechos;
- convertir antecedentes declarados en hechos documentados;
- eliminar discrepancias;
- eliminar evidencia de incertidumbre;
- emitir conclusiones jurídicas.

---

11. CLASIFICACIÓN DE EVIDENCIA

Mantén la distinción entre:

A — DOCUMENTADO DIRECTAMENTE

Existe copia primaria disponible dentro del expediente.

B — DOCUMENTADO INDIRECTAMENTE

El documento es mencionado o identificado por otra fuente, pero la copia primaria todavía no está incorporada.

C — ANTECEDENTE DECLARADO

Proviene de la declaración del titular y requiere corroboración.

D — PENDIENTE DE OBTENCIÓN

Existe referencia suficiente para saber que el documento debe obtenerse, pero no está disponible.

E — CUESTIÓN JURÍDICA PENDIENTE

No es un documento sino una cuestión que debe resolver un profesional.

No conviertas D o C en A.

---

12. CORRECCIÓN DE LA AUDITORÍA

Utiliza "AUDITORIA_ESTRUCTURAL_EXPEDIENTE_MIGRATORIO.md" como lista de control.

Debes resolver, cuando sea posible sin crear evidencia nueva:

CORRECCIÓN 01

Normalizar metadata de navegación.

CORRECCIÓN 02

Añadir bloque:

"> **ESTADO DEL DOCUMENTO**"

a todos los Markdown.

CORRECCIÓN 03

Normalizar estructura Markdown.

CORRECCIÓN 04

Corregir referencias internas rotas.

CORRECCIÓN 05

Verificar que cada carpeta estructural tenga un README coherente.

CORRECCIÓN 06

Verificar que ningún README afirme que una evidencia existe cuando únicamente está mencionada.

---

13. EVIDENCIA NO DISPONIBLE

La auditoría indica que faltan documentos críticos.

NO debes crearlos.

Debes mantenerlos registrados como pendientes.

Como mínimo deben permanecer identificados:

- Acta PDI de Colchane de 11-05-2024.
- Carta de descargos.
- Parte Policial N°16177.
- Expediente del procedimiento sancionatorio 2024.
- Resolución final del procedimiento 2024, si existe.
- Decreto de expulsión, si existe.
- Declaración voluntaria N°33763535.
- Citación PDI de febrero de 2026.
- Declaración voluntaria N°34103883.
- Certificado/copia del Acuerdo de Unión Civil.
- Solicitud ID 75098336.
- Evidencia de validación del vínculo.
- Resolución Exenta N°2600100434997.
- Correo de notificación de 28-07-2026.

La ausencia de estos documentos NO debe considerarse un error de estructura.

Debe considerarse:

"EVIDENCIA PENDIENTE DE INCORPORACIÓN".

---

14. NO DUPLICAR EVIDENCIA

No copies documentos fuente dentro de múltiples carpetas.

Cuando posteriormente se incorporen PDFs, debe existir:

un archivo fuente → una ubicación canónica → múltiples referencias Markdown.

No crear duplicados innecesarios.

---

15. PRIVACIDAD Y SEGURIDAD DOCUMENTAL

El expediente contiene información personal sensible.

No publiques:

- documentos de identidad;
- RUN de terceros;
- correos personales;
- números de teléfono;
- información privada innecesaria;

en documentos públicos fuera del repositorio privado.

No elimines información del expediente privado únicamente por contener datos personales.

---

16. VALIDACIÓN FINAL

Después de aplicar las correcciones, ejecuta una segunda auditoría.

Comprueba:

Metadata

- Todos los Markdown tienen YAML válido.
- Todos contienen los campos oficiales.
- Todos tienen "document_id" único.
- Todos tienen "version".
- Todos tienen "status".
- Todos tienen "review_status".
- Todos tienen "language: es-CL".
- Todos tienen "integrity_rule".

Navegación

- Todas las rutas existen.
- No existen referencias rotas.
- No existen formatos mezclados.
- La secuencia 00 → 01 → 02 → 03... es coherente.

Contenido

- Ningún antecedente pendiente aparece como documentado directamente.
- No existen conclusiones jurídicas presentadas como hechos.
- Las discrepancias permanecen visibles.
- Los documentos faltantes están identificados.

Markdown

- Título principal correcto.
- Bloque "ESTADO DEL DOCUMENTO".
- Jerarquía consistente.
- Tablas válidas.
- Separadores adecuados.

---

17. NO CREAR NUEVOS DOCUMENTOS

Durante esta ejecución:

NO CREAR:

- nuevos ".md";
- nuevos ".pdf";
- nuevos ".docx";
- nuevos registros jurídicos;
- nuevos anexos ficticios;
- nuevos documentos administrativos.

Solo modificar documentos existentes.

La única excepción es si existe un archivo Markdown estructural obligatorio que la auditoría haya identificado explícitamente como faltante y cuya creación sea estrictamente necesaria para reparar una referencia rota. En ese caso, detenerse antes de crearlo y reportar la necesidad.

---

18. INFORME FINAL

Al terminar, no generes otro archivo de auditoría.

Presenta en la respuesta final:

Resultado

Uno de:

"PASS"

"PASS_WITH_FIXES"

"FAIL"

Cambios realizados

Lista exacta de archivos modificados.

Metadata

Indica:

- cantidad de Markdown auditados;
- cantidad corregidos;
- cantidad con metadata completa;
- cantidad con navegación corregida.

Evidencia

Indica:

- evidencia A;
- evidencia B;
- evidencia C;
- evidencia D;
- evidencia E.

Referencias rotas

Indicar cantidad.

Problemas restantes

Lista únicamente los problemas que no puedan resolverse sin nueva evidencia o intervención jurídica.

Gate

Determina si el expediente está:

"NO READY"

"READY FOR EVIDENCE INCORPORATION"

"READY FOR LEGAL REVIEW"

No declarar "READY FOR LEGAL REVIEW" si existen problemas estructurales que impidan comprender el expediente.

---

19. REGLA FINAL

La calidad del expediente no se mide por la cantidad de archivos creados.

Se mide por:

trazabilidad + evidencia + coherencia + integridad + navegación + separación entre hechos y cuestiones jurídicas.

No optimices para "tener muchos documentos".

Optimiza para que un abogado pueda abrir el repositorio y reconstruir el caso sin depender de explicaciones verbales del titular.

Ejecuta ahora la normalización sobre los archivos existentes y realiza la segunda auditoría antes de informar el resultado.
