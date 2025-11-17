# 🧠 MedPrompt  
### **LLM–CNN Fusion with Dynamic Weight Routing for Medical Image Segmentation & Classification**

MedPrompt is a unified, prompt-driven medical image analysis framework that fuses a **few-shot Large Language Model (LLaMA-4-17B)** with a lightweight yet powerful CNN architecture (**DeepFusionLab**) to perform **segmentation** and **classification** directly from **natural language instructions**.

Unlike traditional medical AI systems that rely on numerous task-specific models, MedPrompt interprets your textual prompt, selects the appropriate pretrained weights, and executes multi-stage and conditional workflows—**without retraining**.

---

<p align="center">
  <img src="assets/medprompt_architecture.png" width="85%" />
</p>

---

## 🚀 Key Features

### 🔹 **1. Natural Language → Structured Workflow**
MedPrompt automatically:
- Parses user prompts  
- Detects intent (classification / segmentation)  
- Normalizes targets (e.g., lung, retina, TB, pneumonia)  
- Generates JSON-based task pipelines  
- Handles multi-step and conditional workflows  

**Example prompt:**
"Check for tuberculosis. If detected, segment the lungs."

---

## 🔹 **2. Dynamic Weight Routing**
A novel routing mechanism that:
- Matches tasks to pretrained weights  
- Uses semantic similarity scoring  
- Allows plug-and-play expansion with new weights  
- Avoids retraining  

> Add new weights → MedPrompt automatically routes them.

---

## 🔹 **3. DeepFusionLab – A Dual-Mode CNN**

DeepFusionLab supports:
- **Classification** (mode = 0)  
- **Segmentation** (mode = 1)  

It includes:
- EfficientNet-B0 encoder  
- ASPP multi-scale context module  
- MFF (Multi-Feature Fusion)  
- Lightweight decoder  
- CAFSE attention refinement  

<p align="center">
  <img src="assets/deepfusionlab.png" width="85%">
</p>

---

## 🔹 **4. Strong Performance Across 19 Datasets**

| Task | Performance |
|------|-------------|
| Lung Segmentation | **Dice ≈ 0.986** |
| TB Classification | **F1 ≈ 0.974** |
| Polyp Segmentation | **Dice ≈ 0.945** |
| Retinal Vessel Segmentation | **Dice ≈ 0.811** |
| COVID-19 Classification | **Acc ≈ 0.997** |

---

## 🔹 **5. Fast & Deployment-Ready**
- **97%** prompt-interpretation correctness  
- **~2.5s** CPU end-to-end latency  
- Runs efficiently in low-resource environments  

---

# 📁 Repository Structure
MedPrompt/
│
├── classification-training-for-deepfusionlab.ipynb # Notebook on how to train DeepFusionLab on Classification Datasets
├── medprompt-framework.ipynb #Running Medprompt
├── segmentation-training-for-deepfusionlab.ipynb # Notebook on how to train DeepFusionLab on Segmentation Datasets


