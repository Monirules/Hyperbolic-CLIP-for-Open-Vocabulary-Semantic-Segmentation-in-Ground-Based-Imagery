# Hyperbolic CLIP for Open-Vocabulary Semantic Segmentation in Ground-Based Cloud Imagery

This project introduces a novel approach to **Open-Vocabulary Semantic Segmentation (OVSS)** by combining the zero-shot power of the **CLIP** vision-language model with **hyperbolic geometry**, applied specifically to **Ground-Based Cloud Imagery**.

---

## 💡 Core Innovation: Hyperbolic CLIP (HyperCLIP)

The primary innovation addresses a common challenge in adapting CLIP for pixel-level tasks: maintaining text-image alignment during fine-tuning.

* **Hierarchical Alignment:** We propose mapping CLIP's feature representations into **hyperbolic space** (e.g., the Poincaré ball model). Hyperbolic geometry is inherently better suited for compactly modeling the **hierarchical relationships** found in semantic data (from coarse image concepts to fine-grained pixel details) than traditional Euclidean space.
* **Feature Granularity:** We utilize the concept of **hyperbolic radius**—which correlates with a feature's hierarchical level—to propose a fine-tuning strategy (similar to HyperCLIP) that strategically adjusts the text embeddings. This ensures better alignment with the granular, pixel-level features required for accurate segmentation of complex, open-set categories.

---

## ☁️ Application: Ground-Based Cloud Segmentation

The methodology is demonstrated on a challenging dataset of ground-based cloud images.

* **Baseline Architecture:** A **Fully Convolutional Neural Network (FCNN)** with a **U-NET** architecture is established as the segmentation base.
* **Initial Training:** A baseline is provided where the U-NET is trained for **one epoch** to confirm the data pipeline and basic architecture for cloud region segmentation from remotely sensed optical images.
* **Data Readiness:** The project includes robust scripts for **data reading and formatting**, designed to execute seamlessly on environments like **Google Colab**.

---

## ⚙️ Reproducibility and Next Steps

The repository serves as a validated starting point for advanced experimentation.

* **Current Status:** The current implementation is a **proof of concept** focusing on setting up the architecture and data flow.
* **Next Steps for Researchers:**
    * Modify the FCNN/U-NET architecture or integrate the full Hyperbolic CLIP layer.
    * Run the model for a **higher number of epochs** on dedicated compute resources for a significant increase in performance and accuracy.
    * Expand the model's capability to enable true **open-vocabulary** performance, allowing segmentation based on text prompts for specific cloud types (e.g., "cumulus," "cirrus," "stratus").

For full Dataset, Email me - mahmudislam2025@gmail.com 

## Sample Input with the respective mask
![alt text](https://github.com/Arunprakash-A/U-NET-based-Cloud-Segmentation/blob/main/images/img_mask.png "Sample Image")

## Segmented Cloud Region Prediction
![alt text](https://github.com/Arunprakash-A/U-NET-based-Cloud-Segmentation/blob/main/images/img_mask_pred.png "Predicted Cloud region")
