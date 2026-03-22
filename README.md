# IBKR → Renta 2025 🇪🇸

Analizador fiscal para la declaración de la renta española (ejercicio 2025) a partir de los CSV de **Interactive Brokers**.

🔗 **[Abrir la aplicación](https://TU_USUARIO.github.io/ibkr-renta)**

---

## ¿Qué hace?

- **Multi-cuenta**: sube los CSV de varias cuentas IBKR y consolida los resultados
- **Tipos de cambio oficiales**: descarga automáticamente los tipos diarios EUR/USD del Banco Central Europeo (BCE) y aplica el tipo exacto de cada operación por fecha
- **Casillas del Modelo 100**: calcula exactamente qué importe introducir en cada casilla de Renta WEB 2025
- **Tramos IRPF 2025**: incluye el nuevo tipo del 30% para base del ahorro >300.000€ (Ley 7/2024)
- **Compensación de pérdidas**: calcula la compensación cruzada entre RCM y G/P patrimoniales (art. 49 LIRPF, límite 25%)
- **Exportar CSV**: genera un resumen listo para llevar al asesor fiscal

## Casillas que calcula

| Casilla | Concepto |
|---------|----------|
| 0029 | Dividendos brutos |
| 0033 | Intereses cobrados |
| 0032 | Intereses de margen (gasto deducible) |
| 0327 | Valor de transmisión — acciones y opciones |
| 0328 | Valor de adquisición — acciones y opciones |
| 0358 | G/P en divisas |
| 0588 | Deducción por doble imposición internacional |

## Cómo exportar el CSV desde IBKR

1. Inicia sesión en Interactive Brokers
2. Ve a **Rendimientos → Extracto de Actividad**
3. Formato: **CSV**
4. Período: **Anual 2025**
5. Secciones: **Todo**
6. Generar y descargar

Compatible con IBKR en **español e inglés**. Cuentas en EUR y USD.

## Novedades fiscales 2025 incorporadas

- Nuevo tipo máximo del **30%** para base del ahorro superior a 300.000€ (Ley 7/2024, vigente desde 01/01/2025)
- Nueva casilla diferenciada para ETFs cotizados
- Compensación cruzada RCM ↔ G/P hasta el 25%

## Instalación / Uso local

No requiere instalación. Abre `index.html` directamente en cualquier navegador moderno.

```bash
git clone https://github.com/TU_USUARIO/ibkr-renta.git
cd ibkr-renta
open index.html   # macOS
# o simplemente arrastra el archivo al navegador
```

## Despliegue en GitHub Pages

1. Sube el repositorio a GitHub
2. Ve a **Settings → Pages**
3. Source: **Deploy from a branch**
4. Branch: `main` / carpeta: `/ (root)`
5. Guarda — en unos segundos tendrás la URL activa

## Aviso legal

Esta herramienta es **orientativa**. Los cálculos se basan en los datos del CSV de IBKR y en la normativa IRPF 2025 vigente a la fecha de publicación. No constituye asesoramiento fiscal. Consulta a un asesor para tu declaración definitiva.

Los tipos de cambio se obtienen del **Banco Central Europeo** (BCE) en tiempo real. Si no hay conexión, se usa un tipo medio estimado.

## Privacidad

Todo el procesamiento se realiza **en tu navegador**. Ningún dato se envía a ningún servidor (excepto la consulta de tipos de cambio al BCE, que no incluye datos personales).

---

Hecho con ☕ para simplificar la campaña de Renta 2025.
