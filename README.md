# 📨 **Detector de Spam con IA**

Un clasificador de spam simple y efectivo desarrollado en Python. Este proyecto utiliza un modelo de **Naive Bayes** para detectar mensajes de texto no deseados (spam) basándose en su contenido.

## 🚀 **Objetivo**
Crear un sistema de clasificación de mensajes que pueda identificar si un mensaje es **spam** o **ham** (no spam) utilizando un conjunto de datos de SMS etiquetados.

## ⚙️ **Tecnologías**
- **Python**: Lenguaje de programación.
- **scikit-learn**: Para crear el modelo de Naive Bayes y vectorización de texto.
- **pandas**: Para la manipulación de datos.
- **nltk**: Para el procesamiento de lenguaje natural (opcional).
- **matplotlib** (opcional): Para visualizaciones de métricas.

## 🛠️ **Instalación**
1. Clona este repositorio en tu máquina local:
    ```bash
    git clone https://github.com/tu_usuario/detector-de-spam.git
    cd detector-de-spam
    ```

2. Crea un entorno virtual (opcional pero recomendado):
    ```bash
    python -m venv venv
    source venv/bin/activate  # En Linux/macOS
    venv\Scripts\activate  # En Windows
    ```

3. Instala las dependencias:
    ```bash
    pip install -r requirements.txt
    ```

4. Descarga el dataset de [Kaggle](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset) o usa el que tienes localmente.

## 🔍 **¿Cómo funciona?**

### 1. **Preprocesamiento del Dataset**
- Limpieza de valores nulos y formateo de las columnas.
- Conversión de las etiquetas a valores binarios (spam = 1, ham = 0).

### 2. **Vectorización TF-IDF**
Convierte las sinopsis de los mensajes en vectores numéricos usando la técnica **TF-IDF** (Term Frequency-Inverse Document Frequency).

### 3. **Modelo Naive Bayes**
Entrenamiento del modelo Naive Bayes utilizando el conjunto de datos procesado.

### 4. **Predicción**
Predice si un mensaje es spam o no spam (ham).

## 📝 **Cómo usarlo**

1. Clona el repositorio y asegúrate de que tienes el dataset disponible.
2. Ejecuta el script para entrenar el modelo y hacer predicciones:
    ```bash
    python detector_spam.py
    ```

3. Puedes probar el clasificador con nuevos mensajes:
    ```python
    test_message = ["Congratulations! You've won a $1,000 Walmart gift card. Call now!"]
    prediction = model.predict(test_vector)
    print("¿Es spam?:", "Sí" if prediction[0] == 1 else "No")
    ```

## 📊 **Resultados**

El modelo puede predecir si un mensaje es **spam** o **ham** con una precisión que varía según el dataset y la cantidad de datos de entrenamiento.

### Ejemplo de salida:
```bash
Accuracy: 0.976
Classification Report:
              precision    recall  f1-score   support
    0 (ham)       0.98      0.99      0.99       965
    1 (spam)      0.98      0.95      0.96       149
```

## 📅 **Mejoras futuras**
Ajuste de parámetros para mejorar la precisión del modelo.
Incorporación de técnicas de NLP avanzadas como el Lematizado y TF-IDF ponderado.
Implementación de una interfaz web para interacción en tiempo real usando Flask o Streamlit.

## 📝 **Licencia**
Este proyecto está bajo la Licencia MIT.

## 🙌 **Contribuciones**
Las contribuciones son bienvenidas. Si deseas mejorar el proyecto, abre un Pull Request con tus cambios.