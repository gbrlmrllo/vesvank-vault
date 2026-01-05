# Competencia Venezuela

Análisis de competidores en el mercado venezolano de pagos.

---

## Modelo de Negocio de Vesvank

Vesvank sigue el **modelo Stripe**: infraestructura de pagos B2B para comercios.

| Característica | Stripe | Vesvank |
|----------------|--------|---------|
| Cliente | El comercio/negocio | El comercio/negocio |
| Producto | APIs + Dashboard | APIs + Dashboard |
| Propuesta | "Acepta pagos fácilmente" | "Acepta pagos fácilmente" |
| Métodos | Tarjetas, wallets, etc. | **C2P**, Binance Pay |
| Extras | Billing, invoicing, customers | Clientes, catálogo, facturación |
| Modelo | % del TPV | % del TPV |

### Nota: C2P vs Pago Móvil P2P

| Tipo                         | Flujo                                         | Control                |
| ---------------------------- | --------------------------------------------- | ---------------------- |
| **Pago Móvil P2P**           | Cliente envía → Comercio verifica manualmente | Cliente tiene control  |
| **C2P (Comercio a Persona)** | Comercio inicia cobro → Cliente autoriza      | Comercio tiene control |

Vesvank usa **C2P** - el comercio inicia la transacción. Es como un punto de venta digital, no depende de que el cliente "envíe bien" y mande capturas.

**Pregunta clave:** ¿Quién en Venezuela ofrece infraestructura de pagos B2B estilo Stripe?

---

## Hallazgo Principal

**No existe un "Stripe venezolano" establecido.**

El mercado está fragmentado en:
1. **Billeteras cripto** (B2C) - El usuario tiene la app, no el comercio
2. **Pasarelas bancarias** - APIs limitadas, requieren cuenta jurídica, solo bolívares
3. **Plugins e-commerce** - Solo WooCommerce/PrestaShop, sin plataforma propia

Esto representa una **oportunidad de categoría** para Vesvank.

---

## Competidores por Tipo

### Tipo 1: Infraestructura de Pagos (Modelo Stripe)

#### ekiipago - El más cercano

| Aspecto | Detalle |
|---------|---------|
| Modelo | B2B, infraestructura para comercios |
| Producto | Botón de pago, link de pago, API REST |
| Métodos | Solo pago móvil (bolívares) |
| Target | Comercios, tiendas online |
| Web | ekiipago.com |

**Funcionalidades:**
- Verificación automática (sin capturas)
- Dashboard de conciliación
- Integración vía API

**Limitaciones:**
- No soporta cripto/USDT
- No tiene catálogo de productos
- No tiene gestión de clientes robusta
- Documentación de API no pública

**Conclusión:** Competidor más directo, pero incompleto. Solo resuelve pago móvil.

---

#### Venflow - Competidor directo en recurring payments

| Aspecto | Detalle |
|---------|---------|
| Modelo | B2B, infraestructura de billing |
| Producto | Automatización de suscripciones y cobros recurrentes |
| Métodos | Domiciliación bancaria (solo Banco Activo, Plaza próximamente) |
| Target | SaaS, BNPL, seguros, telecoms, lending |
| Etapa | **Lista de espera** - muy temprano |
| Web | venflow.app |
| Founder | Nicolás Passaro |

**Funcionalidades:**
- Gestión de planes recurrentes
- Autorización digital de domiciliación (sin papel)
- Portal de autoservicio para clientes
- Reintentos automáticos de cobro
- API para integración

**¿Es competencia de Vesvank?**

**Sí.** Vesvank tiene recurring payments en el roadmap, lo que los pone en competencia directa.

| Aspecto | Venflow | Vesvank (futuro) |
|---------|---------|------------------|
| Recurring payments | ✅ Ya enfocado | 🔜 En roadmap |
| Métodos | Solo domiciliación bancaria | C2P + Binance Pay |
| Pagos únicos | ❌ | ✅ |
| Gestión comercial | ❌ | ✅ |

**Ventaja Venflow:** Enfocados 100% en suscripciones, más especializados.

**Ventaja Vesvank:** Plataforma completa (pagos únicos + recurrentes + gestión). Más métodos de pago (C2P, cripto).

**Estado actual:** Venflow en lista de espera, muy temprano. Oportunidad de adelantarse.

**Nota:** Ganaron BanescoInnova 2025. Competidor a monitorear de cerca.

---

### Tipo 2: Billeteras Cripto (NO son modelo Stripe)

Estas empresas parecen competencia pero **no lo son**. Su cliente es el usuario final, no el comercio.

#### Crixto

