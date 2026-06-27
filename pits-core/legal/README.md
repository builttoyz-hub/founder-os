# /legal — Marco Legal

## Propósito

Los documentos legales que rigen la operación de PITS MARKET: contratos con proveedores y socios, términos de servicio para usuarios, políticas internas de operación y cumplimiento regulatorio.

> ⚠️ **Advertencia:** Los documentos en esta carpeta tienen efectos legales. Ningún documento debe modificarse sin revisión de un abogado colombiano especializado en derecho digital o tecnología. El Fundador tiene firma final en todos los documentos legales.

---

## Subcarpetas

### `/contracts` — Contratos con proveedores y socios
Acuerdos firmados con proveedores de servicios (Supabase, Vercel, Twilio), socios comerciales, influencers con contratos formales, y distribuidores.

### `/terms` — Términos de servicio y políticas de privacidad
Los documentos públicos que regulan la relación con los usuarios de la plataforma. Deben estar en línea con la Ley 1581 de 2012 (Protección de Datos Personales de Colombia) y las mejores prácticas internacionales.

### `/policies` — Políticas internas
Las políticas de operación interna: política de moderación de contenido, política de resolución de disputas, política de uso aceptable, política de reembolsos.

### `/compliance` — Cumplimiento regulatorio
Documentación de cumplimiento con regulaciones colombianas y potencialmente internacionales: Ley 1581, Ley de Comercio Electrónico, y normativas de la SIC (Superintendencia de Industria y Comercio).

---

## Documentos Requeridos Antes del Lanzamiento

| Documento | Carpeta | Estado | Obligatorio |
|-----------|---------|--------|-------------|
| Términos de Uso de la Plataforma | `terms/` | ⚪ Por crear | ✅ Sí |
| Política de Privacidad (Ley 1581) | `terms/` | ⚪ Por crear | ✅ Sí |
| Política de Cookies | `terms/` | ⚪ Por crear | ✅ Sí |
| Política de Moderación de Contenido | `policies/` | ⚪ Por crear | ✅ Sí |
| Política de Piezas Prohibidas | `policies/` | ⚪ Por crear | ✅ Sí |
| Política de Resolución de Disputas | `policies/` | ⚪ Por crear | ✅ Sí |

---

## Marco Legal Colombiano Aplicable

| Ley / Decreto | Descripción | Impacto en PITS MARKET |
|---------------|-------------|----------------------|
| Ley 1581 de 2012 | Protección de Datos Personales | Política de privacidad, manejo de datos de usuarios |
| Ley 527 de 1999 | Comercio Electrónico | Validez de contratos electrónicos entre usuarios |
| Código de Comercio | Contratos de compraventa | Las transacciones entre usuarios |
| Ley 1480 de 2011 | Estatuto del Consumidor | Derechos de compradores en la plataforma |
| Decreto SIC | Registro Nacional de Bases de Datos (RNBD) | Inscripción de la base de datos de usuarios |

---

## Convención de Nombres

```
[subcarpeta]/[tipo]-[descripcion]-v[N]-[fecha].md

Tipos por subcarpeta:
  contracts/  → contract-[proveedor/socio]-[fecha].md
  terms/      → terms-of-service-v[N].md | privacy-policy-v[N].md
  policies/   → policy-[nombre]-v[N].md
  compliance/ → compliance-[regulacion]-[fecha].md

Ejemplos:
  contracts/contract-revue-sas-influencer-2026-07.md
  terms/terms-of-service-v1-2026-07.md
  terms/privacy-policy-v1-2026-07.md
  policies/policy-content-moderation-v1.md
  policies/policy-prohibited-items-v1.md
  compliance/compliance-ley-1581-rnbd-2026.md
```

---

*Propietario: Fundador — Requiere revisión legal externa para cambios*
