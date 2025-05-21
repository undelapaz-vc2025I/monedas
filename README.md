## Ejercicio: Conteo de Monedas mediante Componentes Conectadas

Este ejercicio tiene como objetivo implementar un pipeline de procesamiento de imágenes para contar el número de monedas presentes en una fotografía, utilizando técnicas de visión por computador y análisis de componentes conectadas.

### Descripción

A partir de dos imágenes:

* **`monedas.jpg`**, ya incluida en este repositorio, y
* **una imagen adicional** similar, que **debe ser subida por el estudiante al repositorio**,

el script ejecuta un conjunto de pasos para identificar y contar las monedas presentes.

### Proceso

1. **Carga de imagen**: Se leen ambas imágenes desde el repositorio.
2. **Preprocesamiento de cada imagen**:

   * Conversión a escala de grises.
   * Binarización mediante umbral fijo o adaptativo.
   * Aplicación de operaciones morfológicas (por ejemplo: apertura o cierre) para eliminar ruido y separar objetos conectados.
3. **Reducción de resolución**: Se genera una máscara binaria con tamaño igual o menor a la mitad del original.
4. **Detección de componentes conectadas**: Se aplica un algoritmo de etiquetado para identificar regiones individuales que corresponden a monedas.
5. **Visualización y salida**:

   * Se imprime en consola el número de monedas detectadas.
   * Se muestra y guarda una imagen con las regiones conectadas coloreadas y etiquetadas.

### Tecnologías

* Python
* OpenCV (`cv2`)
* NumPy
* Matplotlib (opcional, para visualización)

### Requisitos

* Trabajar obligatoriamente con la imagen `monedas.jpg`.
* Subir una imagen adicional tomada por el estudiante y trabajar también con ella.
* Incluir ambas pruebas en la ejecución del script o en cuadernos separados.

### Ejecución

Una vez instaladas las dependencias, ejecuta:

```bash
python contar_monedas.py
```

Este script debe mostrar los resultados para ambas imágenes (la incluida y la subida por el estudiante).

### Archivos esperados

* `monedas.jpg`: Imagen base incluida en el repositorio.
* `mi_moneda.jpg`: Imagen adicional proporcionada por el estudiante.
* `contar_monedas.py`: Script principal.
* `resultado_moneda_1.png` y `resultado_moneda_2.png`: Imágenes generadas con regiones coloreadas.
