# Monetización

## Contexto

- Vesvank es una plataforma orquestadora de pagos (SaaS)
- No tomamos margen de los fees de los bancos/procesadores
- Milestone para adquisición: $1M TPV en 18 meses
- Necesitamos un modelo que sea fácil de vender con equipo pequeño

---

## Modelo Actual (SaaS puro)

| Plan | Precio | Pagos/mes |
|------|--------|-----------|
| Free | $0 | 30 |
| Básico | $20 | 200 |
| Pro | $99 | 2,000 |
| Enterprise | Custom | 2,000+ |

**Problema:** Pricing basado en # de pagos, pero milestone es TPV. Desalineación de incentivos.

---

## Modelos Evaluados

### 1. SaaS Puro (actual)

| Pros | Contras |
|------|---------|
| Revenue predecible | Fricción alta para vender |
| Fácil de contabilizar | No alinea con milestone TPV |
| | Cliente no sabe cuántos pagos tendrá |

### 2. % del TPV Puro

| Pros | Contras |
|------|---------|
| Fácil de vender ("solo pagas si vendes") | Revenue impredecible |
| Alineado con milestone | Vulnerable a estacionalidad |
| Escala con el cliente | |

### 3. Híbrido (SaaS + % TPV)

| Pros | Contras |
|------|---------|
| Revenue base + upside | Pricing complejo |
| Flexibilidad | Difícil de explicar |

---

## Modelo Definido: Freemium + % TPV

### Estructura Base

| Tier | Costo | Límite |
|------|-------|--------|
| Free | $0 | Hasta $500 TPV/mes |
| Growth | 1.5% del TPV | Sin límite |

### Descuentos por Volumen

| TPV mensual | % | Nota |
|-------------|---|------|
| < $50,000 | 1.5% | Tarifa estándar |
| $50,000 - $200,000 | 1.0% | Descuento volumen |
| > $200,000 | 0.75%+ | Negociable |

**Estrategia:** No ofrecer descuento de entrada. Que el cliente lo pida cuando llegue al volumen. Así:
1. Probamos que el producto vale 1.5%
2. Tenemos leverage de negociación
3. El cliente siente que "ganó" algo

### Por qué este modelo

1. **Cero fricción** - "Pruébalo gratis, solo pagas 1.5% de lo que proceses"
2. **Alineado con milestone** - Más TPV = más revenue = más cerca de $1M
3. **Fácil de explicar** - Una frase, no tiers complejos
4. **Escala automático** - Sin conversaciones de upgrade
5. **Fit Venezuela** - Negocios pequeños empiezan gratis
6. **Incentivo a crecer** - Más volumen = mejor tarifa

### Pitch de ventas

> "Usa Vesvank gratis hasta $500 al mes. Después, solo pagas 1.5% de lo que proceses. Sin mensualidades, sin sorpresas."

### Ejemplos

| Cliente | TPV/mes | % | Pago mensual |
|---------|---------|---|--------------|
| Pequeño | $2,000 | 1.5% | $30 |
| Mediano | $20,000 | 1.5% | $300 |
| Grande | $80,000 | 1.0% | $800 |
| Enterprise | $300,000 | 0.75% | $2,250 |

---

## Proyección de Revenue

Asumiendo crecimiento hacia $1M TPV en mes 18:

| Mes | TPV mensual | TPV acumulado | Revenue (1.5%) | Revenue acumulado |
|-----|-------------|---------------|----------------|-------------------|
| 3 | $1,000 | $2,000 | $15 | $25 |
| 6 | $5,000 | $15,000 | $75 | $175 |
| 9 | $15,000 | $55,000 | $225 | $625 |
| 12 | $30,000 | $150,000 | $450 | $1,525 |
| 15 | $80,000 | $400,000 | $1,200 | $4,325 |
| 18 | $150,000 | $1,000,000 | $2,250 | $10,000 |

**Revenue total al mes 18:** ~$10,000-15,000

No cubre costos operativos, pero demuestra:
- Producto funciona
- Clientes pagan
- Tracción real

---

## Alternativa: Híbrido Light

Si queremos más revenue base:

| Tier | Costo |
|------|-------|
| Starter | $10/mes + 1% TPV |
| Pro | $50/mes + 0.5% TPV |

**Ejemplo Starter con $10k TPV/mes:** $10 + $100 = $110/mes

---

## Consideraciones Adicionales

### Fee mínimo por transacción
- Transacciones muy pequeñas (<$5) podrían no ser rentables
- Considerar: mínimo $0.10 por transacción o solo aplicar % a TPV > $500

### Competencia
- Investigar qué cobran otros orquestadores en LATAM
- Stripe Connect, PayU, etc.

---

## Decisiones

- [x] Modelo final: Freemium + % TPV
- [x] % estándar: 1.5%
- [x] Límite free tier: $500 TPV/mes
- [x] Descuentos volumen: 1% (>$50k), 0.75%+ (>$200k)
- [ ] Validar con potenciales clientes
- [ ] Actualizar página /precios en vesvank.com

---

## Links

- [[Runway & Financials]] - Proyección de costos
