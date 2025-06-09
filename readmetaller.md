# Proyecto: Visualización y Predicción con Red Convolucional entrenada en MNIST

Este proyecto consiste en trabajar con un modelo convolucional previamente entrenado en el conjunto de datos MNIST. El objetivo es explorar y visualizar sus **kernels**, **mapas de activación** y probarlo con **imágenes propias** procesadas para hacer predicciones.

---

## 🧠 Punto 1: ¿Cómo son los kernels del modelo preentrenado?

**¿Qué se hace?**

Se cargan los pesos del modelo (`mnist_model.h5`) y se extraen los **kernels** (filtros) de la **primera capa convolucional**. Estos filtros son los que el modelo ha aprendido para detectar patrones simples como bordes, líneas, etc.

**¿Qué se muestra?**

- Se visualizan los primeros 10 kernels aplicados al primer canal de entrada.
- Se imprimen los valores numéricos de esos kernels para analizar su contenido.

**¿Para qué sirve?**

Para entender cómo el modelo "ve" y procesa las imágenes: estos filtros son fundamentales para extraer características útiles para la clasificación.

---

## 🌀 Punto 2: ¿Cómo se ve la salida de la convolución con los kernels?

**¿Qué se hace?**

Se toma una imagen del conjunto de prueba de MNIST (por ejemplo `x_test[1]`) y se pasa a través del modelo **hasta la primera capa convolucional**.

**¿Qué se muestra?**

Se visualizan los **feature maps** generados por la convolución de la imagen con los primeros 10 kernels. Cada mapa representa cómo responde un filtro específico ante la imagen.

**¿Para qué sirve?**

Permite visualizar cómo cada filtro "detecta" diferentes partes de una imagen: bordes, zonas oscuras, líneas, etc. Es la primera etapa del "proceso visual" del modelo.

---

## 🖼️ Punto 3: ¿Cómo se predicen dígitos en imágenes propias?

**¿Qué se hace?**

Se procesan 10 imágenes propias (una por cada dígito del 0 al 9). Para que sean compatibles con el modelo, se aplican los siguientes pasos de **preprocesamiento**:

1. Convertir a escala de grises.
2. Redimensionar a 28x28 píxeles.
3. Invertir blanco y negro (fondo negro, número blanco).
4. Centrar el número en la imagen.
5. Normalizar a valores entre 0 y 1.
6. Dar forma `(28, 28, 1)`.

**¿Qué se muestra?**

- Se visualizan las imágenes procesadas.
- Se muestran las predicciones del modelo sobre cada una.

**¿Para qué sirve?**

Demuestra que el modelo puede generalizar más allá del dataset original si las imágenes externas son correctamente preprocesadas.

---

## 🔄 Punto 4: ¿Qué ocurre si aplico los kernels a una imagen propia?

**¿Qué se hace?**

Se selecciona una de las imágenes propias (por ejemplo `5.jpg`), se preprocesa y se pasa **a través de la primera capa convolucional** del modelo.

**¿Qué se muestra?**

Se visualizan los **feature maps** resultantes (salidas de la convolución) de esta imagen con los 10 primeros filtros del modelo.

**¿Para qué sirve?**

Permite comparar visualmente cómo el modelo procesa una imagen real frente a una imagen del dataset original. Es útil para evaluar si el preprocesamiento fue exitoso.

---

## 📦 Requisitos del entorno

- TensorFlow
- OpenCV (`cv2`)
- NumPy
- Matplotlib
- PIL (opcional, para carga de imágenes propias)

---

## GRUPOS DE TRABAJO
- mIGUEL diaz 
- Cesar Porras
- Over Medrano

