# 📌 Detección de ciberataques neuronales basada en detección de anomalías 📌

Repositorio correspondiente al **Trabajo Fin de Máster (TFM)** del **Máster en Tecnologías de Análisis de Datos Masivos: Big Data** de la **Universidad de Murcia**.

El trabajo aborda la **detección del ciberataque neuronal Neuronal Flooding (FLO)** mediante **técnicas de Machine Learning y Deep Learning**, aplicadas a **simulaciones neuronales** bajo dos tipos de estímulos visuales: **Flash** y **Movie**.

---

## 📁 data/

Contiene los **datasets utilizados en los experimentos**, tanto los de las simulaciones neuronales originales como los generados para la detección de anomalías.

Incluye:
- Directorio **CSV**: simulaciones espontáneas y con ataque FLO del estímulo Flash.
- Directorio **spontaneous_30s_movie_one_resultados**: simulación neuronal espontánea del estímulo Movie.
- Archivo **spontaneous_30s_movie_one_resultados.zip**: simulaciones con ataque FLO del estímulo Movie.
- Conjuntos de datos separados en **train**, **validation** y **test**, para cada uno de los estímulos **Flash (supervisado y semisupervisado)** y **Movie**

---

## 📁 EstímuloFlash/

Notebooks asociados al análisis del **estímulo Flash**, organizados por enfoque:

### 🔹 Enfoque semisupervisado
- **ExperimentaciónLSTMAutoencoder.ipynb**  
  Implementación y evaluación de un **LSTM Autoencoder** entrenado únicamente con actividad espontánea.
- **RedifinciónConjuntoDatos.ipynb**  
  Redefinición del proceso de generación de datos para evitar **data leakage**.

### 🔹 Enfoque supervisado
- **GeneraciónConjuntoDatosSupervisado.ipynb**  
  Construcción del dataset etiquetado.
- **ExperimentaciónSupervisados.ipynb**  
  Evaluación de modelos supervisados:
  - Regresión Logística  
  - SVM  
  - Random Forest  
  - XGBoost  
  - MLP  

### 🔹 Estudio del tamaño de ventana
- **EstudioTamañoVentana.ipynb**  
  Análisis del impacto del tamaño de la ventana temporal en la representación de la señal neuronal.

---

## 📁 EstímuloMovie/

Notebooks asociados al **estímulo Movie**, caracterizado por una dinámica temporal más compleja:

- **PreprocesamientoMovie.ipynb**  
  Limpieza y preparación de los datos.
- **GeneracionConjuntosDatosMovie.ipynb**  
  Construcción del dataset para el enfoque semisupervisado.
- **ExperimentaciónMovie.ipynb**  
  Entrenamiento y evaluación de un **LSTM Autoencoder** mediante detección de **ráfagas de anomalías**.

---

## 🤖 modelo_LSTM_flash.keras

Modelo **LSTM Autoencoder** entrenado para la detección del ataque FLO con el **estímulo Flash**.

---

## 🤖 modelo_LSTM_movie.keras

Modelo **LSTM Autoencoder** entrenado para la detección del ataque FLO con el **estímulo Movie**.

---

## 📄 TFG_PascualBox_María.pdf

Memoria completa del **Trabajo Fin de Grado (TFG)** previo.

---

## 🎓 Autora

**María Pascual Box**  
Máster en Tecnologías de Análisis de Datos Masivos: Big Data  
**Universidad de Murcia**
