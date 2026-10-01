# Comparative Study: Garbage Classification using InceptionV3 vs. MobileNetV2

An end-to-end automated solid waste classification benchmark comparing a high-capacity multi-scale CNN (**InceptionV3**) with an edge-optimized lightweight CNN (**MobileNetV2**). Both models were trained for 100 epochs on the benchmark TrashNet dataset.

---

## 📊 Performance Benchmark (100 Epochs)

| Metric | InceptionV3 | MobileNetV2 | Advantage |
| :--- | :--- | :--- | :--- |
| **Input Shape** | 299 × 299 × 3 | 224 × 224 × 3 | MobileNetV2 (lower memory footprint) |
| **Training Time/Epoch** | ~54–57 s/epoch | ~3–4 s/epoch | **MobileNetV2 (~15x faster)** |
| **Total Training Time** | ~90 mins | ~8 mins | **MobileNetV2** |
| **Training Accuracy** | 94.22% | 98.62% | MobileNetV2 |
| **Peak Validation Accuracy** | 84.49% | **84.95%** | **MobileNetV2 (+0.46%)** |
| **Validation Loss** | 0.5780 | **0.4209** | **MobileNetV2 (-0.1571)** |
| **Parameter Footprint** | ~23.8M | ~3.5M | MobileNetV2 (~6.8x smaller) |

---

## 🗂️ Dataset Details
- **Dataset:** TrashNet (Gary Thung & Mindy Yang)
- **Total Images:** 2,527 images
- **Classes (6):** Cardboard (403), Glass (501), Metal (410), Paper (594), Plastic (482), Trash (137)
- **Split:** 80% Training (2,024 images) / 20% Validation (503 images)

---

## 📁 Repository Structure
- `InceptionV3_Garbage_Classification.ipynb`: Google Colab implementation for InceptionV3 model training and evaluation.
- `MobileNetV2_Garbage_Classification.ipynb`: Google Colab implementation for MobileNetV2 model training and evaluation.
- `accuracy_loss_graph.png`: Training vs. Validation curves.

---

## 🚀 Live Demo (Gradio)
The interactive demo interface is built with Gradio and can be launched directly inside the Colab notebooks to classify uploaded waste images across the 6 classes.
