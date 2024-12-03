# Sobol Sampling para Optimización de Hiperparámetros

Este proyecto implementa **Sobol Sampling**, una técnica de muestreo utilizada frecuentemente en la optimización de hiperparámetros para modelos de aprendizaje automático. Sobol Sampling genera puntos distribuidos uniformemente en un espacio multidimensional, cubriendo de manera eficiente el rango de búsqueda definido.

## Descripción

En este ejemplo, se aplica Sobol Sampling para generar valores para dos hiperparámetros comunes:

1. **Learning Rate (Tasa de aprendizaje):** Controla el paso de ajuste de los pesos durante el entrenamiento de un modelo.
2. **Batch Size (Tamaño de lote):** Determina cuántas muestras se procesan juntas durante el entrenamiento.

El código genera un conjunto de puntos en este espacio de búsqueda, distribuidos de manera uniforme, asegurando una exploración eficiente.

### ¿Qué es Sobol Sampling?

Sobol Sampling utiliza secuencias Sobol, que son números cuasi-aleatorios diseñados para cubrir un espacio de manera uniforme. Esto lo hace especialmente útil para problemas donde es importante explorar todos los rincones del espacio de búsqueda, como la optimización de hiperparámetros.

## Requisitos

Antes de ejecutar este código, asegúrate de tener instaladas las siguientes bibliotecas:

- **NumPy:** Para trabajar con arreglos numéricos.
- **Matplotlib:** Para visualizar los puntos generados.
- **SciPy:** Para el generador de secuencias Sobol.

Puedes instalarlas ejecutando:

```bash
pip install numpy matplotlib scipy
```

## Código

El código realiza los siguientes pasos:

1. **Definir el espacio de búsqueda:** Se establecen los rangos de los hiperparámetros:
   - Learning rate: [0.01, 0.1]
   - Batch size: [16, 128]
2. **Generar puntos con Sobol Sampling:** Se usa el generador Sobol de `SciPy` para obtener puntos distribuidos uniformemente en el espacio normalizado [0, 1]. Luego, los puntos se reescalan a los rangos definidos.
3. **Visualizar los puntos:** Se crea un gráfico 2D para mostrar cómo se distribuyen las muestras en el espacio.

## Visualización

El gráfico generado muestra los puntos creados por Sobol Sampling. En el eje X se representa el rango del *learning rate* y en el eje Y el *batch size*. Los puntos distribuidos uniformemente indican que Sobol Sampling cubre el espacio eficientemente.

## Ejecución

Para ejecutar el código:

1. Copia el código en un archivo Python (por ejemplo, `sobol_sampling.py`).
2. Ejecuta el archivo en tu terminal o IDE:

```bash
python sobol_sampling.py
```

## Resultados Esperados

Un gráfico como este será generado:

![Sobol Sampling](ruta_a_la_imagen)

El gráfico demuestra cómo Sobol Sampling asegura una cobertura uniforme del espacio de búsqueda, maximizando la diversidad de combinaciones de hiperparámetros.

## Uso en Casos Reales

Sobol Sampling es útil en tareas como:
- Optimización de hiperparámetros en modelos de Machine Learning.
- Exploración de espacios de diseño en simulaciones.
- Búsqueda de configuraciones óptimas en problemas complejos.



