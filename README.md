# ✈️ Análisis de Series de Tiempo: Airline Baggage Complaints

Proyecto final de la materia **Análisis de Series de Tiempo** (Grupo 6AV1, ESCOM-IPN).

Análisis y pronóstico mensual de las quejas por equipaje en aerolíneas (2004–2010) con modelos ARIMA y SARIMA.

**Equipo:** Huerta Rodríguez Sofía · Zhang Tan Rubi

## 📁 Contenido

| Archivo | Descripción |
|---|---|
| `ProyectoSeriesDeTiempoFinal (1).ipynb` | Notebook con el análisis completo (código, gráficas y resultados). |
| `ReporteProyectoFinalST.pdf` | Reporte final del proyecto. |
| `baggagecomplaints.csv` | Datos mensuales de quejas por equipaje por aerolínea. |

## 🔍 Metodología

1. **Análisis exploratorio:** serie completa 2004–2010, estadística descriptiva, descomposición en componentes, mapa de calor de correlación y gráficas ACF/PACF.
2. **Recorte de la serie (2007–2010):** el periodo 2004–2006 es más irregular, así que se modela el segmento más homogéneo.
3. **Estacionariedad:** estadísticas móviles y pruebas **ADF**, **KPSS** y **Ljung-Box**.
4. **Transformaciones:** logaritmo natural (estabiliza la varianza) y diferenciación de orden 1 (elimina la tendencia, d = 1), con nueva verificación de estacionariedad.
5. **Modelos ARIMA:** candidatos AR(1), MA(1) y ARMA(1,1) a partir de ACF/PACF; diagnóstico de residuos (Ljung-Box) y prueba **ARCH-LM** de heteroscedasticidad condicional.
6. **Modelos SARIMA:** identificación de órdenes estacionales, ajuste de candidatos y diagnóstico del mejor modelo.
7. **Pronóstico y validación:** pronóstico fuera de muestra de los últimos 6 meses, métricas de error y validación cruzada temporal, comparando SARIMA contra MA(1).

## 🛠️ Tecnologías

Python · pandas · NumPy · statsmodels · matplotlib · seaborn · Jupyter

## ▶️ Cómo ejecutarlo

```bash
git clone https://github.com/sofiarodriguezzz/ProyectoFinalSeriesDeTiempo.git
cd ProyectoFinalSeriesDeTiempo
```

Abre el notebook en Jupyter o Google Colab y ejecútalo en orden, con `baggagecomplaints.csv` en la misma carpeta.
