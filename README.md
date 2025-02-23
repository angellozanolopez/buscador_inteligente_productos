# **Formación en NLP e interpretación de textos + extracción de contenido**

## **Introducción**

En pocas ocasiones, cuando una empresa recibe una solicitud de presupuesto, éste incluye las referencias de producto exactas. En cambio, los clientes solicitan los presupuestos por ejemplo en un e-mail:

> "Hola, quisiera cuatro cajas de arroz, seis pallets de azúcar..."

## **Ejercicio**

El sistema a desarrollar consiste en crear un modelo que pueda identificar qué productos se solicitan.

Para ello, te proporcionamos el siguiente dataset: [Dataset de productos](https://apioverstand.es/training/dataset_productos.csv)

Con ellos, genera manualmente varios textos de muestra donde se soliciten varios de estos productos. La idea es que tu sistema traduzca, por ejemplo, en el caso anterior:

> "cien chuletas de cordero paletilla" → **producto id 7 | 100 unidades**  
> "15 Aguardiente de orujo El Afilador 70 cl" → **producto id 63 | 15 unidades**

## **Entregable 1**

Análisis de tecnologías existentes y, si llevan coste asociado, pantallazo de dicho coste. Se dará prioridad a las tecnologías open source que no lleven costes asociados.

En base a ello, se decidirá por la tecnología a usar y se procederá al desarrollo de la solución.

## **Entregable 2**

### **Entregables (en un único WeTransfer):**
✅ Código fuente de la solución  
✅ Video explicativo del código fuente (máximo 3 minutos)  
✅ Video mostrando e interpretando los resultados (máximo 2 minutos)  

---

# **SOLUCIÓN**

## **Entregable 1: Análisis de tecnologías y costos asociados**

El desarrollo de un sistema de detección de solicitudes de productos a partir de texto implica el uso de varias tecnologías clave:

### **1. Lenguaje de Programación y Entorno de Desarrollo:**
- **Python**: Con su amplia comunidad, flexibilidad y una gama robusta de bibliotecas, Python es una elección sólida. Además, puede emplearse en entornos como **Jupyter Notebooks** o IDEs como **VSCode** para la construcción del sistema.

### **2. Librerías de Manipulación y Análisis de Datos:**
- **Pandas y NumPy**: Estas librerías son fundamentales para la manipulación, limpieza y procesamiento de datos estructurados. Son de código abierto y ofrecen herramientas poderosas para trabajar con conjuntos de datos.

### **3. Algoritmos de Similitud y Procesamiento de Texto:**
- **Cosine Similarity (scikit-learn)**: Utilizado para calcular la similitud entre vectores o matrices, esta función es esencial en el procesamiento de texto y la comparación de solicitudes con productos existentes.

### **4. Vectorización de Texto:**
- **CountVectorizer (scikit-learn)**: Una herramienta clave para la conversión de texto en vectores numéricos, facilitando su procesamiento y análisis en algoritmos de aprendizaje automático.

### **5. Costos Asociados:**
La mayoría de estas tecnologías son de código abierto y no tienen costos asociados. Sin embargo, en proyectos que involucren almacenamiento masivo de datos o utilización intensiva de servicios en la nube para entrenamiento de modelos, plataformas como **AWS** pueden ofrecer niveles de servicio gratuitos con limitaciones o niveles de servicio de pago.

Considerando la preferencia por tecnologías de código abierto y sin costos asociados, el uso de bibliotecas como **NumPy, Pandas, CountVectorizer** y la funcionalidad de **cosine_similarity** en **scikit-learn** es una elección sólida para este proyecto.

---

## **Entregable 2: Desarrollo y entrega**

Para realizar el código se han seguido los siguientes pasos:

1. **Importar librerías:**  
   - Importar las librerías necesarias (**pandas, scikit-learn, etc.**).

2. **Cargar el dataset:**  
   - Cargar el conjunto de datos que contiene la información de los productos.

3. **Manejo de datos faltantes:**  
   - Verificar si hay registros nulos o vacíos en el dataset.

4. **Eliminación de registros nulos:**  
   - Si se encuentran registros nulos, eliminarlos del conjunto de datos.

5. **Identificación de registros duplicados:**  
   - Revisar si existen registros duplicados en el dataset.

6. **Normalización de texto:**  
   - Eliminar tildes u otros caracteres especiales del texto de los productos para una comparación más precisa.

7. **Cálculo de similitud coseno:**  
   - Utilizar la similitud del coseno para comparar la frase del pedido del cliente con los registros del dataset.

8. **Localización del producto y su ID:**  
   - Identificar el producto más similar a la frase del pedido y obtener su ID.

9. **Extracción de la cantidad:**  
   - Extraer la cantidad mencionada en la frase del cliente.

10. **Conversión de cantidad texto a numérica:**  
   - Si la cantidad está expresada en texto, convertirla a su representación numérica.

11. **Obtención de la cantidad final en formato numérico:**  
   - Obtener la cantidad final en formato numérico para el producto.

12. **Verificación del resultado final:**  
   - Verificar y asegurar que la cantidad y el producto identificado sean correctos con varios ejemplos.

---

## **🎥 Video Explicativo y Demostración**

🔹 [![Ver en YouTube](https://img.shields.io/badge/🎥%20Explicación%20del%20Código-red?logo=youtube&logoColor=white)](https://youtu.be/A0CEHH_zB-k)  
🔹 [![Ver en YouTube](https://img.shields.io/badge/🎥%20Demostración-red?logo=youtube&logoColor=white)](https://youtu.be/ihCvrrKcUKM)  
📌 *Haz clic con el botón derecho encima del botón y selecciona "Abrir enlace en una nueva pestaña" para no salir del repositorio.*

