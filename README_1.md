# 📦 Comercial y Logística — Dashboard de Ventas (Superstore)

Dashboard interactivo de 3 páginas construido en Looker Studio sobre el dataset "Superstore" (9,994 líneas de pedido, 5,009 órdenes, 793 clientes, 49 estados de EE. UU., 2014-2017). Cubre reporte de órdenes, reporte financiero y reporte de clientes, con filtros globales por región, segmento, categoría, modo de envío y año.

🔗 **[Ver el dashboard en vivo](https://datastudio.google.com/reporting/d4d3027c-b50d-40ec-bb5f-98a08c1f3ea3/page/LIE4F)**

*Parte de mi [Data Analytics Portfolio](https://github.com/eleazarsoto/data-analytics-portfolio) · Crédito: [Oráculo Analytics](https://oraculoanalytics.com)*

---

## 📋 Resumen del proyecto

- **Fuente:** dataset Superstore, tabla conectada a Looker Studio (copia en `data/Comercial_y_Logística.xlsx`)
- **Volumen:** 5,009 órdenes (9,994 líneas de pedido), 793 clientes, 49 estados, 3 segmentos, periodo 2014-2017
- **Ventas totales:** $2,441,157.91
- **Filtros globales:** región, segmento, categoría, modo de envío, y año — aplicados a las 3 páginas

## 🛠️ Estructura del dashboard

**Página 1 — Orders Report.** Panel de control principal: 5 tarjetas de KPI (Order ID, Cantidad de Clientes, Cantidad de Estados, Cantidad de Segmentos, Sales), 3 gráficos circulares (órdenes por región/categoría/segmento), tendencia de ventas por año (línea) y por mes (barras), y un mapa coroplético de EE. UU. por ventas.

**Página 2 — Financial Report.** Tres gráficos de barras apiladas por año, comparando ventas por segmento, por categoría y por modo de envío — permite ver no solo el crecimiento total, sino qué está impulsando ese crecimiento año con año.

**Página 3 — Customer Report.** Mismo patrón que el financiero, pero contando clientes únicos en vez de ventas: clientes por segmento, por categoría y por modo de envío, más un desglose mensual de clientes para el año más reciente (2017).

## 💡 Hallazgos

1. **Las ventas casi se duplicaron entre 2014 y 2017** (de $498,540 a $772,305, +55%), con crecimiento sostenido cada año — no hay ningún año de caída.
2. **West es la región con más órdenes** (1,611), seguida de East (1,401); South es la más chica (822) — casi la mitad que West.
3. **Office Supplies concentra la mayor cantidad de órdenes** (3,742, el 51% del total) pero eso no se traduce directo en ventas: para 2017, Technology ($271,731) superó a Office Supplies ($247,096) en ingreso — pedidos frecuentes de bajo ticket vs. pedidos menos frecuentes de mayor valor.
4. **Consumer es, por mucho, el segmento dominante** tanto en órdenes (2,586, 52%) como en clientes (361 en 2017) y en ventas ($352,756 en 2017 — más que Corporate y Home Office juntos).
5. **Standard Class domina el modo de envío** en ventas todos los años ($427,804 en 2017, el 55% del total de ese año), muy por encima de Second Class, First Class y Same Day combinados.
6. **La base de clientes también crece cada año**, no solo las ventas: Consumer pasó de 311 clientes en 2014 a 361 en 2017 — el crecimiento en ingresos viene acompañado de una base de clientes que también se expande, no solo de que los mismos clientes compren más.

## 📊 Vistas del dashboard

| Página | Captura | Contenido |
|---|---|---|
| 1 — Orders Report | `screenshots/pagina1_orders_report.png` | KPIs, circulares por región/categoría/segmento, tendencia anual y mensual, mapa por estado |
| 2 — Financial Report | `screenshots/pagina2_financial_report.png` | Ventas por segmento/categoría/modo de envío, por año |
| 3 — Customer Report | `screenshots/pagina3_customer_report.png` | Clientes por segmento/categoría/modo de envío, por año, y desglose mensual 2017 |

> Capturas tomadas directamente del dashboard en Looker Studio — no son reproducciones.

## 🗂️ Estructura del repositorio

```
comercial-logistica-dashboard/
├── data/
│   └── Comercial_y_Logística.xlsx   # datos fuente (Superstore)
├── screenshots/                      # 3 capturas reales del dashboard
└── README.md
```
