# LAB04 Ramos Mamani Crishman

1. IA‑Colores (jojeda5171/IA-Colores)

¿Qué hace?
Es un sistema que clasifica colores en imágenes usando algoritmos de machine learning (KNN y SVM), y emplea YOLO para detectar personas en tiempo real, luego aplica la clasificación de colores al torso y piernas de las personas detectadas
github.com+1github.com+1
.

Principales componentes:

  knn.py, svm.py, svm1.py: scripts de entrenamiento de clasificadores (KNN/SVM) tras preprocesar imágenes (filtro de mediana, normalización, aplanamiento).

  main.py: carga el modelo SVM entrenado, utiliza YOLO para detección de personas y clasifica los colores sobre regiones específicas.

  Carpeta Data/Colors/: contiene conjuntos de imágenes etiquetadas por color.

  Carpeta Models/: almacena los modelos entrenados.

Aplicación en diseño y animación 2D/3D:

  Selección automática de paletas: analizar escenas renderizadas para extraer colores predominantes en vestuario, fondo, objetos.

  Análisis de consistencia cromática: validar que estilos visuales cumplan con paletas predefinidas.

  Interacción en herramientas: integrar detección de color en tiempo real en interfaces de diseño, para feedback instantáneo al animador.

  Posproducción: clasificación automática de partes (ropa, piel) para ajustes segmentados de color en post.

2. Co‑Tracker (facebookresearch/co‑tracker)

¿Qué hace?
Es un modelo basado en Transformers que permite seguir cualquier punto (pixel) en un video. Integra ventajas de Optical Flow y ofrece seguimiento:

  de un pixel,

  de un conjunto cuasi-denso de puntos,

  mediante selección manual o muestreo en cuadrícula
  github.com
  github.com+6github.com+6github.com+6
  .

Versiones y avances:

  CoTracker2: seguimiento de miles de puntos (hasta 265×265) con eficiencia de memoria.

  CoTracker3: arquitectura mejorada, entrenada con 1000× menos datos, más ligera
  github.com+10github.com+10github.com+10
  .

  Incluye VGA SfM (Structure from Motion) para recuperación de poses y estructura 3D
  github.com+5github.com+5github.com+5
  .

  Demo interactiva via Gradio y notebooks disponibles para pruebas
  github.com+2github.com+2github.com+2
  .

Aplicación en diseño y animación 2D/3D:

  Rotoscopia avanzada: trazado preciso de contornos y puntos de interés en escenas animadas para máscaras o tracking.

  Transferencia de movimientos entre rigs: seguimiento de puntos en captura de movimiento y aplicación a modelos 3D.

  Estabilización y corrección de planos: medir desplazamientos sutiles entre cuadros para mejorar interpolación o anticipación.

  Reconstrucción de cámara: con SfM, extraer movimientos de cámara en escena para integrar elementos 3D consistentes.

  Herramientas de animación asistida: seleccionar puntos específicos en frames clave y que el modelo propague su posición automáticamente en frames intermedios.
