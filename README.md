## VFM and VLFM for 3D CT scans

[VFM and VLFM for 3D CT scans](https://github.com/YuanshengZhang/VFM-VLM-for-3D-CT/) is a repository that includes:

* the latest publicly available Vision Foundation Models (VFMs) and Vision-Language Foundation Models (VLFMs) specifically designed for 3D Computed Tomography (CT);
* the latest publicly available 3D CT dataset;
* the overview of metrics employed for evaluating VFM and VLFM;


### The list of medical VFMs for 3D CT

| Model | Vision Encoder | Pretraining Data | Downstream task | Paper | Code | Year |
|------|------|------|------|------|------|------|
| CT-FM | SegResNet37 encoder | 150K 3D CT | whole-body and tumor  segmentation, head CT triage, medical image retrieval, and semantic understanding | [Pai et al.](https://www.nature.com/articles/s41467-025-62385-7) | [GitHub](https://aim.hms.harvard.edu/ct-fm) |2025|
| Foundation model for cancer imaging biomarkers | 3D ResNet50 | 11,467 annotated CT lesions identified from 2,312 unique patients | site classification, nodule malignancy prediction, NSCLC prognostication | [Pai et al.](https://www.nature.com/articles/s42256-024-00807-9) | [GitHub](https://github. com/AIM-Harvard/foundation-cancer-image-biomarker) |2024|



### The list of medical VLFMs for 3D CT

| Model | Vision Encoder | Text Encoder | Pretraining Data | Downstream task | Paper | Code | Year |
|------|------|------|------|------|------|------|
| RadFM | 3D ViT | MedLLaMA-13B | 16M 2D+3D multimodal | diagnosis, visual question answering, report generation | [Wu et al.](https://www.nature.com/articles/s41467-025-62385-7) | [GitHub](https://github.com/chaoyi-wu/RadFM) |2025|
| M3D | 3D ViT | LLaMA-2 | 120K 3D CT | image-text retrieval, report generation, visual question answering, positioning, and segmentation | [Bai et al.](http://arxiv.org/abs/2404.00578) | [GitHub](https://github.com/BAAIDCAI/M3D) |2024|
| Merlin | 3D ResNet152 | Clinical-Longfornmer | 14K 3D abdominal CT | zero-shot classification, phenotype classification, and zero-shot cross-modal retrieval, disease prediction, radiology report generation, and 3D segmentation | [Blankemeier et al.](http://arxiv.org/abs/2406.06512) | [GitHub](https://github.com/StanfordMIMI/Merlin) |2024|
| CT-CHAT | 3D CT-ViT | CXR-Bert | 26K 3D chest CT | multi-abnormality detection, case retrieval | [Hamamci et al.](http://arxiv.org/abs/2403.17834); [Hamamci et al.](https://link.springer.com/10.1007/978-3-031-72986-7) | [GitHub](https://github.com/ibrahimethemhamamci/CT-CLIP) |2024|



### The list of 3D CT Datasets

| Dataset | Anatomical Targets | Image-Text pairs | QA pairs | Paper | Link |
|------|------|------|------|------|------|
| CT-ORG | 140 CT scans containing six organ classes: liver, lungs, bladder, kidney, bones and brain | - | - | [Rister et al.]([https://link.springer.com/chapter/10.1007/978-3-030-01364-6_20](https://www.nature.com/articles/s41597-020-00715-8) | [Data](https://www.cancerimagingarchive.net/collection/ct-org/) |
| CT-RATE | 25,692 non-contrast 3D chest CT scans from 21,304 unique patients | + | + | [Hamamci et al.](http://arxiv.org/abs/2403.17834); [Hamamci et al.](https://link.springer.com/10.1007/978-3-031-72986-7) | [GitHub](https://github.com/ibrahimethemhamamci/CT-CLIP) | [Data](https://huggingface.co/datasets/ibrahimhamamci/CT-RATE) |
