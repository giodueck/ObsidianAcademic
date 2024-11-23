2024-11-19
---
# Tesis - Estado del arte - Tabla PI 3

3. ¿Qué soluciones existen para abordar la falta de datos de entrenamiento para las redes neuronales convolucionales?

## Proyectos relevantes
Safonova 2023
Maggiori 2016-0
Castelluccio 2015
Nogueira 2017
Zhong 2016
Amato 2023

## Tabla

Tecnica | Descripcion | Ventajas | Desventajas | Fuente
--------|-------------|----------|-------------|-------
Transferencia (Transfer, Fine-tuning) | Uso de modelo preentrenado con un conjunto de datos relevante y ajustado con un conjunto de datos nuevo | Mejor rendimiento, menos datos de entrenamiento, mejor generalizabilidad | Riesgo de reduccion de rendimiento con transferencia a dominio diferente, tamaño de modelo grande | Sofanova, Maggiori, Castelluccio, Nogueira, Zhong, Amato
Auto supervisado (Self-supervised) | Creacion de un modelo con etiquetas creadas por el modelo, seguido de entrenamiento supervisado con etiquetas proveidas | Uso de datos no etiquetados, reconocimiento de patrones sin necesidad de etiquetacion, mejor generalizabilidad | Computacionalmente caro, posibilidad de que el modelo deje de entrenarse con algunas tecnicas | Sofanova
Semi supervisado (Semi-supervised) | Mezcla de entrenamiento supervisado y no supervisado con conjuntos de datos etiquetados y no etiquetados | Uso de datos etiquetados y no etiquetados, mejor generalizabilidad | Computacionalmente caro, riesgo de "overfitting", sensible a calidad de datos | Sofanova
Few-shot | Entrenar modelos con unos pocos ejemplos etiquetados por clase a generalizar para nuevos problemas | Enfocado al problema de pocos datos, adaptacion rapida del modelo, mejor generalizabilidad | Complejidad limitada, riesgo de "overfitting", sensible a calidad de datos | Sofanova
Zero-shot | Modelo Few-shot entrenado para reconocer clases que nunca ha visto antes | Adaptable a clases que no conoce, transferibilidad mejorada | Extremamente sensible a calidad de datos de nuevas instancias | Sofanova
Debilmente supervisado (Weakly-supervised) | Desarrollo de un modelo con datos etiquetados parcialmente, imprecisamente o con ruido | Costo de etiquetamiento reducido, permite un modelo inexacto para permitir escalabilidad | Computacionalmente caro, menos exacto que entrenamiento (completamente) supervisado | Sofanova
Multi-task | Entrenamiento de modelo para reconocer patrones generales utiles para varias tareas | Eficiencia de entrenamiento para varias tareas, mejor generalization, requerimiento reducido de datos | Complejidad de modelamiento, interferencia de tareas, escalabilidad limitada | Sofanova
Conjunto (Ensemble) | Combinacion de muchos modelos individuales que aprendieron patrones de forma diferente, para prediccion | Mejor generalizabilidad, robustez contra perturbacion de datos e incertidumbre | Computacionalente caro, pero interpretabilidad que un modelo simple | Sofanova
Consciente del proceso (Process-aware) | Incorporacion de regulacion del entrenamiento por medio de procesos | Aprendizaje mecanico, mejor transferibilidad | Riesgo de perdida de rendimiento si se depende de una suposicion equivocada | Sofanova
Validacion cruzada (Cross-validation) | Entrenar y validar un modelo varias veces usando diferentes particiones de datos para el entrenamiento y la validacion | Modelo menos sesgado, evita reportaje sobreoptimista de rendimiento, mejor generalizabilidad | Computacionalmente caro | Sofanova
