This is a report over the Cruise Customer Satisfaction Prediction using XGBoost.

Here, top two features will be covered in report.

In this report, following things are mentioned:
1. SHAP values over features
2. Dependence Plot

1. SHAP values over features:

For feature Gasto_Promedio_Diario_Huesped_USD: 
The thickness in positive and negative shows that this relation is very stable relation.

For feature Tipo_Ruta:
Mediterranean cruises have a more variable effect. Some are only slightly negative, while others are much more negative.
Non-Mediterranean cruises have a more consistent positive effect. Many bookings get a similar upward push.

2. Dependence Plot:
The SHAP dependence plot for Lead_Time_Dias does not show a strong monotonic relationship with customer satisfaction. For most bookings, the contribution of lead time remains close to zero. However, for very long booking lead times (approximately 180–200 days), the SHAP values exhibit greater variability, indicating that the influence of lead time depends on interactions with other booking characteristics rather than acting as an independent driver of satisfaction.