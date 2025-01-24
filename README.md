# **Visión Artificial - UNIR**
# **Actividad grupal: exploración de filtros espaciales y morfológicos en escenarios reales.**

---

#### **Autores del Notebook**   
- **Jara Arroyo, Miguel**  
- **García Mayorga, Ismael**  
- **Parra Idarraga, Óscar**  
- **Caballero Cortes, Marcos**  

---

## Detección de Tomates Maduros en Plantaciones
Este notebook tiene como objetivo la detección de tomates maduros en una plantación a partir de imágenes extraídas de un video. Para lograrlo, se emplean **filtros espaciales** y **filtros morfológicos** que permiten, respectivamente, mejorar la calidad de las imágenes y refinar las regiones detectadas. Las imágenes utilizadas provienen del dataset disponible en [datasetninja.com/tomatod](https://datasetninja.com/tomatod).


## **Metodología**

### Filtrado Espacial
En este paso se utiliza un **filtro espacial**. Las imágenes son cargadas en formato RGB y suavizadas mediante un filtro gaussiano, lo que permite reducir el ruido y facilitar los pasos posteriores. Posteriormente, se realiza una conversión al espacio de color HSV para aislar mejor los colores asociados a los tomates maduros.

### Detección de Color
Se trabaja sobre las imágenes en el espacio de color HSV. Se definen rangos específicos para el color rojo, considerando tanto tonos intermedios como extremos. A partir de estos rangos, se generan máscaras binarias que permiten segmentar las regiones rojas en la imagen.

### Filtrado Morfológico
En este paso se aplican **filtros morfológicos**. Se utilizan operaciones de cierre (dilatación seguida de erosión) para eliminar pequeñas imperfecciones o áreas de ruido, y operaciones de apertura (erosión seguida de dilatación) para perfeccionar las formas de las regiones detectadas. Esto se realiza utilizando un kernel elíptico.

### Detección y Análisis de Contornos
Una vez filtradas las regiones mediante operaciones espaciales y morfológicas, se identifican los contornos de las áreas segmentadas. Sobre estas regiones se dibujan rectángulos alrededor de cada tomate detectado. Además, se calculan y muestran las características de cada tomate, como su posición, dimensiones y área.

### Resultado Final
El resultado final es una imagen procesada donde los tomates maduros están claramente identificados. Cada tomate está numerado y marcado con un rectángulo, acompañado de un registro detallado con sus características.

![image](https://github.com/user-attachments/assets/a553dbdf-ef3e-4555-8568-9bb0caea6e46)


---

## **Citación del Conjunto de Datos**  
Tsironis V., Bourou S., Stentoumis C. (2020). *tomatOD: Evaluation of object detection algorithms on a new real-world tomato dataset.*  
ISPRS - International Archives of the Photogrammetry, Remote Sensing and Spatial Information Sciences.  
Disponible en: [https://github.com/up2metric/tomatOD](https://github.com/up2metric/tomatOD)  


---
---


# English:
# **Computer Vision - UNIR**  
# **Group Activity: Exploring Spatial and Morphological Filters in Real-World Scenarios**

---

#### **Notebook Authors**  
- **Jara Arroyo, Miguel**  
- **García Mayorga, Ismael**  
- **Parra Idarraga, Óscar**  
- **Caballero Cortes, Marcos**  

---

## **Detection of Ripe Tomatoes in Plantations**  
This notebook aims to detect ripe tomatoes in a plantation using images extracted from a video. The process employs **spatial filters** and **morphological filters** to enhance image quality and refine detected regions. The images used come from the dataset available at [datasetninja.com/tomatod](https://datasetninja.com/tomatod).  

---

## **Methodology**

### **Spatial Filtering**  
This step involves the application of a **spatial filter**. Images are loaded in RGB format and smoothed using a Gaussian filter, which reduces noise and facilitates subsequent processing steps. Then, the images are converted to the HSV color space to better isolate the colors associated with ripe tomatoes.  

### **Color Detection**  
The images are processed in the HSV color space. Specific ranges for the color red, covering both intermediate and extreme tones, are defined. Based on these ranges, binary masks are generated to segment the red regions in the image.  

### **Morphological Filtering**  
At this stage, **morphological filters** are applied. Closing operations (dilation followed by erosion) are used to eliminate small imperfections or noisy areas, and opening operations (erosion followed by dilation) are used to refine the shapes of the detected regions. These operations are performed using an elliptical kernel.  

### **Contour Detection and Analysis**  
After filtering the regions using spatial and morphological operations, contours of the segmented areas are identified. Rectangles are drawn around each detected tomato, and the characteristics of each tomato, such as position, dimensions, and area, are calculated and displayed.  

### **Final Result**  
The final output is a processed image where ripe tomatoes are clearly identified. Each tomato is numbered and marked with a rectangle, accompanied by a detailed record of its characteristics.  

![image](https://github.com/user-attachments/assets/a553dbdf-ef3e-4555-8568-9bb0caea6e46)

---

## **Dataset Citation** 
Tsironis V., Bourou S., Stentoumis C. (2020). *tomatOD: Evaluation of object detection algorithms on a new real-world tomato dataset.*  
ISPRS - International Archives of the Photogrammetry, Remote Sensing and Spatial Information Sciences.  
Available at: [https://github.com/up2metric/tomatOD](https://github.com/up2metric/tomatOD)  


---
