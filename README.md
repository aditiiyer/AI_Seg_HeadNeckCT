# CT Swallowing & Chewing Structures — DeepLabV3 Auto-Segmentation

[![License: LGPL v3](https://img.shields.io/badge/License-LGPL_v3-blue.svg)](https://www.gnu.org/licenses/lgpl-3.0)
[![DOI](https://img.shields.io/badge/DOI-10.1088%2F1361--6560%2Fac4000-green)](https://doi.org/10.1088/1361-6560/ac4000)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cerr/CT_SwallowingAndChewing_DeepLabV3/blob/master/demo_DLseg_swallowing_and_chewing_structures.ipynb)
[![GitHub Stars](https://img.shields.io/github/stars/cerr/CT_SwallowingAndChewing_DeepLabV3?style=social)](https://github.com/cerr/CT_SwallowingAndChewing_DeepLabV3/stargazers)

---

Deep learning ensemble model for automated CT segmentation of **six swallowing and chewing structures** relevant to head & neck radiation therapy planning and dysphagia toxicity research:

| Organ | Risk |
|---|---|
| Masseter (left & right) | Chewing — mandibular function |
| Medial pterygoid (left & right) | Chewing — trismus risk |
| Larynx | Swallowing — aspiration risk |
| Pharyngeal constrictor muscle | Swallowing — dysphagia risk |

Validated prospectively ([*Physics in Medicine & Biology, 2022*])(https://iopscience.iop.org/article/10.1088/1361-6560/ac4000). Part of the [CERR](https://github.com/cerr/CERR) deep-learning model library.

---

## Quick start

The fastest way to run the model is via the interactive Colab demo — no local install required.

**[▶ Open demo notebook in Google Colab](https://colab.research.google.com/github/cerr/pycerr-notebooks/blob/main/autosegment_CT_HeadAndNeck_OARs.ipynb)**

The notebook walks through:
1. Environment setup (conda + pyCERR dependencies)
2. Loading a sample CT scan
3. Running inference with the pre-trained model
4. Visualizing and exporting the resulting RT structure set

---

## Local installation

### Requirements

- Python 3.7+
- The [pyCERR package](https://github.com/cerr/CERR)
- CUDA-capable GPU (recommended; CPU inference is supported but slow)

Produces NIfTI/DICOM RTSTRUCT segmentations.

---

## Repository structure

```
CT_SwallowingAndChewing_DeepLabV3/
├── model/                  # Pre-trained model weights
├── model_wrapper/          # Python inference wrapper
├── recipe/                 # Container recipe (Singularity/Docker)
├── environment.yml         # Conda environment specification
└── demo_DLseg_swallowing_and_chewing_structures.ipynb  # Demo notebook
```

---

## Citation

If you use this model in your research, please cite both of the following:

```bibtex
@article{iyer2022swallowing,
  title   = {Prospectively-validated deep learning model for segmenting
             swallowing and chewing structures in CT},
  author  = {Iyer, Aditi and Thor, Maria and Onochie, Ifeoma and Hesse,
             Joshua and Zakeri, Kaveh and LoCastro, Eve and Jiang, Jue and
             Veeraraghavan, Harini and Elguindi, Sharif and Lee, Nancy Y.
             and Deasy, Joseph O. and Apte, Aditya P.},
  journal = {Physics in Medicine \& Biology},
  volume  = {67},
  number  = {2},
  pages   = {024001},
  year    = {2022},
  doi     = {10.1088/1361-6560/ac4000}
}

@article{apte2020cerr,
  title   = {Library of deep-learning image segmentation and outcomes
             model-implementations},
  author  = {Apte, Aditya P. and Iyer, Aditi and Thor, Maria and others},
  journal = {Physica Medica},
  volume  = {73},
  pages   = {190--196},
  year    = {2020},
  doi     = {10.1016/j.ejmp.2020.04.011}
}
```

---

## License

```
This codebase uses the GNU-GPL copyleft license (https://www.gnu.org/licenses/lgpl3.0.en.html) to allow open-source distribution with additional restrictions. The license retains the ability to propagate any changes to the codebase back to the opensource community along with the following restrictions (i) No Clinical Use, (ii) No Commercial Use, and (iii) Dual Licensing which reserve the right to diverge and/or modify and/or expand the model implementations library to have a closed source/proprietary version along with the open source version in future. It should be noted that the segmentation models are distributed strictly for research use. Clinical or commercial use is prohibited. CERR and containerized model implementations have not been approved by the U.S. Food and Drug Administration (FDA). The library merely provides implementations of the developed models, whereas the creators of models retain the copyright to their work.
```

---

## Acknowledgements

Developed at Memorial Sloan Kettering Cancer Center. Supported by NIH/NCI.
