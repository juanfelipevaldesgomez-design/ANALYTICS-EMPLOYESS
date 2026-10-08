# ANALYTICS-EMPLOYESS
HR Data Cleaning & Analysis — Conclusiones y Checklist
8 oct 2026 · @Identificar como es la composición patrimonial de la empresa, si es por acciones
Cierre del proyecto de limpieza y análisis del dataset de empleados (Employees_raw_Data.csv), enfocado en apoyar decisiones de RRHH sobre retención y compensación.

Resultados
• 16 empleados (5.3%) combinan bajo desempeño y salario bajo frente a su departamento — lista entregada a RRHH.
• HR (66.7%) y Finance (61.7%) son los departamentos con más riesgo proporcional; Sales el que menos (51.8%).
• Nadie en el dataset tiene menos de 1 año de antigüedad, probable limitación de la muestra.
• El trabajo remoto muestra desempeño algo mejor (3.79 vs 3.49 presencial), diferencia moderada.
• 16 empleados (5.3% de la plantilla) combinan bajo desempeño y salario por debajo de su departamento — lista nominal entregada para revisión de RRHH.
• HR (66.7%) y Finance (61.7%) tienen la mayor proporción de empleados con al menos una señal de riesgo, por encima del promedio de la empresa; Sales es el más bajo (51.8%).
• No se detectaron empleados con menos de 1 año de antigüedad en todo el dataset — posible limitación de la muestra, no un hallazgo de negocio.
• Los empleados en modalidad remota muestran un desempeño promedio ligeramente superior (3.79) frente a presenciales (3.49) y no especificados (3.46) — diferencia real pero moderada.


Conclusiones
Lo que más me quedó fue el criterio para tratar nulos: un dato numérico se puede promediar, uno categórico no, así que rellené department y remote_work con "Unknown" en vez de inventar un valor. Es lo primero que contaría en una entrevista.
Con más tiempo, el paso lógico sería dejar las reglas fijas de riesgo y entrenar un modelo con datos reales de quién renunció — algo que este dataset no tiene.
Lo que más reforcé en este proyecto fue la limpieza de datos con criterio real de negocio, no solo mecánica: entender que un valor faltante numérico (salario) y uno categórico (departamento) requieren estrategias completamente distintas — no se puede "promediar" una categoría, así que decidí rellenar con "Unknown" en vez de inventar un dato que no tenía evidencia de ser correcto. Esa es la decisión que mencionaría primero en una entrevista: muestra que entiendo la diferencia entre completar datos y inventarlos.
Con más tiempo o recursos, el siguiente paso lógico sería dejar de inferir riesgo con reglas fijas (3 señales combinadas) y construir un modelo predictivo real de probabilidad de rotación, entrenado con datos históricos de quién efectivamente dejó la empresa — algo que este dataset no incluye, y que sería la limitación más importante a resolver antes de llevar este análisis a producción.