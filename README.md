## VFM and VLFM for 3D CT scans

[VFM and VLFM for 3D CT scans](https://github.com/YuanshengZhang/VFM-VLM-for-3D-CT/) is a repository that includes:

* the latest publicly available Vision Foundation Models (VFMs) and Vision-Language Foundation Models (VLFMs) specifically designed for 3D Computed Tomography (CT);
* the latest publicly available 3D CT dataset;
* the overview of metrics employed for evaluating VFM and VLFM;


### memo: The list of medical VFMs for 3D CT

| Model | Vision Encoder | Pretraining Data | Downstream task | Paper | Code | Year |
|------|------|------|------|------|------|------|
| CT-FM | SegResNet37 encoder | 150K 3D CT | whole-body and tumor  segmentation, head CT triage, medical image retrieval, and semantic understanding | [Pai et al.](https://www.nature.com/articles/s41467-025-62385-7) | [GitHub](https://aim.hms.harvard.edu/ct-fm) |2025|
| Foundation model for cancer imaging biomarkers | 3D ResNet50 | 11,467 annotated CT lesions identified from 2,312 unique patients | site classification, nodule malignancy prediction, NSCLC prognostication | [Pai et al.](https://www.nature.com/articles/s42256-024-00807-9) | [GitHub](https://github.com/AIM-Harvard/foundation-cancer-image-biomarker) |2024|
| DeSD | 3D ResNet50 | 11K |  | [Ye et al.](https://link.springer.com/chapter/10.1007/978-3-031-16440-8_52) | [GitHub](https://github.com/yeerwen/DeSD) |2022|


### memo: The list of medical VLFMs for 3D CT

| Model | Vision Encoder | Text Encoder | Pretraining Data | Downstream task | Paper | Code | Year |
|------|------|------|------|------|------|------|------|
| RadFM | 3D ViT | MedLLaMA-13B | 16M 2D+3D image-text pairs (MedMD) | diagnosis, visual question answering, report generation | [Wu et al.](https://www.nature.com/articles/s41467-025-62385-7) | [GitHub](https://github.com/chaoyi-wu/RadFM) |2025|
| M3D | 3D ViT | LLaMA-2 | 120K 3D CT | image-text retrieval, report generation, visual question answering, positioning, and segmentation | [Bai et al.](http://arxiv.org/abs/2404.00578) | [GitHub](https://github.com/BAAIDCAI/M3D) |2024|
| Merlin | 3D ResNet152 | Clinical-Longfornmer | 14K 3D abdominal CT | classification, cross-modal retrieval, disease prediction, radiology report generation, and 3D segmentation | [Blankemeier et al.](http://arxiv.org/abs/2406.06512) | [GitHub](https://github.com/StanfordMIMI/Merlin) |2024|
| CT-CHAT | 3D CT-ViT | CXR-Bert | 26K 3D chest CT | multi-abnormality detection, case retrieval | [Hamamci et al.](http://arxiv.org/abs/2403.17834); [Hamamci et al.](https://link.springer.com/10.1007/978-3-031-72986-7) | [GitHub](https://github.com/ibrahimethemhamamci/CT-CLIP) |2024|
| M3FM | 3D CT-ViT | Transformer | 49 clinical data types, 163,725 chest CT series, and 17 tasks involved in LCS | detection, characterization, diagnosis, mortality risk prediction, chest abnormality exams | [Niu et al.](https://doi.org/10.1038/s41467-025-56822-w) | [GitHub](https://github.com/niuchuangnn/M3FM) |2025|
| Med-2E3 | M3D-CLIP | Phi-3 | M3D-Cap and M3D-VQA. The dataset includes over 120K CT volumes with corresponding 115K caption and 420K VQA annotations | report generation, medical visual question answering (VQA) | [Shi et al.](http://arxiv.org/abs/2411.12783) | [GitHub](https://github.com/MSIIP/Med-2E3) |2024|
| 3D-CT-GPT | 3D CT-ViT encoder from CT-CLIP | linear projection layer like LLaVA | 25K chest CT scans from CT-RATE, 2K chest CT scans from Dataset-XY | generating radiology reports from 3D chest CT scans | [Chen et al.](http://arxiv.org/abs/2409.19330) | [GitHub](-) |2024|
| E3D-GPT | 3D MAE | GPT-4 | BIMCV-R, which contains 7K 3D CT image-report pairs, and CTRATE, which includes 47K 3D CT image-report pairs | report generation, visual question answering, and disease diagnosis | [Lai et al.](https://arxiv.org/abs/2410.14200) | [GitHub](-) |2024|
| Medical Continual Self-Supervised (MedCoSS) | plain ViT/B | BERT | 356K X-ray from MIMIC-CXR, 10K CT from DeepLesion, 4K MRI from ADNI, 217K Rath from TCGA | claaification, segmentation | [Ye et al.](http://arxiv.org/abs/2311.17597) | [GitHub](https://github.com/yeerwen/MedCoSS) |2025|


### memo: The list of 3D CT Datasets

| Dataset | Anatomical Targets | Image-Text pairs | QA pairs | Paper | Link |
|------|------|------|------|------|------|
| CT-RATE | 25,692 non-contrast 3D chest CT scans from 21,304 unique patients | + | + | [Hamamci et al.](http://arxiv.org/abs/2403.17834); [Hamamci et al.](https://link.springer.com/10.1007/978-3-031-72986-7) | [Data](https://huggingface.co/datasets/ibrahimhamamci/CT-RATE) |
| RadGenome-Chest-CT | CT-RATE + interpretation (organ-level segmentation masks covering 197 categories) | + | + | [Zhang et al.](https://www.nature.com/articles/s41597-025-05922-9) | [Data](https://github.com/xiaoman-zhang/RadGenome-ChestCT) |
| OpenM3Chest | 128,693 CT scans (125K chest CT of 26K patients from NLST, 35K chest CT of 7K patients from MIDRC) | + | + | [Niu et al.](https://www.nature.com/articles/s41467-025-56822-w) | [Data](https://zenodo.org/records/14363994) |
| SAT-DS | 72 diverse publicly available medical segmentation datasets, totaling 22,186 scans including CT, MRI, and PET, and 302,033 segmentation annotations spanning 8 different regions of the human body: Brain, Head and Neck, Upper Limb, Thorax, Abdomen, Pelvis, and Lower Limb | - | - | [Zhao et al.](http://arxiv.org/abs/2312.17183) | [Data](https://github.com/zhaoziheng/SAT-DS) |
| BIMCV-R | 8,069 paired samples with more than 2M slices. More importantly, we engaged over 20 medical professionals to diagnose 1,475 of these samples, identifying 96 different diseases, including tumors, infectious diseases, cardiovascular diseases, and respiratory conditions | + | - | [Chen et al.](http://arxiv.org/abs/2403.15992) | [Data](https://huggingface.co/datasets/cyd0806/BIMCV-R) |
| TotalSegmentator | 1204 CT scans were used to segment 104 anatomic structures (27 organs, 59 bones, 10 muscles, and eight vessels) | - | - | [Wasserthal et al.](https://pubs.rsna.org/doi/full/10.1148/ryai.230024) | [Data](https://www.github.com/wasserth/TotalSegmentator)) |
| CT-ORG | 140 CT scans containing six organ classes: liver, lungs, bladder, kidney, bones and brain | - | - | [Rister et al.](https://www.nature.com/articles/s41597-020-00715-8) | [Data](https://www.cancerimagingarchive.net/collection/ct-org/) |
| Medical Segmentation Decathlon (MSD) | 750 brain, 30 heart, 201 liver, 394 hippocamppus, 48 prostate, 96 lung, 420 pancreas, 443 hepatic vessel, 61 spleen, 190 colon | - | - | [Simpson et al.](http://arxiv.org/abs/1902.09063) | [Data](http://medicaldecathlon.com/) |
| M3D-Seg | 5,772 labeled 3D CTs from 25 public datasets | - | - | [Bai et al.](http://arxiv.org/abs/2404.00578) | [Data](https://huggingface.co/datasets/GoodBaiBai88/M3D-Seg) |
| RadChestCT | 36,316 chest CT volumes from 19,993 unique patients | - | - | [Draelos et al.](https://doi.org/10.1016/j.media.2020.101857) | [Data](https://cvit.duke.edu/resource/rad-chestct-dataset/) |
| CC-CCII | 617,775 CT images from 4,154 patients (A subset: 361,221 CT images from 2,246 patients including 752 NCP patients, 797 common pneumonia patients, and 697 normal control patients) | - | - | [Zhang et al.](https://doi.org/10.1016/j.cell.2020.04.045) | [Data](http://ncov-ai.big.ac.cn/download?lang=en) |
| RICORD | 120 Chest CT scans | - | - | [Tsai et al.](https://doi.org/10.1148/radiol.2021203957) | [Data](https://www.cancerimagingarchive.net/collection/midrc-ricord-1a/) |


### memo: The list of evaluation metrics of VFM and VLFM

| Metrics | Full names | Description | Use Case |
|------|------|------|------|
| BLEU | BiLingual Evaluation Understudy | N-gram overlap for text similarity. the accuracy of the report generation result. | General VQA evaluation. |
| ROUGE | Recall-Oriented Understudy for Gisting Evaluation | a set of evaluation measures that assess the overlap between a generated summary and a set of reference summaries. | Long medical descriptions. |
| METEOR | Metric for Evaluation of Translation with Explicit ORdering | a more linguistically informed and recall-focused metric that excels at sentence-level evaluations and captures more flexible language use. an evaluation metric for machine translation that improves over traditional metrics like BLEU by incorporating linguistic features such as synonymy, stemming, and word order, and placing more emphasis on recall to better align with human judgments of translation quality. | machine translation, text summarization, paraphrase detection |
| BERTScore | BERT similarity score, BERT-F1 score | Semantic similarity using BERT embeddings. It measures the similarity between the generated report and the reference report using contextualized word embeddings provided by the BERT model | Semantic relevance in medical text. |
| CheXpert Labeler | | Rule-based pathology detection. | Chest X-ray report evaluation. |
| RadGraph | RadGraph F1 | Graph-based entity-relationship evaluation. an automatic metric that computes the overlap in clinical entities and relations between a model-generated report and a radiologist-generated report | Radiology report accuracy. |
| RadCliQ | | RadCliQ predicts a radiologist-determined error score from a combination of automated metrics, including BLEU, BERTScore, CheXbert vector similarity, and RadGraph. |
| Hit Score | | The Hit Score is a specific metric designed for evaluating abnormalities. It compares the model’s prediction with the ground truth. If the model’s prediction matches any abnormality specified in the ground truth, the score is set to 1; otherwise, it is 0. The overall score is then calculated as the average of these individual scores. |
| Clinical Correctness Score | | Expert evaluation of diagnostic accuracy. | Clinical report validation. |
