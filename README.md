# Proyecto Final - PromptAudit

### Autor
Lautaro Falco  
Curso: Generación de Prompts con IA  
Comisión: 76410  
Fecha: Agosto 2025  

---

## Introducción
**PromptAudit** es una herramienta diseñada para auditar la calidad de datasets en formato CSV antes de utilizarlos para análisis o toma de decisiones.  

---

## Presentación del problema
En entornos donde pequeñas empresas, emprendedores y estudiantes manejan datos, es común que los archivos CSV presenten errores ocultos: valores nulos, tipos mal definidos, duplicados, outliers y formatos inconsistentes.  
Esto puede llevar a decisiones erróneas en áreas críticas como ventas, inversión, logística y marketing.

---

## Propuesta de solución
La solución propuesta es **PromptAudit**, un sistema basado en *prompting* que conecta con modelos de IA (Gemini + Hugging Face) para:
- Diagnosticar problemas de calidad en un dataset.
- Generar sugerencias de limpieza.
- Producir visualizaciones simples de los problemas detectados.

---

## Objetivos
1. Comprender cómo aplicar **Fast Prompting** para optimizar interacciones con la IA.  
2. Diseñar una **POC funcional en Jupyter Notebook**.  
3. Minimizar consultas innecesarias a la API, reduciendo costos y mejorando eficiencia.  
4. Demostrar cómo el prompting puede mejorar la confiabilidad de un dataset.  

---

## Metodología
1. **Carga y preprocesamiento**: Lectura del CSV en Python, obtención de resúmenes de datos.  
2. **Texto → Texto**: Prompts a Gemini para diagnóstico, riesgos y sugerencias.  
3. **Texto → Imagen**: Prompts a Hugging Face para generar visualizaciones (ej. nulos, duplicados, outliers).  
4. **Fast Prompting**: Uso de prompts concisos, enfocados en resultados específicos, optimizando el número de tokens.  

---

## Herramientas y tecnologías
- **Python** (pandas, matplotlib, dotenv)  
- **Gemini API** (texto → texto)  
- **CLIPDROP API** (texto → imagen, con modelos como `stabilityai/stable-diffusion`)  
- **Jupyter Notebook** para la POC  

---

## Implementación
La implementación se encuentra en [`notebook/PromptAudit_POC.ipynb`](notebook/PromptAudit_POC.ipynb).  

Incluye ejemplos de:
- Diagnóstico automático de dataset (texto → texto).  
- Visualización generada por IA de problemas de calidad (texto → imagen).  
- Optimización con **Fast Prompting**.  