| Aspecto | Detalle |
|---------|---------|
| Modelo | **B2C** - El usuario descarga CrixtoPay |
| Producto | Billetera cripto con pagos en comercios |
| Cómo funciona | Usuario escanea QR → Crixto convierte → Comercio recibe bolívares |
| Alianza | Master Aggregator de Binance Pay |

**Por qué NO es competencia directa:**
- El comercio no tiene dashboard ni herramientas
- No hay gestión de clientes, catálogo, facturación
- Crixto controla la relación con el usuario final
- El comercio solo "recibe" dinero, no gestiona pagos

**Es más comparable a:** Una red de puntos de venta (como Visa) que una plataforma para comercios (como Stripe).

#### Ibis

| Aspecto | Detalle |
|---------|---------|
| Modelo | **B2C** - Billetera personal |
| Producto | USDT wallet + tarjeta Mastercard |
| Target | Freelancers, remesas, ahorro |

**Por qué NO es competencia:** No ofrece nada para comercios.

#### Kontigo

| Aspecto | Detalle |
|---------|---------|
| Modelo | **B2C** - Super app |
| Producto | Pagos, cambios, ahorro |
| Alianza | 40,000 comercios vía Dis Global |

**Por qué NO es competencia:** Similar a Crixto - el usuario tiene la app, no el comercio.

---

### Tipo 3: Pasarelas y Soluciones Tradicionales

#### InstaPago - Pasarela con API (solo tarjetas)

| Aspecto | Detalle |
|---------|---------|
| Modelo | Pasarela de pagos B2B |
| Producto | API de pagos + plugins e-commerce |
| Métodos | Solo tarjetas crédito (Visa, MC) vía Banesco |
| Target | Comercios online, personas naturales y jurídicas |
| API | Sí, documentada públicamente |
| Plugins | WooCommerce, Shopify |
| Web | instapago.com |

**Fortalezas:**
- API real y documentada
- Compatible con múltiples lenguajes (PHP, Java, .NET, Ruby)
- Plugins listos para e-commerce
- Acepta personas naturales (no solo jurídicas)

**Limitaciones:**
- Solo tarjetas de crédito (no pago móvil, no cripto)
- Dependiente de alianza con Banesco
- Requiere certificado SSL
- No tiene gestión comercial (clientes, catálogo)

**¿Es competencia de Vesvank?** Parcialmente. Tiene API como Vesvank, pero solo resuelve tarjetas de crédito. No compite en pago móvil ni cripto.

---

#### Ubii Pagos - Híbrido hardware + billetera

| Aspecto | Detalle |
|---------|---------|
| Modelo | Soluciones de pago (hardware + software) |
| Productos | Puntos de venta físicos, C2P app, Ubii App (billetera) |
| Métodos | Tarjetas (POS), pago móvil C2P |
| Target | Comercios físicos principalmente |
| API pública | No encontrada |
| Web | ubiipagos.com |

**Productos:**
- **POS físicos**: Terminales inalámbricos con liquidación a bancos
- **C2P**: App para que comercios cobren pago móvil (como POS virtual)
- **Ubii App**: Billetera B2C para usuarios finales (remesas, pagos)

**¿Es competencia de Vesvank?** No directamente. Es más proveedor de hardware/terminales + billetera B2C. No ofrece infraestructura API para desarrolladores.

---

#### Otras Pasarelas Bancarias

APIs de bancos venezolanos. Técnicamente "infraestructura", pero con muchas fricciones.

| Banco | Métodos | API | Requisitos |
|-------|---------|-----|------------|
| Mercantil | TDC, TDD, C2P | Sí | Cuenta jurídica, trámites |
| BDV | TDD, Pago Móvil | Sí | Cuenta jurídica, trámites |
| BVC | TDC, TDD, C2P | Sí | Cuenta jurídica, trámites |

**Otros intermediarios:**
| Pasarela | Métodos | Requisitos |
|----------|---------|------------|
| Credicard | TDC, pago móvil | Cuenta jurídica |
| Megasoft | C2P | Cuenta jurídica cualquier banco |

**Por qué NO son competencia real:**
- Solo bolívares
- Requieren cuenta jurídica (excluye freelancers, pequeños negocios)
- Sin gestión comercial (clientes, catálogo, facturación)
- Integración compleja
- Sin cripto

---

### Tipo 4: Plugins E-commerce

#### Cujiware / Yipi.app

| Aspecto | Detalle |
|---------|---------|
| Producto | Plugins WooCommerce/PrestaShop |
| Integraciones | BDV, Mercantil, BNC, BVC |
| Modelo | Membresía mensual |

