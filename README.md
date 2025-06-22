# Trabajo Fin de Máster

Este repositorio contiene el código desarrollado para el Trabajo de Fin de Máster **"Segmentación automática de paneles solares en imágenes aéreas mediante arquitecturas U-Net"**. El objetivo principal es detectar y segmentar paneles solares en tejados a partir de imágenes satelitales usando redes convolucionales.


## 🧠 Modelos implementados

- 🔹 **U-Net estándar**: arquitectura completa, entrenada desde cero.
- 🔸 **Mini U-Net**: versión compacta para entornos con menos recursos.
- 🧩 **U-Net + ResNet34**: arquitectura con encoder preentrenado en ImageNet usando _transfer learning_.

## 📊 Resultados

| Modelo              | Dice (Val) | IoU (Val) | Parámetros | Tamaño | Observaciones |
|---------------------|------------|-----------|------------|--------|----------------|
| U-Net               | 0.9058     | 0.8319    | ~31M       | Alto   | Precisión alta, entrenamiento más lento |
| Mini U-Net          | 0.8863     | 0.8004    | ~7.7M      | Bajo   | Más rápido, menor precisión |
| U-Net + ResNet34    | 0.8653     | 0.7709    | ~23M       | Medio  | Converge rápido, pero peor generaliza |

También se realizó un test real sobre imágenes del municipio de **Molina de Segura**, donde se evaluó la capacidad de generalización de los modelos.

## 🔍 Visualización y análisis

El repositorio incluye:
- Visualizaciones de segmentación sobre nuevas imágenes.
- Activaciones con **Grad-CAM** para interpretar la atención del modelo.
- Comparativas cuantitativas y cualitativas.
