# 🧠 Proyecto Final - PromptAudit

### Autor  
**Lautaro Falco**  
Curso: Generación de Prompts con IA  
Comisión: 76410  
Fecha: Agosto 2025  

---

## 📌 Introducción

**PromptAudit** es una herramienta diseñada para auditar la calidad de datasets en formato CSV antes de utilizarlos para análisis o toma de decisiones. Utiliza modelos de IA generativa para diagnosticar problemas comunes y generar visualizaciones explicativas, combinando código, texto e imagen en una notebook interactiva.

---

## 🔍 Presentación del problema

En entornos donde pequeñas empresas, emprendedores y estudiantes manejan datos, es común que los archivos CSV presenten errores ocultos: valores nulos, tipos mal definidos, duplicados, outliers y formatos inconsistentes.  
Estos problemas pueden llevar a decisiones erróneas en áreas críticas como ventas, inversión, logística y marketing. La falta de herramientas accesibles para auditar datos de forma visual y automatizada agrava esta situación.

---

## 💡 Propuesta de solución

La solución propuesta es **PromptAudit**, un sistema basado en *prompting* que conecta con modelos de IA de **OpenAI** para:

- Diagnosticar problemas de calidad en un dataset.
- Generar sugerencias de limpieza.
- Producir visualizaciones simples de los problemas detectados.

Se utiliza Fast Prompting para optimizar la interacción con los modelos, reduciendo costos y mejorando la precisión de las respuestas.

---

## 🎯 Objetivos

1. Comprender cómo aplicar **Fast Prompting** para optimizar interacciones con la IA.  
2. Diseñar una **POC funcional en Jupyter Notebook**.  
3. Minimizar consultas innecesarias a la API, reduciendo costos y mejorando eficiencia.  
4. Demostrar cómo el prompting puede mejorar la confiabilidad de un dataset.  
5. Evaluar la viabilidad técnica y económica del proyecto.

---

## 🧪 Metodología

1. **Carga y preprocesamiento**: Lectura del CSV en Python, obtención de resúmenes de datos.  
2. **Texto → Texto**: Prompt a `gpt-4o-mini` para diagnóstico automático.  
3. **Texto → Imagen**: Prompt a `gpt-image-1` para generar visualización de nulos, duplicados y outliers.  
4. **Fast Prompting**: Uso de prompts concisos, con estructura clara y estilo definido, optimizando tokens y resultados.  
5. **Documentación**: Registro de decisiones técnicas, resultados y reflexiones.

---

## 🛠️ Herramientas y tecnologías

- **Python** (`pandas`, `dotenv`, `openai`, `PIL`)  
- **OpenAI API**  
  - `gpt-4o-mini`: para diagnóstico textual.  
  - `gpt-image-1`: para generación de imágenes.  
- **Jupyter Notebook**: entorno de desarrollo y presentación.  
- **Archivo `.env`**: para proteger la clave de API.  
- **`.gitignore`**: para evitar subir claves privadas y archivos temporales.

---

## ⚙️ Implementación

La implementación se encuentra en `PromptAudit_POC.ipynb`.  
Incluye:

- Diagnóstico automático del dataset (texto → texto).  
- Visualización generada por IA (texto → imagen).  
- Registro de decisiones y reflexiones.

---

## 📊 Estimación de uso de tokens y costos

| Interacción           | Modelo usado     | Tokens estimados | Costo aproximado (USD) |
|-----------------------|------------------|------------------|-------------------------|
| Diagnóstico textual   | `gpt-4o-mini`    | ~1000 tokens     | ~$0.005                 |
| Generación de imagen  | `gpt-image-1`    | ~1000 tokens + imagen | ~$0.02–0.04 (según plan) |

> Total estimado por ejecución: **~$0.025–0.045 USD**

El aumento a 1000 tokens en el diagnóstico textual permite generar respuestas más completas, estructuradas y útiles, como reportes en formato Markdown con interpretación, recomendaciones y conclusiones.  
Se mantiene el enfoque de **Fast Prompting**, priorizando prompts bien diseñados que maximizan la calidad sin generar llamadas innecesarias.  
El costo sigue siendo accesible para entornos educativos, pruebas de concepto o proyectos personales.


---

## 🧠 Justificación de elecciones técnicas

- Se eligió **`gpt-4o-mini`** por su velocidad y bajo costo, ideal para respuestas breves y diagnósticos estructurados.  
- Se utilizó **`gpt-image-1`** en lugar de DALL·E por su mayor precisión en gráficos con números, etiquetas y estilo sobrio.  
- Los prompts fueron diseñados con estructura clara: concepto + estilo + idioma + formato, para maximizar la calidad visual y semántica.

---

## 📁 Estructura del repositorio

- `PromptAudit_POC.ipynb`: notebook principal con análisis, prompts y visualizaciones.  
- `dataset.csv`: dataset de prueba utilizado.  
- `infografia_calidad.png`: imagen generada por IA.  
- `.env.example`: archivo de ejemplo para configurar tu clave.  
- `.gitignore`: evita subir claves privadas y archivos temporales.  
- `README.md`: documentación completa del proyecto.

---

## 🧭 Cómo ejecutar el proyecto

1. Cloná el repositorio:
   ```bash
   git clone https://github.com/tuusuario/PromptAudit.git
   cd PromptAudit

2. Instalá las dependencias:
   pip install -r requirements.txt

3. Archivo `.env` con tu clave de OpenAI:
    OPENAI_API_KEY=tu_clave_aqui

4. Ejecutá el notebook PromptAudit_POC.ipynb desde Jupyter.


