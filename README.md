# Vehicle Damage Classification Using Deep Learning

**Course:** COMP-671 Deep Learning, Rivier University  
**Student:** Anjali Tummala

## Project overview

This project classifies vehicle damage images into seven categories using a baseline convolutional neural network (CNN) and ImageNet-pretrained ResNet50 models, with and without data augmentation.

## Dataset

The experiment used 963 labeled images: 674 training, 144 validation, and 145 held-out test images. Categories: `bumper_dent`, `bumper_scratch`, `door_dent`, `door_scratch`, `glass_shatter`, `head_lamp`, and `tail_lamp`.

The original dataset source and license must be verified and cited before publishing the dataset. The original archive is not included in this README.

## Recorded results

| Model | Test accuracy |
|---|---:|
| Baseline CNN | 42.07% |
| ResNet50 without augmentation | 77.93% |
| ResNet50 with augmentation | 78.62% |

For the augmented ResNet50, the recorded test loss was 0.5573, macro precision 0.81, macro recall 0.78, and macro F1 0.78. The model correctly classified 114 of 145 test images. These are recorded results from the accompanying notebook and evaluation files, not independently reproduced here.

**Interpretation caution:** The ResNet50 experiments used different training settings, including learning rates, so the 0.69-percentage-point difference does not isolate the effect of augmentation.

## Project files

- `Vehicle_Damage_Classification.ipynb` — Colab experiment notebook (rename the uploaded notebook before committing).
- `Vehicle_Damage_Classification_Final_Report.pdf` — final academic report.
- `results/` — comparison plots, classification report, confusion matrix, and failure-analysis figures, when included.

Trained `.keras` and `.h5` model files and the dataset archive are stored separately in Google Drive; they are not necessary to include in the GitHub repository.

## Environment and reproducibility

The notebook uses Google Colab, TensorFlow/Keras, NumPy, pandas, scikit-learn, and Matplotlib. Image inputs are resized to 224 × 224 pixels. Dataset splits use stratification and a random seed of 42.

**Important:** The submitted notebook records multiple Colab sessions and recovery steps, with paths specific to the author's Google Drive. It is not yet a verified one-click, run-all pipeline. To reproduce, obtain the appropriately licensed dataset, update the Drive/data paths, and execute the relevant setup and model sections in order.

## Limitations

The dataset is relatively small; visually similar damage categories are sometimes confused. The study uses a single test split and does not establish the causal effect of augmentation.

## References

- He, K., Zhang, X., Ren, S., & Sun, J. (2016). *Deep Residual Learning for Image Recognition*. CVPR. https://arxiv.org/abs/1512.03385
- TensorFlow/Keras documentation: https://www.tensorflow.org/
- Dataset source: **To be confirmed and cited.**


## Submission files

- `Vehicle_Damage_Classification_Clean.ipynb` — organized notebook with no automatic retraining.
- `results/` — recorded experiment tables and figures.
- `Vehicle_Damage_Classification_Final_Report.pdf` — final report.

The original training notebook is kept as a separate backup; the clean notebook preserves experimental outcomes but is not an exact replacement for training logs. Dataset ZIP and trained model weights are intentionally excluded from this GitHub bundle. Add dataset provenance/license before publishing data.
