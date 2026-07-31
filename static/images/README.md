# SpatialQuery

**SpatialQuery: Closest-Instance Distance Reasoning in Indoor Scenes via BEV Visual Block Rendering and Uncertainty-Aware Chain-of-Thought Prompting**

**Authors:** Hai Nguyen, Tung Vu, Cong Tran  
**Institution:** Posts and Telecommunications Institute of Technology  
**Status:** Under Review

---

## Overview

SpatialQuery is a training-free framework for fine-grained metric spatial reasoning in indoor environments. It addresses the *Closest-Instance Distance Query* (CIDQ) task—identifying the closest instance among multiple candidates of the same object class from a single RGB image.

### Key Contributions

1. **SpatialQuery-1M** — A large-scale benchmark with over one million RGB-only CIDQ question-answer pairs with absolute metric ground truth across 200 diverse indoor scenes.

2. **Scene Cubifying via BEV Visual Block Rendering** — A plug-and-play module that back-projects tilt-corrected 3D centroids onto a canonical Bird's-Eye View canvas, rendering each detected instance as a uniformly sized, color-coded cuboid.

3. **Uncertainty-Aware Chain-of-Thought (UA-CoT) Prompting** — Embeds per-instance spatial uncertainty (quantified via MAD-RANSAC-filtered point-cloud standard deviation) directly into the VLM reasoning chain.

---

## Results

On SpatialQuery-1M with a **Qwen3-VL-8B** backbone (zero-shot, train-free):

| Metric | Score |
|---|---|
| 3D-MAE (↓) | **0.259 m** |
| Unc-Acc@0.3 m (↑) | **90.5%** |
| Proximity Classification Accuracy (↑) | **84.18%** |

---

## Project Page

This website is built based on the [Nerfies website](https://nerfies.github.io) template.

---

## Website License

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
