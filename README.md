# GFMdataset: Publicly Available UAV Image Dataset of Mining-Induced Ground Fissures

Motivated by advances in deep learning for ground fissure detection, we introduce the **GFM (Ground Fissures in Mining areas)** dataset—a meticulously annotated and comprehensive UAV-based resource designed for **instance segmentation** in mining-induced fissure scenarios—and provide a novel framework for its application.

This repository provides the publicly available resources related to the paper:

**“A UAV-based Image Dataset and a Novel Morphological Feature Extraction Framework for Identifying Ground Fissures Caused by Coal Mining Activities”**

---

## 1. Publicly Available Resources

To ensure **reproducibility** and **transparency**, the following materials are currently released.

### 1.1 GFM YOLO-Format Subset (Trainable & Testable)

A **representative** and fully annotated subset of the GFM dataset in **YOLO instance segmentation format** is publicly available:

- **Download (Google Drive):**  
  https://drive.google.com/file/d/1enheDcyM0bzJO5CMdXAa--QexW3HEs_R/view?usp=drive_link

**The released subset:**
- ✅ Directly trainable under **YOLOv8-seg**
- ✅ Contains complete **image–label** pairs
- ✅ Covers representative fissure scenarios (e.g., vegetation-covered, non-vegetated, shadow-affected)
- ✅ Supports reproduction of the experimental pipeline described in the manuscript

---

### 1.2 Baseline YOLOv8-seg Implementation

We provide:
- The official **Ultralytics** source code (compressed package)
- A dataset configuration file (`.yaml`) that can be adapted to your local dataset path.  
  Together with a YOLOv8-seg model configuration (`.yaml`), users can directly train a baseline model on the released GFM subset.

**Example training command:**

```bash
yolo segment train \
  data=PATH/TO/GFM.yaml \
  model=PATH/TO/yolov8n-seg.yaml \
  imgsz=640 \
  epochs=500 \
  batch=4 \
  device=0
```
This enables direct reproduction of **YOLOv8-seg baseline** results on the released GFM subset.

---

### 1.3 FS-YOLO Components

We provide:
- **DSPP** module implementation
- **D-LKA** module implementation
- **FS-YOLO** model configuration (`.yaml`)
- Example configuration files for training

**Users can:**
1. Insert the provided **DSPP** and **D-LKA** modules into the Ultralytics framework  
2. Load the provided **FS-YOLO** model configuration  
3. Train and evaluate **FS-YOLO** on the released GFM subset  

> Note: A more user-friendly and fully integrated FS-YOLO codebase (including complete runnable scripts) will be released in the next update.

---

## 2. Reproducibility Statement

The currently released materials allow:
- Reproducing **YOLOv8-seg baseline** experiments
- Running **FS-YOLO** model variants
- Verifying segmentation improvements on the released GFM subset

All experimental pipelines described in the manuscript can be validated using the released subset and configuration files.

---

## 3. Full Dataset Release Plan

The full GFM dataset (including complete raw UAV imagery and full-scale annotations) is being finalized for structured release.

The following resources will be progressively released:
- Full GFM original annotation repository
- Detailed annotation specifications and labeling protocol
- MMDetection-compatible dataset version
- Dataset preprocessing scripts
- Pretrained model weights on GFM
- Complete FS-YOLO training framework and runnable scripts

**Expected timeline:** *prior to final publication / upon acceptance.*

Researchers requiring early access for review or academic purposes may contact the corresponding author.

---

## 4. Dataset Description (GFM)

The GFM dataset is a UAV-based ground fissure instance segmentation dataset collected in mining areas, featuring:
- High-resolution UAV orthophotos
- Pixel-level instance annotations
- Diverse backgrounds (vegetation-covered, non-vegetated, shadow-affected)
- Complex fissure morphologies

The dataset is specifically designed to support:
- Instance segmentation research
- Thin elongated object modeling
- Mining-induced ground fissure analysis

---

## 5. Citation

If you use this dataset or code, please cite:

> *[Paper citation will be updated upon publication.]*

---
