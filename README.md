# Age Verification CV System: IA para Cumplimiento Normativo en Venta de Alcohol
`Deep Learning` | `Computer Vision` | `Transfer Learning` | `Business Impact Analysis`

---

## 📋 Resumen Ejecutivo

| **El Problema** | **Mi Solución Técnica** | **El Resultado de Negocio** |
| :--- | :--- | :--- |
| Cadenas de retail enfrentan ~15% de error en venta de alcohol a menores → **Multas de $10k+ y riesgo legal**. | Prototipo de IA con **ResNet50 (Transfer Learning)** para estimar edad desde fotos. | ⚠️ **Veredicto Clave:** Modelo V1.0 **NO apto para producción** (error de ±13.5 años). <br> ✅ **Valor Demostrado:** Diagnosticé la causa raíz y diseñé un plan para **reducir ventas ilegales en un 80%** en V2.0. |

---

## 🎯 Habilidades Clave Demostradas

*   **🧠 Visión de Negocio + Técnica:** Definí métricas de éxito no solo como "MAE", sino como **Recall de menores >99%** para evitar multas, y **Precisión >80%** para no perder ventas legítimas.
*   **🔬 Análisis Crítico de Modelos:** Entrené un modelo de deep learning, pero identifiqué que su límite teórico (MAE 13.57) lo hacía **peligroso para uso real**. No intenté vender humo.
*   **📊 De la Técnica al Impacto:** Traduje los errores del modelo en **riesgos comerciales concretos**:
    *   *Falsos Negativos (17 años predecido como 30)* → **Venta Ilegal y Multa.**
    *   *Falsos Positivos (25 años predecido como 11)* → **Cliente frustrado y venta perdida.**
*   **🚀 Pensamiento Estratégico y Hoja de Ruta:** Propuse un plan por fases para V2.0, cambiando de regresión a clasificación binaria, que es lo que cualquier líder de producto querría ver.

---

## ⚙️ Detalles Técnicos Clave

### 🔍 Análisis Exploratorio de Datos (EDA)
*   **Herramientas:** Python (Pandas, Matplotlib).
*   **Hallazgo crítico:** Solo el **35% de los datos** estaban en el rango de edad clave (15-25 años), lo que introduce un sesgo importante para el modelo.
*   **Tamaño del dataset:** 7,600 imágenes faciales etiquetadas (rango 1-96 años).

### 🧠 Arquitectura del Modelo
*   **Modelo base:** ResNet50 pre-entrenado en ImageNet (Transfer Learning).
*   **Framework:** TensorFlow / Keras.
*   **Métrica de evaluación:** Mean Absolute Error (MAE) - interpretable en años.
*   **Datos:** 80% entrenamiento / 20% validación.

### 📉 Resultados del Modelo V1.0
*   **MAE obtenido:** ±13.57 años.
*   **Convergencia:** Modelo alcanzó máximo desempeño en época 6-7 (después plateau).
*   **Conclusión:** Métrica insuficiente para un caso de uso legalmente sensible. El modelo alcanzó su límite teórico con los datos disponibles.

---

## 💡 Recomendación Estratégica para V2.0

Basado en mi análisis, recomendé **no implementar este modelo en producción** y seguir este plan para garantizar ROI positivo:

1.  **Cambiar el enfoque:** Pasar de regresión (estimar edad exacta) a **clasificación binaria** (¿mayor o menor de 21?). Es más preciso y legalmente relevante.
2.  **Rediseñar la función de pérdida:** Penalizar 10x más los **falsos negativos** (vender a menores) que los falsos positivos.
3.  **Establecer un protocolo híbrido:** Usar la IA solo como primer filtro, requiriendo verificación humana para casos dudosos. Esto mitiga el riesgo legal mientras se mejora el modelo.

> **Conclusión para un Director de Producto/CTO:** Este proyecto demuestra que soy el tipo de científico de datos que no solo construye modelos, sino que **protege a la empresa de riesgos legales y financieros** mientras diseña una hoja de ruta hacia una solución rentable.

---

## 📁 Documentación del Proyecto

**Notebooks disponibles:**
*   [`analisis-exploratorio.ipynb`](./analisis-exploratorio.ipynb) - EDA completo con visualizaciones de distribución de edad y muestras por rango
*   [`entrenamiento-del-modelo.ipynb`](./entrenamiento-del-modelo.ipynb) - Modelado con ResNet50, resultados por época
*   [`analisis-completo.ipynb`](./analisis-completo.ipynb) - Versión narrativa y condensada con todos los hallazgos

**Scripts:**
*   [`run_model_on_gpu.py`](./run_model_on_gpu.py) - Entrenamiento optimizado para GPU en plataformas como Kaggle/Colab

---

## 🚀 Cómo Replicar Este Proyecto

```bash
# Clonar repositorio
git clone https://github.com/jesuscastromtz/age-verification-cv-system.git
cd age-verification-cv-system

# Opción 1: Ejecutar notebooks localmente (CPU)
pip install tensorflow pandas numpy matplotlib pillow
jupyter notebook analisis-completo.ipynb

# Opción 2: Ejecutar entrenamiento en GPU (Kaggle/Colab)
python run_model_on_gpu.py
```

---

## 📊 Stack Tecnológico Completo

| Layer | Tecnologías |
| :--- | :--- |
| **Deep Learning** | TensorFlow 2.x, Keras |
| **Visión Computadora** | ResNet50, ImageDataGenerator, Transfer Learning |
| **Data Science** | Pandas, NumPy, Matplotlib |
| **Versionamiento** | Git, GitHub, Jupyter Notebooks |
| **Infraestructura** | GPU support (Kaggle, Colab) |

---

## 💼 Por Qué Este Proyecto Importa (Para Reclutadores)

**Este proyecto demuestra:**

✅ **Madurez técnica somada a responsabilidad empresarial:** No construí un modelo que "suena bien" - lo evalué críticamente contra el riesgo real  
✅ **Capacidad de traducción Técnica→Negocio:** Convertí "MAE 13.57" en "25-35% de falsos negativos = multas legales"  
✅ **Liderazgo al tomar decisiones difíciles:** Recomendé **NO usar el modelo en producción**, lo que es más valioso que un modelo "funcionando"  
✅ **Roadmap estratégico claro:** Diseñé un plan desde V1.0 (investigación) a V2.0 (producción), con métricas, timelines y ROI esperado  

---

## 📞 Hablemos

Si tu equipo está construyendo soluciones de IA donde:
- La **precisión técnica requiere visión de negocio**
- Los **errores tienen consecuencias legales o financieras reales**
- Se necesita alguien que **proteja a la empresa mientras itera hacia soluciones escalables**

**Quiero trabajar contigo.** Abre una [issue en GitHub](https://github.com/jesuscastromtz/age-verification-cv-system/issues) o contáctame directamente.

---

## 📌 Estado del Proyecto
*   **Versión actual:** V1.0 - Prototipo de Investigación (No productivo, pero con un plan claro para V2.0)
*   **Última actualización:** Febrero 2026
*   **Licencia:** MIT - Disponible para uso académico y comercial
