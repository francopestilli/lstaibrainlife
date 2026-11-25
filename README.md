# lstaibrainlife

<!-- brainlife-app:begin (generated from the App manifest; edit the manifest, not this block) -->

> **Segments multiple sclerosis white matter lesions from T1-weighted and FLAIR images with LST-AI and outputs lesion masks.**

Thin wrapper that runs the LST-AI command (lst --t1 --flair --output) without modifying it. Use it for MS lesion segmentation when you have T1w and FLAIR of the same subject. The main script reads inputs from config.json keys that do not match the registered keys and calls lst without a container, so the App may not run as registered.

| | |
|---|---|
| 📥 **Inputs** | `neuro/anat/t1w` · `neuro/anat/flair` |
| 📤 **Outputs** | `neuro/mask` · `raw` |
| 🔗 **Run it** | [doi.org/10.25663/brainlife.app.886](https://doi.org/10.25663/brainlife.app.886) |

#### 📥 Inputs

| Input | Datatype | Required | Description |
|---|---|---|---|
| `T1_input` | `neuro/anat/t1w` | yes | T1-weighted MRI |
| `FLAIR_input` | `neuro/anat/flair` | yes | FLAIR MRI |

#### 📤 Outputs

| Output | Datatype | Description |
|---|---|---|
| `masks` | `neuro/mask` | LST-AI segmentation masks (annotated and unannotated) |
| `stats` | `raw` |  |

<!-- brainlife-app:end -->

creating an LST-AI Brainlife.io app for neuroimaging 

This repository contains a simple Brainlife wrapper for running **LST-AI**  
(MS lesion segmentation using T1 + FLAIR MRI)

The scientific code for LST-AI is developed here:  
https://github.com/CompImg/LST-AI  
This wrapper does **not** modify LST-AI — it only provides Brainlife integration.

## Inputs

- T1-weighted image (.nii.gz)  
- FLAIR image (.nii.gz)

- ## Outputs

- LST-AI lesion segmentation and related output files