**Por qué NO son competencia:**
- Solo funcionan en WordPress/PrestaShop
- El comercio debe gestionar su propia relación con el banco
- No es plataforma, es plugin
- Sin cripto

---

## Matriz: ¿Quién compite realmente con Vesvank?

| Criterio | Vesvank | ekiipago | InstaPago | Ubii Pagos | Crixto |
|----------|---------|----------|-----------|------------|--------|
| **Modelo B2B** | ✅ | ✅ | ✅ | Parcial | ❌ |
| **API para integrar** | ✅ | ✅ | ✅ | ❌ | ❌ |
| **Dashboard comercio** | ✅ | ✅ | Básico | ✅ | ❌ |
| **C2P** | ✅ | ✅ | ❌ | ✅ | ❌ |
| **Tarjetas crédito** | ❌ | ❌ | ✅ | ✅ | ❌ |
| **Cripto/USDT** | ✅ | ❌ | ❌ | ❌ | ✅* |
| **Links de pago** | ✅ | ✅ | ❌ | ❌ | ❌ |
| **Gestión clientes** | ✅ | Parcial | ❌ | ❌ | ❌ |
| **Catálogo productos** | ✅ | ❌ | ❌ | ❌ | ❌ |
| **Sin cuenta jurídica** | ✅ | ❓ | ✅ | ❓ | ✅ |

*Crixto procesa cripto pero el comercio no tiene control - solo recibe bolívares.

**Competidores más cercanos:**
1. **ekiipago** - C2P + links, pero sin cripto ni gestión comercial
2. **Venflow** - Recurring payments, pero solo domiciliación y sin pagos únicos
3. **InstaPago** - API real, pero solo tarjetas de crédito (no C2P)

---

## Posicionamiento Estratégico

### Vesvank vs. ekiipago

| Vesvank gana en | ekiipago gana en |
|-----------------|------------------|
| Cripto/USDT (Binance Pay) | ¿Más tiempo en mercado? |
| Gestión de clientes | ¿Más integraciones bancarias? |
| Catálogo de productos | |
| Facturación digital | |

**Estrategia:** Vesvank es "ekiipago + cripto + gestión comercial"

### Vesvank vs. Crixto

No compiten directamente. Diferentes modelos:
- Crixto: Red de aceptación cripto (como Visa)
- Vesvank: Plataforma para comercios (como Stripe)

**Oportunidad:** Vesvank podría integrar la red de Crixto como método de pago, igual que Stripe integra Apple Pay.

### Vesvank vs. Pasarelas tradicionales

| Vesvank gana en | Pasarelas ganan en |
|-----------------|-------------------|
| Facilidad de integración | Relación bancaria directa |
| Sin cuenta jurídica | Más métodos fiat |
| Cripto | |
| Herramientas comerciales | |

---

## Oportunidad de Mercado

1. **Categoría vacía:** No hay "Stripe venezolano" establecido
2. **Fragmentación:** Comercios usan 3-4 herramientas diferentes para cobrar
3. **Dolor real:** Verificar pagos móviles manualmente con capturas de pantalla
4. **Cripto sin gestión:** Crixto trae usuarios pero no herramientas para comercios
5. **Excluidos:** Freelancers y pequeños negocios sin cuenta jurídica no pueden usar pasarelas tradicionales

---

## Amenazas

1. **Crixto escala:** Si llegan a 100k puntos de venta y luego agregan dashboard para comercios
2. **ekiipago agrega cripto:** Cerraría la brecha con Vesvank
3. **Bancos mejoran:** C2P y NFC cada vez más accesibles
4. **Binance directo:** Si Binance lanza herramientas B2B para Venezuela

---

## Pricing de Referencia

| Competidor | Modelo | Notas |
|------------|--------|-------|
| Credicard | 1.45% - 10.5% | Variable por volumen |
| Crixto | ~7% spread | Implícito en tasa de conversión |
| ekiipago | No publicado | |
| Vesvank | 1.5% TPV | Ver [[Monetización]] |

---

## Resumen Ejecutivo

**Competencia directa:**
- **ekiipago** - incompleto (no cripto, no gestión comercial)
- **Venflow** - recurring payments (pero muy temprano, solo domiciliación)

**Competencia indirecta:**
- Billeteras cripto (Crixto, Ibis) - diferente modelo
- Pasarelas bancarias - diferente target (solo jurídicos)
- Plugins - diferente producto (no plataforma)

**Posición de Vesvank:** Único en combinar:
- Infraestructura B2B (modelo Stripe)
- C2P + Cripto (Binance Pay)
- Gestión comercial (clientes, catálogo, facturación)

---

## Links

- [[Monetización]] - Modelo de pricing de Vesvank
