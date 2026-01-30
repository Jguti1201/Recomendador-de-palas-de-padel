# 🎾 Encuentra tu Pala de Pádel Ideal — AI Recommender System

Aplicación web desarrollada con **Streamlit** que utiliza **inteligencia artificial y búsqueda semántica** para recomendar palas de pádel personalizadas según el perfil del jugador.

El sistema combina:
- Información técnica extraída de documentación especializada
- Embeddings vectoriales
- Modelos de lenguaje de **Azure OpenAI**
para ofrecer recomendaciones **explicadas, coherentes y accionables**.

---

## 🚀 Funcionalidades principales

- 🧠 **Recomendación personalizada de palas**
- 📄 Análisis automático de documentación técnica en PDF
- 🔍 **Búsqueda semántica** mediante embeddings y similitud coseno
- 🎯 Filtros por:
  - Nivel de juego
  - Tipo de jugador
  - Lesiones (codo)
  - Rango de precio
- 💬 Explicación en lenguaje natural del porqué de cada recomendación
- 🌐 Enlaces directos a compra

---

## 🧠 Cómo funciona el sistema

1. **Carga de documentación**
   - Se extrae texto desde un PDF con criterios de elección de palas

2. **Embeddings**
   - Cada pala está representada como un vector semántico
   - Se almacenan en un archivo JSON (`palas_embeddings.json`)

3. **Consulta del usuario**
   - Se construye un prompt con:
     - Perfil del jugador
     - Preferencias
     - Documentación técnica

4. **Generación de recomendaciones**
   - Azure OpenAI genera el perfil ideal de pala
   - Se buscan las palas más similares por **cosine similarity**

5. **Resultados**
   - Top palas recomendadas
   - Explicación detallada
   - Precio y link de compra

---

## 🛠️ Tecnologías utilizadas

- **Python**
- **Streamlit**
- **Azure OpenAI**
  - `gpt-35-turbo`
  - `text-embedding-ada-002`
- **NumPy**
- **PyMuPDF (fitz)**
- **JSON**
- **Machine Learning / NLP**

---


