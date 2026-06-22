# Aggregate Metrics and Result Artefacts

This folder contains aggregate result artefacts for the five model tracks reported in the manuscript:

**Robustness Analysis of Hybrid Quantum-Classical Deep Learning for Diabetic Foot Ulcer Classification Under NISQ-Inspired Noise**

## Contents

| File          | Description                                                                                                                                                            |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Model_1.zip` | Result artefacts for the baseline hybrid ResNet18-VQC model, including available curves, confusion matrix, ROC output and logs.                                        |
| `Model_2.zip` | Result artefacts for the ResNet50 fusion hybrid model, including available metrics, classification report, confusion matrix and training curves.                       |
| `Model_3.zip` | Result artefacts for the ideal versus noise-aware QTL-style hybrid model, including ideal/noise-aware comparison outputs, confusion matrices, ROC comparison and logs. |
| `Model_4.zip` | Result artefacts for the classical baseline versus hybrid fusion comparison, including classical, ideal fusion and noisy fusion outputs.                               |
| `Model_5.zip` | Result artefacts for the robustness sweep, including summary CSV files, robustness plots, heatmaps and ranked run tables.                                              |

## Purpose

These files are included to support transparency of the reported aggregate metrics, figures and robustness findings. They provide supporting evidence for the manuscript results but do not contain the raw image dataset.

## Statistical testing note

These aggregate artefacts are not sufficient by themselves for paired statistical testing such as McNemar's test or bootstrap confidence intervals.

For statistical testing, per-sample prediction exports are required with fields such as:

```text
test_sample_index, image_path_or_hash, y_true, y_pred, y_prob, threshold, model_name, condition
```

If generated, those files should be stored separately in:

```text
results/prediction_exports/
```

## Data privacy and dataset note

The raw diabetic foot ulcer image dataset is not redistributed in this repository. The dataset remains subject to its original licence and terms of use.
