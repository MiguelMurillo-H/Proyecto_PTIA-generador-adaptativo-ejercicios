# Generador Adaptativo de Ejercicios

Sistema basado en RAG (Retrieval-Augmented Generation) que genera ejercicios de opción múltiple a partir de los apuntes en PDF de un estudiante y ajusta la dificultad según su desempeño durante la sesión de práctica.

Proyecto del curso Principios y Tecnologías de IA (PTIA), Escuela Colombiana de Ingeniería Julio Garavito.

**Integrantes:** Carlos Duban Rojas Riveros - Miguel Angel Murillo Hurtado

## Estado del proyecto

- [x] Prototipo de interfaz navegable: https://follow-stuff-35196601.figma.site
- [x] Primer avance del pipeline: lectura del PDF, fragmentación, indexación en ChromaDB y recuperación de los fragmentos más cercanos a un tema (`notebooks/`)
- [ ] Generación de preguntas con LLM (Hito 3)
- [ ] Módulo adaptativo de dificultad (Hito 3)
- [ ] MVP funcional con interfaz en Streamlit (Hito 3)

Nota: en el prototipo de Figma el contenido es simulado. La generación a partir de un PDF real se implementa en el Hito 3.

## Arquitectura prevista

Interfaz → Ingesta y segmentación → Indexación (embeddings + ChromaDB) → Recuperador → Generador (LLM) → Módulo adaptativo → Resumen de sesión.

## Herramientas

Python · pypdf · sentence-transformers · ChromaDB · API de LLM con capa gratuita · Streamlit · Figma

## Estructura del repositorio

- `notebooks/`: experimentos y pipeline de indexación
- `docs/`: capturas del prototipo y diagramas
- `data/`: documentos de prueba (los PDF no se suben al repositorio)

## Configuración

Las claves de API van en un archivo `.env` local, que no se sube al repositorio.

## Enlace al Jupyter Notebook: https://colab.research.google.com/drive/1GC043I-fdAcmLxCWPo-49ecgF6kOufa0?usp=sharing

