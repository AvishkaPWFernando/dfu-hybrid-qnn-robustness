# Robustness Analysis of Hybrid Quantum-Classical Deep Learning for Diabetic Foot Ulcer Classification Under NISQ-Inspired Noise

This repository contains code, notebooks, figures and reproducibility materials for the manuscript:

**Robustness Analysis of Hybrid Quantum-Classical Deep Learning for Diabetic Foot Ulcer Classification Under NISQ-Inspired Noise**

The study evaluates hybrid quantum-classical deep learning models for binary diabetic foot ulcer patch classification under ideal and simulated noisy quantum conditions. The work is framed as an academic simulator-based robustness analysis, not as a clinically deployable diagnostic system and not as a claim of quantum advantage.

## Repository status

This repository is provided to support manuscript reproducibility and review. It contains the main experimental notebooks and supporting artefacts used for the submitted study. The repository may be updated with additional reproducibility improvements.

## Model tracks

The study evaluates five experimental tracks:

1. Baseline hybrid ResNet18-VQC model.
2. ResNet50 fusion hybrid model.
3. Ideal versus noise-aware QTL-style hybrid model.
4. Classical baseline versus hybrid fusion comparison.
5. Robustness sweep across fusion and QTL-like hybrid families under simulated quantum noise.

## Dataset

The raw diabetic foot ulcer image dataset is **not redistributed** in this repository. Users should obtain the dataset from the original public dataset source described in the manuscript.

Expected dataset structure:

```text
dataset/
├── Normal/
└── Abnormal/
```

All experiments use binary patch classification:

* Normal: healthy skin patches
* Abnormal: diabetic foot ulcer patches

## Reproducibility notes

The experiments were implemented using Python, PyTorch, Torchvision, PennyLane, NumPy, scikit-learn and Matplotlib in Google Colab GPU environments.

A fixed random seed of 42 was used where supported. The dataset split followed a stratified train, validation and test protocol as described in the manuscript.

Due to differences between Colab runtimes and GPU availability, exact runtime-level reproduction may vary. The repository is intended to support transparent inspection of the experimental workflow, model configurations, evaluation protocol and reported results.

## Statistical testing note

The current manuscript reports aggregate metrics, confusion matrices, ROC-AUC, F1-score and robustness summaries. Statistical testing such as bootstrap confidence intervals and McNemar’s test requires per-sample prediction exports containing:

```text
test_sample_index, image_path_or_hash, y_true, y_pred, y_prob, threshold, model_name, condition
```

Where available, prediction exports should be placed in:

```text
results/prediction_exports/
```

## Clinical validity statement

This work provides internally valid simulator-based evidence under the evaluated dataset split, preprocessing pipeline, model configurations and simulated quantum-noise settings. External clinical validity is not established because no independent dataset, patient-level split, prospective clinical evaluation or real-world clinical workflow validation was performed.

## Authors

Avishka Pramuditha Warnakulasuriya Fernando
Staffordshire University London, United Kingdom
w022401o@student.staffs.ac.uk

Dr. Behrad Vakili
King’s College London, United Kingdom
behrad.vakili@kcl.ac.uk

Dr. Mahsa Zolfaghari
Staffordshire University London, United Kingdom
mahsa.zolfaghari@staffs.ac.uk

## Citation

If you use this repository, please cite the associated manuscript once available.

## Licence

This repository is released under the MIT Licence for research-code reuse. The dataset is not included and remains subject to its original licence and terms of use.

