# Notebooks

This folder contains the implementation notebooks for the five experimental model tracks reported in the manuscript:

**Robustness Analysis of Hybrid Quantum-Classical Deep Learning for Diabetic Foot Ulcer Classification Under NISQ-Inspired Noise**

## Contents

| File            | Description                                                                                      |
| --------------- | ------------------------------------------------------------------------------------------------ |
| `Model_1.ipynb` | Baseline hybrid ResNet18-VQC model.                                                              |
| `Model_2.ipynb` | ResNet50 fusion hybrid model.                                                                    |
| `Model_3.zip`   | Compressed notebook archive for the ideal versus noise-aware QTL-style hybrid model.             |
| `Model_4.zip`   | Compressed notebook archive for the classical baseline versus hybrid fusion comparison.          |
| `Model_5.zip`   | Compressed notebook archive for the robustness sweep across fusion and QTL-like hybrid families. |

## Why some notebooks are zipped

Models 3-5 are provided as compressed notebook archives because the full notebooks contain large outputs and may exceed GitHub browser preview limits. Users can download and extract the ZIP files to inspect or run the notebooks locally.

## Dataset note

The raw diabetic foot ulcer image dataset is not included in this repository. Users should obtain the dataset from the original public source described in the manuscript and organise it according to the instructions in `docs/dataset_instructions.md`.

## Reproducibility note

The notebooks are provided to support transparency and reproducibility of the experimental workflow. Exact reruns may vary depending on Google Colab runtime, GPU availability, package versions and random-seed behaviour.

The experiments are intended for academic simulator-based robustness analysis only. They are not a clinically deployable diagnostic system and do not claim quantum advantage.
