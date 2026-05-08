# Geospatial Foundation Models

Curated catalog of geospatial, Earth-observation, remote-sensing, weather/climate, and geospatial vision-language foundation models.

Last updated: 2026-05-08.

Scope note: "Geospatial foundation model" is used inconsistently in the literature. This file includes models explicitly described as foundation models, plus widely used FM-adjacent remote-sensing pretraining systems that serve the same role in downstream EO workflows.

Availability audit, 2026-05-08:

- Checked 169 unique GitHub and Hugging Face URLs referenced in this file.
- Result: 169/169 returned reachable HTTP status codes at audit time.
- Hugging Face model API verified for the major open model IDs listed in the table below.
- This is an availability check, not a reproducibility check. "Reachable" means the page/model card exists; it does not mean weights load locally or inference has been reproduced.

| Model | Hugging Face ID | API status | Downloads at audit | Likes at audit |
| --- | --- | --- | ---: | ---: |
| Prithvi-EO-2.0 300M | `ibm-nasa-geospatial/Prithvi-EO-2.0-300M` | reachable | 13443 | 40 |
| Clay | `made-with-clay/Clay` | reachable | 173 | 54 |
| TerraMind base | `ibm-esa-geospatial/TerraMind-1.0-base` | reachable | 20756 | 47 |
| TerraMind large | `ibm-esa-geospatial/TerraMind-1.0-large` | reachable | 1565 | 15 |
| OlmoEarth base | `allenai/OlmoEarth-v1-Base` | reachable | 12154 | 24 |
| SatlasPretrain | `allenai/satlas-pretrain` | reachable | 0 | 20 |
| DOFA | `earthflow/DOFA` | reachable | 0 | 21 |
| Prithvi WxC 2.3B | `ibm-nasa-geospatial/Prithvi-WxC-1.0-2300M` | reachable | 200 | 82 |
| Prithvi WxC gravity-wave | `ibm-nasa-geospatial/Prithvi-WxC-1.0-2300m-gravity-wave-parameterization` | reachable | 19 | 10 |
| ViTP | `GreatBird/ViTP` | reachable | 0 | 3 |
| SARCLIP ViT-L/14 | `BiliSakura/SARCLIP-ViT-L-14` | reachable | 7 | 0 |

---

## 1. Core Earth Observation / Remote Sensing Foundation Models

### Prithvi-EO-1.0 / Prithvi-EO-2.0
- Organization: IBM, NASA, Jülich Supercomputing Centre
- Modalities: optical / multispectral, HLS, Sentinel-2 / Landsat-derived workflows
- Tasks: segmentation, classification, regression, downstream EO fine-tuning
- Notes: One of the most important open EO foundation model families; Prithvi-EO-2.0 adds stronger multi-temporal capabilities.
- Paper: https://arxiv.org/abs/2412.02732
- GitHub: https://github.com/NASA-IMPACT/Prithvi-EO-2.0
- Hugging Face: https://huggingface.co/ibm-nasa-geospatial/Prithvi-EO-2.0-300M
- IBM blog: https://research.ibm.com/blog/prithvi2-geospatial

### Clay
- Organization: Clay Foundation / Development Seed ecosystem
- Modalities: multisensor EO, including Sentinel-2, Landsat, Sentinel-1 SAR, NAIP, MODIS, LINZ
- Tasks: embeddings, classification, regression, segmentation, downstream adaptation
- Notes: Open Earth foundation model focused on practical embeddings and use across heterogeneous sensors.
- Project: https://clay-foundation.github.io/model/
- GitHub: https://github.com/Clay-foundation/model
- Hugging Face: https://huggingface.co/made-with-clay/Clay
- Development Seed: https://developmentseed.org/projects/clay/

### TerraMind 1.0
- Organization: IBM, ESA Phi-lab, Jülich
- Modalities: Sentinel-1, Sentinel-2, DEM, NDVI, land-cover layers, other EO modalities
- Tasks: multimodal prediction, generation, reconstruction, segmentation/classification adaptation
- Notes: Multimodal any-to-any EO foundation model.
- Project: https://ibm.github.io/terramind/
- GitHub: https://github.com/IBM/terramind
- Hugging Face base: https://huggingface.co/ibm-esa-geospatial/TerraMind-1.0-base
- Hugging Face large: https://huggingface.co/ibm-esa-geospatial/TerraMind-1.0-large
- ESA: https://www.esa.int/Applications/Observing_the_Earth/ESA_and_IBM_collaborate_on_TerraMind

### OlmoEarth
- Organization: Allen Institute for AI
- Modalities: Sentinel-1, Sentinel-2, Landsat, image time series
- Tasks: embeddings, segmentation, fine-tuning, operational EO modeling
- Notes: Open multimodal/spatio-temporal EO foundation model family with code, weights, and platform tooling.
- Paper: https://arxiv.org/abs/2511.13655
- GitHub: https://github.com/allenai/olmoearth_pretrain
- Hugging Face base: https://huggingface.co/allenai/OlmoEarth-v1-Base
- Docs: https://docs.olmoearth.allenai.org/
- Ai2 blog: https://allenai-web-dev.allen.ai/blog/olmoearth-models

### AlphaEarth Foundations
- Organization: Google DeepMind / Google Earth
- Modalities: multimodal Earth observation signals; released primarily as satellite embedding data
- Tasks: global mapping, low-label classification/regression, embedding-based analysis
- Notes: Public access is centered on a satellite embedding dataset rather than a conventional downloadable model.
- Paper: https://arxiv.org/abs/2507.22291
- DeepMind announcement: https://deepmind.google/blog/alphaearth-foundations-helps-map-our-planet-in-unprecedented-detail/
- Google Earth blog: https://medium.com/google-earth/ai-powered-pixels-introducing-googles-satellite-embedding-dataset-31744c1f4650
- Google Earth AI: https://ai.google/earth-ai/

### Galileo
- Organization: NASA Harvest, McGill, Allen Institute for AI, Vector Institute collaborators
- Modalities: multimodal Earth observation
- Tasks: agriculture, crop mapping, EO representation learning, downstream fine-tuning
- Paper: https://proceedings.mlr.press/v267/tseng25a.html
- arXiv PDF: https://arxiv.org/pdf/2502.09356
- GitHub: https://github.com/nasaharvest/galileo
- Crop mapping repo: https://github.com/crop-type-mapping/FM/tree/main

### TerraFM
- Organization: MBZUAI Oryx
- Modalities: multisensor EO
- Tasks: unified multisensor Earth observation
- Notes: Scalable foundation model for unified multisensor EO.
- Paper: https://arxiv.org/abs/2506.06281
- GitHub: https://github.com/mbzuai-oryx/TerraFM

### SkySense
- Organization: Wuhan University / collaborators
- Modalities: multimodal remote sensing
- Tasks: scene classification, object detection, segmentation, change detection
- Notes: CVPR 2024 remote-sensing foundation model.
- Paper: https://arxiv.org/abs/2312.10115
- CVF: https://openaccess.thecvf.com/content/CVPR2024/papers/Guo_SkySense_A_Multi-Modal_Remote_Sensing_Foundation_Model_Towards_Universal_Interpretation_CVPR_2024_paper.pdf

### SkySense++
- Organization: Wuhan University / collaborators
- Modalities: multimodal remote sensing
- Tasks: diverse EO interpretation tasks
- Notes: Semantic-enhanced multimodal remote-sensing foundation model.
- Nature Machine Intelligence: https://www.nature.com/articles/s42256-025-01078-8
- GitHub: https://github.com/kang-wu/SkySensePlusPlus
- Pretraining data: https://zenodo.org/records/14994430

### SkySense V2
- Organization: SkySense team
- Modalities: multimodal remote sensing
- Tasks: remote sensing interpretation
- Paper: https://arxiv.org/html/2507.13812v1

### RingMo
- Organization: Aerospace Information Research Institute, CAS / collaborators
- Modalities: remote-sensing imagery
- Tasks: classification, detection, segmentation, downstream RS interpretation
- Notes: Early masked-image-modeling remote-sensing foundation model.
- Paper page: https://dblp.org/rec/journals/tgrs/SunWLZLHLRYCHYWLF23
- Overview: https://colab.ws/articles/10.1109%2Ftgrs.2022.3194732

### RingMo-lite
- Organization: RingMo ecosystem
- Modalities: remote-sensing imagery
- Tasks: lightweight multitask interpretation, on-orbit / efficient scenarios
- Paper: https://arxiv.org/abs/2309.09003

### RingMoE
- Organization: CAS / RingMo ecosystem
- Modalities: optical, SAR, multispectral, multimodal RS
- Tasks: classification, detection, segmentation, tracking, change detection, depth estimation
- Notes: Mixture-of-modality-experts RS foundation model; paper reports 14.7B parameters with pruning to smaller variants.
- Paper: https://arxiv.org/abs/2504.03166

### RingMo-Sense / RingMo-SenseV2
- Organization: RingMo ecosystem
- Modalities: multisource heterogeneous time-series data
- Tasks: spatiotemporal prediction
- Notes: Predictive foundation model for heterogeneous remote-sensing time series.
- RingMo-SenseV2: https://eurekamag.com/research/099/893/099893543.php

### SatMAE
- Organization: SustainLab / collaborators
- Modalities: temporal and multispectral satellite imagery
- Tasks: representation learning, classification, segmentation
- Notes: Important masked autoencoder baseline for satellite imagery.
- Paper: https://arxiv.org/abs/2207.08051
- Project: https://sustainlab-group.github.io/SatMAE/
- GitHub: https://github.com/sustainlab-group/SatMAE

### SatMAE++
- Organization: SatMAE++ authors
- Modalities: optical and multispectral satellite imagery
- Tasks: representation learning and downstream classification/segmentation
- Notes: CVPR 2024 extension with multi-scale pretraining.
- GitHub: https://github.com/techmn/satmae_pp

### Scale-MAE
- Organization: BAIR Climate Initiative / collaborators
- Modalities: remote-sensing imagery
- Tasks: scale-aware representation learning
- Notes: Scale-aware MAE for geospatial data; widely used as a GFM baseline.
- GitHub: https://github.com/bair-climate-initiative/scale-mae

### SatlasPretrain / SatlasNet
- Organization: Allen Institute for AI
- Modalities: Sentinel-2, Sentinel-1, Landsat 8/9, aerial imagery
- Tasks: satellite/aerial image understanding, segmentation, classification, detection-style heads
- Notes: Large-scale pretraining dataset and models for remote-sensing understanding.
- GitHub models: https://github.com/allenai/satlaspretrain_models
- GitHub dataset/code: https://github.com/allenai/satlas
- Hugging Face: https://huggingface.co/allenai/satlas-pretrain
- ICCV paper: https://openaccess.thecvf.com/content/ICCV2023/papers/Bastani_SatlasPretrain_A_Large-Scale_Dataset_for_Remote_Sensing_Image_Understanding_ICCV_2023_paper.pdf

### CROMA
- Organization: CROMA authors
- Modalities: optical multispectral and SAR
- Tasks: multimodal representations, classification, segmentation
- Notes: Contrastive radar-optical masked autoencoder; strong baseline in many GFM benchmarks.
- Paper: https://arxiv.org/abs/2311.00566
- GitHub: https://github.com/antofuller/CROMA
- Hugging Face paper page: https://huggingface.co/papers/2311.00566

### DOFA
- Organization: EarthFlow / Zhu Lab ecosystem
- Modalities: multiple EO modalities
- Tasks: unified multimodal remote sensing, downstream task adaptation
- Notes: Dynamic One-For-All model designed to handle different EO sensor modalities.
- Paper: https://arxiv.org/abs/2403.15356
- GitHub: https://github.com/zhu-xlab/DOFA
- Hugging Face: https://huggingface.co/earthflow/DOFA
- Esri integration: https://www.esri.com/arcgis-blog/products/arcgis-pro/geoai/use-remote-sensing-foundation-models-with-arcgis

### GFM / GeoPile
- Organization: Amazon Science / University collaborators
- Modalities: geospatial imagery from GeoPile
- Tasks: geospatial representation learning
- Notes: Continual pretraining approach for geospatial foundation models.
- Paper: https://huggingface.co/papers/2302.04476
- GitHub: https://github.com/boranhan/Geospatial_Foundation_Models
- Amazon Science PDF: https://assets.amazon.science/15/73/30fb418f4a4eae2fb556e9027ba9/towards-geospatial-foundation-models-via-continual-pretraining.pdf

### msGFM
- Organization: Amazon Science / collaborators
- Modalities: multisensor geospatial data
- Tasks: multisensor representation learning
- Notes: Extension from GFM toward multisensor geospatial foundation modeling.
- Paper PDF: https://arxiv.org/pdf/2404.01260
- Related repo: https://github.com/boranhan/Geospatial_Foundation_Models
- Amazon Science PDF: https://assets.amazon.science/0e/f6/589a77f4480da174f1e8df553bb6/bridging-remote-sensors-with-multisensor-geospatial-foundation-models.pdf

### AnySat
- Organization: AnySat authors
- Modalities: multimodal satellite and aerial imagery across resolutions
- Tasks: scale-adaptive EO representation learning
- Notes: JEPA-style scale-adaptive foundation model for Earth observation.
- GitHub: https://github.com/gastruc/AnySat
- DeepWiki overview: https://deepwiki.com/gastruc/AnySat/1-anysat-overview

### EarthPT
- Organization: EarthPT authors
- Modalities: Earth observation time series
- Tasks: autoregressive EO sequence modeling
- Notes: Time-series foundation model for Earth observation.
- Paper: https://arxiv.org/abs/2309.07207
- DBLP: https://dblp.org/rec/journals/corr/abs-2309-07207

### SatVision-TOA
- Organization: NASA / collaborators
- Modalities: MODIS L1B 14-band top-of-atmosphere radiance
- Tasks: coarse-resolution all-sky remote-sensing representation learning
- Notes: Addresses moderate/coarse-resolution all-sky imagery rather than cloud-free high-resolution scenes.
- Paper: https://huggingface.co/papers/2411.17000

### RobSense
- Organization: La Trobe University / collaborators
- Modalities: multispectral, SAR, static and temporal inputs
- Tasks: robust multimodal remote-sensing classification and segmentation
- Notes: Designed for missing bands, incomplete inputs, and temporal irregularity.
- Project: https://ikhado.github.io/robsense/
- CVF paper: https://openaccess.thecvf.com/content/CVPR2025/papers/Kha_RobSense_A_Robust_Multi-modal_Foundation_Model_for_Remote_Sensing_with_CVPR_2025_paper.pdf

### SatMamba
- Organization: SatMamba authors
- Modalities: remote-sensing imagery
- Tasks: foundation modeling with state-space models
- Notes: Mamba/state-space approach to remote-sensing pretraining.
- Paper: https://arxiv.org/abs/2502.00435
- GitHub: https://github.com/mdchuc/HRSFM

### CMID
- Organization: NJU-LHRS
- Modalities: remote-sensing imagery
- Tasks: self-supervised pretraining and downstream RS image understanding
- Notes: Unified SSL framework; often treated as an FM-adjacent remote-sensing pretraining baseline.
- Paper: https://arxiv.org/abs/2304.09670
- GitHub: https://github.com/NJU-LHRS/official-CMID

### Extended remote-sensing vision FM index

The entries below are included for coverage. They should be promoted to full model cards once metadata, code/weight availability, and reproducibility status are verified.

| Model | Focus |
| --- | --- |
| GeoKR | Geographical knowledge-driven RS representation learning |
| GASSL | Geography-aware self-supervised learning |
| SeCo | Seasonal contrastive pretraining for RS imagery |
| RSP | Empirical study / pretraining baseline for remote sensing |
| MATTER | Material and texture representation learning for RS tasks |
| DINO-MM | Joint SAR-optical self-supervised ViT representation learning |
| GeCo | Geographical supervision correction for RS representation learning |
| RS-BYOL | Invariant representations from multispectral and SAR images |
| CSPT | Consecutive pretraining strategy for RS transfer learning |
| RVSA | Plain ViT adaptation toward RS foundation modeling |
| DINO-MC | Global-local view alignment for RS self-supervised learning |
| Cross-Scale MAE | Multiscale masked autoencoding for remote sensing |
| USat | Unified self-supervised encoder for multisensor satellite imagery |
| AIEarth | Cloud platform / intelligent computing system for geospatial big data |
| GeRSP | Generic knowledge boosted pretraining for RS images |
| SMLFR | Generative ConvNet FM with sparse modeling and low-frequency reconstruction |
| U-BARN | Spatiotemporal representation learning for satellite image time series |
| SwiMDiff | Scene-wide matching contrastive learning with diffusion constraint |
| BFM | Billion-scale foundation model for remote sensing images |
| Hydro | Foundation model for water in satellite imagery |
| S2MAE | Spatial-spectral pretraining model for spectral RS data |
| MTP | Multitask pretraining for RS foundation models |
| RS-DFM | Distributed remote-sensing foundation model for diverse downstream tasks |
| OFA-Net | Unified foundation model direction for Earth vision |
| MM-VSF | Knowledge-guided multimodal foundation modeling for RS |
| LeMeViT | Efficient ViT with learnable meta tokens for RS interpretation |
| SAR-JEPA | Joint-embedding predictive architecture for SAR ATR |
| DeCUR | Decoupled common and unique multimodal self-supervision |
| MMEarth | Multimodal pretext tasks for geospatial representation learning |
| OmniSat | Self-supervised modality fusion for Earth observation |
| MA3E | Masked angle-aware autoencoder for RS images |
| SoftCon | Multilabel-guided soft contrastive EO pretraining |
| PIS | Intra-instance similarity pretraining for RS foundation models |
| FG-MAE | Feature-guided masked autoencoder for remote sensing |
| OReole-FM | Billion-parameter FM direction for high-resolution satellite imagery |
| A2-MAE | Spatial-temporal-spectral anchor-aware masked autoencoder |
| FoMo | Multimodal, multiscale, multitask FMs for forest monitoring |
| PIEViT | Pattern integration/enhancement ViT for RS SSL |
| SARATR-X | Foundation model for SAR target recognition |
| DynamicVis | Dynamic visual perception for efficient RS foundation models |
| SUMMIT | SAR foundation model with auxiliary-task-enhanced intrinsic characteristics |
| SenPa-MAE | Sensor-parameter-aware masked autoencoder for multisatellite pretraining |
| HyperSL | Spectral foundation model for hyperspectral image interpretation |
| TiMo | Spatiotemporal foundation model for satellite image time series |
| Panopticon | Any-sensor foundation model for Earth observation |
| HyperFree | Channel-adaptive/tuning-free hyperspectral FM |
| WV-Net | SAR WV-mode contrastive foundation model |
| DeepAndes | Multispectral RS foundation model for the Andes |
| RingMamba | Multisensor pretraining with visual state-space models |
| RingMo-Aerial | Aerial RS foundation model with affine transformation contrastive learning |
| SeaMo | Multiseasonal and multimodal RS foundation model |
| MoSAiC | Multimodal multilabel supervision-aware contrastive learning |
| CGEarthEye | High-resolution RS vision FM based on Jilin-1 constellation |
| CtxMIM | Context-enhanced masked image modeling for RS image understanding |
| ViTP | Visual instruction pretraining for domain-specific foundation models |
| FedSense | Privacy-preserved RSFM pretraining with federated mutual-guidance learning |
| Copernicus-FM | Unified Copernicus foundation model for Earth vision |
| SelectiveMAE | Efficient masked image modeling over massive satellite imagery |
| SMARTIES | Spectrum-aware multisensor autoencoder |
| RS-vHeat | Heat-conduction-guided efficient RS foundation model |
| RoMA | Mamba-based foundation model scaling for remote sensing |
| GeoLink | RSFM enhanced with OpenStreetMap data |
| CrossEarth | Domain-generalizable RS semantic segmentation FM |
| PhySwin | Efficient physically informed multispectral EO FM |
| FlexiMo | Flexible remote-sensing foundation model |
| MAPEX | Modality-aware pruning of experts for RSFMs |
| Complex-valued SAR FM | Physically inspired complex-valued SAR representation learning |
| MAESTRO | MAE for multimodal, multitemporal, multispectral EO |
| Alliance | Spectral-spatial-frequency awareness foundation model |
| THOR | EO foundation model for climate and society applications |
| AgriFM | Multisource temporal RS foundation model for agriculture mapping |
| CrossEarth-SAR | SAR-centric billion-scale geospatial FM |
| NeighborMAE | MAE exploiting spatial dependencies between neighboring EO images |
| MOMO | Mars orbital foundation model for Mars orbital applications |
| TESSERA | Temporal embeddings of surface spectra for Earth representation |
| RAMEN | Resolution-adjustable multimodal encoder for EO |
| SARMAE | Masked autoencoder for SAR representation learning |

---

## 2. Hyperspectral / Spectral Foundation Models

### SpectralGPT
- Organization: Danfeng Hong and collaborators
- Modalities: spectral / hyperspectral remote-sensing imagery
- Tasks: spectral scene understanding and downstream HSI tasks
- Notes: Purpose-built foundation model for spectral remote-sensing data.
- Paper: https://arxiv.org/abs/2311.07113
- GitHub: https://github.com/danfenghong/IEEE_TPAMI_SpectralGPT
- Zenodo: https://zenodo.org/records/8412377

### HyperSIGMA
- Organization: WHU-Sigma
- Modalities: hyperspectral imagery
- Tasks: hyperspectral interpretation
- Notes: Billion-level foundation model for HSI interpretation, pretrained on HyperGlobal-450K.
- GitHub: https://github.com/WHU-Sigma/HyperSIGMA

### Hyper-MAE / LESS ViT
- Organization: UIUC / collaborators
- Modalities: hyperspectral and multimodal geospatial data
- Tasks: hyperspectral geospatial representation learning
- Project: https://uiuctml.github.io/GeospatialFM/

### SpectralEarth
- Organization: SpectralEarth authors
- Modalities: EnMAP hyperspectral time series
- Tasks: hyperspectral pretraining and downstream land-cover / crop-type mapping
- Notes: Large-scale hyperspectral dataset and pretraining benchmark direction.
- Paper: https://arxiv.org/abs/2408.08447

### SIGMAE
- Organization: SIGMAE authors
- Modalities: multispectral remote sensing
- Tasks: spectral-index-guided multispectral representation learning
- Notes: 2026 multispectral FM; code/weights announced by authors.
- Paper: https://arxiv.org/abs/2603.07463
- GitHub: https://github.com/zxk688/SIGMAE

---

## 3. Remote-Sensing Vision-Language and Multimodal LLM Models

### GeoRSCLIP / RS5M
- Organization: OM AI Lab / collaborators
- Modalities: remote-sensing image-text pairs
- Tasks: zero-shot classification, text-image retrieval, semantic localization
- Paper: https://arxiv.org/abs/2306.11300
- GitHub: https://github.com/om-ai-lab/RS5M

### RemoteCLIP
- Modalities: remote-sensing image-text
- Tasks: remote-sensing vision-language representation learning
- Paper: https://arxiv.org/pdf/2306.11029

### LRSCLIP
- Modalities: remote-sensing image and long text
- Tasks: long-text remote-sensing vision-language learning
- Paper: https://arxiv.org/html/2503.19311v1

### DOFA-CLIP
- Organization: DOFA ecosystem
- Modalities: remote-sensing imagery and text
- Tasks: vision-language extension of DOFA
- GitHub: https://github.com/xiong-zhitong/DOFA-CLIP

### SAR-KnowLIP
- Modalities: SAR and language / knowledge-enhanced geospatial metadata
- Tasks: SAR multimodal foundation modeling
- Notes: Described as a universal SAR multimodal foundation model.
- Paper: https://arxiv.org/abs/2509.23927

### GeoChat
- Organization: MBZUAI Oryx
- Modalities: remote-sensing imagery and language
- Tasks: visual question answering, remote-sensing dialogue, referring/grounded understanding
- Paper: https://arxiv.org/abs/2311.15826
- Project: https://mbzuai-oryx.github.io/GeoChat/
- GitHub: https://github.com/mbzuai-oryx/GeoChat

### EarthGPT
- Modalities: remote-sensing imagery and language
- Tasks: multimodal EO reasoning and understanding
- Paper: https://arxiv.org/abs/2401.16822

### TEOChat
- Modalities: temporal Earth-observation imagery and language
- Tasks: temporal EO assistant / reasoning
- Paper: https://arxiv.org/html/2410.06234v1

### RingMo-Agent
- Organization: RingMo ecosystem
- Modalities: multiplatform, multimodal remote-sensing imagery and language
- Tasks: multimodal reasoning over RS images
- Paper: https://arxiv.org/abs/2507.20776

### DescribeEarth
- Organization: Earth Insights
- Modalities: remote-sensing imagery and language
- Tasks: remote-sensing image description
- GitHub org: https://github.com/earth-insights
- Repo: https://github.com/earth-insights/DescribeEarth

### SegEarth-R1 / SegEarth-R2 / SegEarth-OV
- Organization: Earth Insights
- Modalities: remote-sensing imagery and language
- Tasks: geospatial pixel reasoning, language-guided segmentation, open-vocabulary segmentation
- GitHub org: https://github.com/earth-insights
- SegEarth-R1: https://github.com/earth-insights/SegEarth-R1
- SegEarth-R2: https://github.com/earth-insights/SegEarth-R2
- SegEarth-OV-2: https://github.com/earth-insights/SegEarth-OV-2

### Extended remote-sensing vision-language / MLLM index

| Model | Focus |
| --- | --- |
| SkyCLIP | SkyScript-based RS vision-language pretraining |
| GRAFT | Ground remote alignment without manual annotations |
| EarthMarker | Visual prompting MLLM for remote sensing |
| RingMoGPT | Unified RS model for vision, language, and grounded tasks |
| RS-LLaVA | Captioning and VQA for remote-sensing imagery |
| SkySenseGPT | Fine-grained instruction tuning for RS VLMs |
| RSCLIP | Vision-language learning in RS without human annotations |
| GeoText | Spatial-relation matching for drones / geotext tasks |
| LHRS-Bot | VGI-enhanced multimodal RS assistant |
| GeoGround | Unified RS visual grounding model |
| RSUniVLM | Unified RS VLM with granularity-oriented mixture of experts |
| REO-VLM | VLM adaptation for EO regression tasks |
| UniRS | Multi-temporal RS tasks through VLMs |
| VHM | Versatile and honest RS VLM |
| Falcon | Remote-sensing vision-language foundation model |
| GeoRSMLLM | Multimodal LLM for geoscience and remote sensing |
| OmniGeo | Multimodal LLM direction for geospatial AI |
| DGTRS-CLIP | Dual-granularity RS image-text alignment |
| EagleVision | Object-level attribute MLLM for remote sensing |
| SkyEyeGPT | Instruction-tuned RS VLM |
| EarthGPT-X | Spatial MLLM for multilevel multisource RS imagery |
| LISAt | Language-instructed segmentation assistant for satellite imagery |
| DynamicVL | Dynamic city understanding with MLLMs |
| RSGPT | RS vision-language model and benchmark |
| LHRS-Bot-Nova | Improved RS multimodal assistant |
| EarthDial | Interactive dialogues from multisensory Earth observations |
| SkySense-O | Open-world RS interpretation with vision-centric VLMs |
| XLRS-Bench | Ultra-high-resolution RS MLLM benchmark/modeling direction |
| GeoPix / GeoPixel | Pixel-level image understanding and grounding in remote sensing |
| Co-LLaVA | Efficient RS VQA through model collaboration |
| RLita | Region-level image-text alignment for RSFMs |
| EarthMind | Unified multimodal LLM using cross-sensor EO data |
| Geo-R1 | Few-shot geospatial referring expression understanding |
| RSThinker | Perceptually grounded geospatial chain-of-thought |
| FUSAR-KLIP | Multimodal foundation modeling for RS |
| GeoMag | Pixel-level fine-grained RS image parsing |
| RemoteSAM | Segment Anything direction for Earth observation |
| LRS-VQA | Coarse-to-fine pruning for large RS VQA |
| UrbanLLaVA | Urban intelligence with spatial reasoning |
| SARCLIP | Contrastive language-image pretraining for SAR imagery |
| FUSE-RSVLM | Feature-fusion RS vision-language model |
| Aquila | Hierarchically aligned RS VLM |
| RSCoVLM | Cotraining VLMs for RS multitask learning |
| GeoReason | Logical-consistency reinforcement learning for RS VLMs |
| RemoteReasoner | Unified geospatial reasoning workflow |
| SkyMoE | Mixture-of-experts VLM for geospatial interpretation |
| GeoEyes | Evidence-grounded ultra-high-resolution RS understanding |
| GeoSolver | Test-time reasoning for RS with process supervision |
| GeoAlignCLIP | Fine-grained RS vision-language alignment |
| RS-WorldModel | RS understanding and future-sense forecasting |
| RemoteShield | Robust MLLMs for Earth observation |
| UniChange | Change detection with multimodal LLMs |
| ZoomEarth | Active perception for ultra-high-resolution geospatial VLM tasks |
| UniGeoSeg | Unified open-world segmentation for geospatial scenes |
| FUSAR-GPT | Spatiotemporal visual-language model for SAR imagery |
| SATtxt | Spectrally distilled satellite representations aligned with LLM instructions |
| TerraScope | Pixel-grounded visual reasoning for Earth observation |

---

## 4. Generative, Vision-Location, and Vision-Audio Geospatial Foundation Models

### Generative remote-sensing models

| Model | Focus |
| --- | --- |
| GeoRSSD | RS5M-derived remote-sensing stable diffusion model |
| CRS-Diff | Controllable remote-sensing image generation |
| DiffusionSat | Generative foundation model for satellite imagery |
| HSIGene | Foundation model for hyperspectral image generation |
| Text2Earth | Text-driven remote-sensing image generation |
| MetaEarth | Global-scale remote-sensing image generation |
| EcoMapper | Climate-aware satellite imagery generation |
| OSMGen | OSM-conditioned satellite image synthesis |
| Any2RSI | Controllable RS text-to-image generation |
| GeoDiT | Point-conditioned diffusion transformer for satellite imagery |
| MetaEarth3D | World-scale 3D geospatial generation |

### Vision-location models

| Model | Focus |
| --- | --- |
| CSP | Contrastive spatial pretraining for geospatial-visual representations |
| GeoCLIP | CLIP-style alignment between images and locations for geolocalization |
| SatCLIP | General-purpose location embeddings with satellite imagery |
| RANGE | Retrieval-augmented neural fields for multiresolution geo-embeddings |
| Geo2 | Geometry-guided cross-view geolocalization and image synthesis |
| GeoBridge | Semantic-anchored multiview model for geolocalization |

### Vision-audio geospatial models

| Model | Focus |
| --- | --- |
| GeoBind | Binding text, image, and audio through satellite images |
| PSM | Probabilistic embeddings for multiscale zero-shot soundscape mapping |
| Sat2Sound | Zero-shot soundscape mapping from satellite context |

---

## 5. Weather, Climate, Atmosphere, and Earth-System Foundation Models

### Prithvi WxC
- Organization: IBM, NASA, Oak Ridge National Laboratory collaborators
- Modalities: weather/climate variables, MERRA-2-derived data
- Tasks: forecasting, downscaling, gravity-wave parameterization, extreme events
- Notes: 2.3B-parameter open weather/climate foundation model.
- Paper: https://arxiv.org/abs/2409.13598
- GitHub: https://github.com/NASA-IMPACT/Prithvi-WxC
- Hugging Face pretrained: https://huggingface.co/ibm-nasa-geospatial/Prithvi-WxC-1.0-2300M
- Hugging Face gravity-wave fine-tune: https://huggingface.co/ibm-nasa-geospatial/Prithvi-WxC-1.0-2300m-gravity-wave-parameterization
- NASA Earthdata: https://www.earthdata.nasa.gov/news/blog/prithvi-weather-climate-advancing-our-understanding-atmosphere
- IBM blog: https://research.ibm.com/blog/foundation-model-weather-climate

### Aurora
- Organization: Microsoft Research
- Modalities: atmospheric, air-pollution, and ocean-wave variables
- Tasks: weather prediction, air pollution prediction, ocean wave prediction, tropical cyclone tracking
- Notes: Foundation model of the atmosphere with open code and Hugging Face weights.
- GitHub: https://github.com/microsoft/aurora
- Docs: https://microsoft.github.io/aurora/
- Models: https://microsoft.github.io/aurora/models.html

### ClimaX
- Organization: Microsoft Research
- Modalities: weather and climate variables
- Tasks: weather/climate modeling across variables and tasks
- Notes: Early general foundation model for weather and climate.
- Paper: https://arxiv.org/abs/2301.10343
- GitHub: https://github.com/microsoft/ClimaX

### GraphCast
- Organization: Google DeepMind
- Modalities: global weather reanalysis fields
- Tasks: medium-range weather forecasting
- Notes: Not always labeled a foundation model, but important FM-adjacent global weather AI baseline.
- DeepMind: https://deepmind.google/discover/blog/graphcast-ai-model-for-faster-and-more-accurate-global-weather-forecasting/
- GitHub: https://github.com/google-deepmind/graphcast

### GenCast
- Organization: Google DeepMind
- Modalities: weather reanalysis fields
- Tasks: probabilistic weather forecasting
- Notes: FM-adjacent generative weather model.
- DeepMind: https://deepmind.google/discover/blog/gencast-predicts-weather-and-the-risks-of-extreme-conditions-with-sota-accuracy/

### FourCastNet
- Organization: NVIDIA / collaborators
- Modalities: global weather fields
- Tasks: data-driven weather forecasting
- Notes: Important weather-AI baseline; FM-adjacent rather than usually described as a foundation model.
- GitHub: https://github.com/NVlabs/FourCastNet

### Pangu-Weather
- Organization: Huawei Cloud / collaborators
- Modalities: global weather fields
- Tasks: global medium-range weather forecasting
- Notes: Important weather-AI baseline; FM-adjacent.
- Nature: https://www.nature.com/articles/s41586-023-06185-3

---

## 6. Geospatial, Population, Subsurface, and Other Geo-Domain Foundation Models

### Population Dynamics Foundation Model (PDFM)
- Organization: Google Research / University of Nevada, Reno collaborators
- Modalities: population dynamics and geospatial covariates
- Tasks: downstream geospatial population modeling
- Paper: https://arxiv.org/abs/2411.07207
- GitHub: https://github.com/google-research/population-dynamics

### ThinkOnward Geophysical Foundation Model
- Organization: ThinkOnward
- Modalities: geophysical / subsurface data
- Tasks: geophysical modeling
- GitHub: https://github.com/thinkonward/geophysical-foundation-model

### GAIR
- Modalities: geo-aligned implicit representations
- Tasks: geospatial representation learning
- Paper: https://arxiv.org/pdf/2503.16683

---

## 7. Agentic GeoAI and Foundation-Model Composition

### Google Geospatial Reasoning / Earth AI
- Organization: Google Research / Google Earth AI
- Modalities: multiple geospatial foundation models, imagery, maps, structured geospatial data
- Tasks: cross-modal geospatial reasoning, insights, analysis workflows
- Geospatial Reasoning blog: https://research.google/blog/geospatial-reasoning-unlocking-insights-with-generative-ai-and-multiple-foundation-models/
- Earth AI blog: https://research.google/blog/google-earth-ai-unlocking-geospatial-insights-with-foundation-models-and-cross-modal-reasoning/
- Project: https://sites.research.google/gr/geospatial-reasoning/
- Google Earth AI hub: https://ai.google/earth-ai/

### REMSA
- Modality: LLM agent over remote-sensing foundation model metadata and selection tasks
- Tasks: automated remote-sensing FM selection
- Notes: Relevant because model selection itself is becoming an agentic workflow.
- OpenReview: https://openreview.net/forum?id=F1ZD5wi02T
- arXiv HTML: https://arxiv.org/html/2511.17442v1

### Foundation Model Composition for Earth Observation
- Task: composition of multiple EO foundation models
- Paper: https://arxiv.org/html/2506.20174

---

## 8. Benchmarks, Surveys, and Resource Lists

### PANGAEA
- Purpose: global benchmark for geospatial foundation models
- Notes: Evaluates GFMs across datasets, tasks, resolutions, modalities, and temporalities.
- Paper: https://arxiv.org/abs/2412.04204
- Hugging Face paper page: https://huggingface.co/papers/2412.04204

### WxC-Bench
- Purpose: downstream weather and climate benchmark dataset
- Paper: https://arxiv.org/abs/2412.02780
- Hugging Face dataset: https://huggingface.co/datasets/nasa-impact/WxC-Bench

### Surveys
- Survey of Multimodal Geospatial Foundation Models: https://arxiv.org/abs/2510.22964
- A Survey on Remote Sensing Foundation Models: From Vision to Multimodality: https://arxiv.org/abs/2503.22081
- Vision Foundation Models in Remote Sensing: https://arxiv.org/abs/2408.03464
- Advances on Multimodal Remote Sensing Foundation Models: https://www.mdpi.com/2072-4292/17/21/3532
- On the foundations of Earth foundation models: https://www.nature.com/articles/s43247-025-03127-x

### Existing Awesome Lists / Resource Lists
- Awesome Remote Sensing Foundation Models: https://github.com/Jack-bo1220/Awesome-Remote-Sensing-Foundation-Models
- RS Foundation Models: https://github.com/wgcban/RS-Foundation-Models
- Awesome Remote Sensing Multimodal LLMs: https://github.com/ZhanYang-nwpu/Awesome-Remote-Sensing-Multimodal-Large-Language-Model
- Awesome Vision-Language Models for Earth Observation: https://github.com/geoaigroup/awesome-vision-language-models-for-earth-observation
- Advanced Earth Observation paper list: https://github.com/earth-insights/Advanced-Earth-Observation
- Purdue geoscience foundation models knowledge base: https://www.rcac.purdue.edu/knowledge/gfms?all=true

---


## 9. Comprehensive Upstream RSFM Index

This section mirrors the maintained Awesome Remote Sensing Foundation Models index, last checked on 2026-05-08. It is included to make this file closer to complete. The detailed model cards above should be treated as curated summaries; this appendix is the broad coverage layer.

Source: https://github.com/Jack-bo1220/Awesome-Remote-Sensing-Foundation-Models

### 9.1 Vision Foundation Models

| Model | Title | Venue / year | Paper | Code / weights |
| --- | --- | --- | --- | --- |
| GeoKR | Geographical Knowledge-Driven Representation Learning for Remote Sensing Images | TGRS2021 | [paper](https://ieeexplore.ieee.org/abstract/document/9559903) | [link](https://github.com/flyakon/Geographical-Knowledge-driven-Representaion-Learning) |
| - | Self-Supervised Learning of Remote Sensing Scene Representations Using Contrastive Multiview Coding | CVPRW2021 | [paper](https://openaccess.thecvf.com/content/CVPR2021W/EarthVision/html/Stojnic_Self-Supervised_Learning_of_Remote_Sensing_Scene_Representations_Using_Contrastive_Multiview_CVPRW_2021_paper.html) | [link](https://github.com/vladan-stojnic/CMC-RSSR) |
| GASSL | Geography-Aware Self-Supervised Learning | ICCV2021 | [paper](https://openaccess.thecvf.com/content/ICCV2021/html/Ayush_Geography-Aware_Self-Supervised_Learning_ICCV_2021_paper.html) | [link](https://github.com/sustainlab-group/geography-aware-ssl) |
| SeCo | Seasonal Contrast: Unsupervised Pre-Training From Uncurated Remote Sensing Data | ICCV2021 | [paper](https://openaccess.thecvf.com/content/ICCV2021/html/Manas_Seasonal_Contrast_Unsupervised_Pre-Training_From_Uncurated_Remote_Sensing_Data_ICCV_2021_paper.html) | [link](https://github.com/ServiceNow/seasonal-contrast) |
| RSP | An Empirical Study of Remote Sensing Pretraining | TGRS2022 | [paper](https://ieeexplore.ieee.org/abstract/document/9782149) | [link](https://github.com/ViTAE-Transformer/Remote-Sensing-RVSA) |
| MATTER | Self-Supervised Material and Texture Representation Learning for Remote Sensing Tasks | CVPR2022 | [paper](https://openaccess.thecvf.com/content/CVPR2022/html/Akiva_Self-Supervised_Material_and_Texture_Representation_Learning_for_Remote_Sensing_Tasks_CVPR_2022_paper.html) | [link](https://github.com/periakiva/MATTER) |
| - | Self-supervised Vision Transformers for Land-cover Segmentation and Classification | CVPRW2022 | [paper](https://openaccess.thecvf.com/content/CVPR2022W/EarthVision/html/Scheibenreif_Self-Supervised_Vision_Transformers_for_Land-Cover_Segmentation_and_Classification_CVPRW_2022_paper.html) | [link](https://github.com/HSG-AIML/SSLTransformerRS) |
| DINO-MM | Self-Supervised Vision Transformers for Joint SAR-Optical Representation Learning | IGARSS2022 | [paper](https://doi.org/10.1109/igarss46834.2022.9883983) | [link](https://github.com/zhu-xlab/DINO-MM) |
| GeCo | Geographical Supervision Correction for Remote Sensing Representation Learning | TGRS2022 | [paper](https://ieeexplore.ieee.org/abstract/document/9869651) | [link](https://github.com/GeoX-Lab/G-RSIM) |
| RingMo | RingMo: A remote sensing foundation model with masked image modeling | TGRS2022 | [paper](https://ieeexplore.ieee.org/abstract/document/9844015) | [link](https://github.com/comeony/RingMo) |
| RS-BYOL | Self-Supervised Learning for Invariant Representations From Multi-Spectral and SAR Images | JSTARS2022 | [paper](https://ieeexplore.ieee.org/abstract/document/9880533) | [link](https://ieeexplore.ieee.org/abstract/document/9880533) |
| CSPT | Consecutive Pre-Training: A Knowledge Transfer Learning Strategy with Relevant Unlabeled Data for Remote Sensing Domain | RS2022 | [paper](https://www.mdpi.com/2072-4292/14/22/5675#) | [link](https://github.com/ZhAnGToNG1/transfer_learning_cspt) |
| RVSA | Advancing plain vision transformer toward remote sensing foundation model | TGRS2022 | [paper](https://ieeexplore.ieee.org/abstract/document/9956816) | [link](https://github.com/ViTAE-Transformer/Remote-Sensing-RVSA) |
| SatMAE | SatMAE: Pre-training Transformers for Temporal and Multi-Spectral Satellite Imagery | NeurIPS2022 | [paper](https://proceedings.neurips.cc/paper_files/paper/2022/hash/01c561df365429f33fcd7a7faa44c985-Abstract-Conference.html) | [link](https://github.com/sustainlab-group/SatMAE) |
| DINO-MC | Extending Global-Local View Alignment for Self-Supervised Learning with Remote Sensing Imagery | Arxiv2023 | [paper](https://arxiv.org/abs/2303.06670) | [link](https://github.com/WennyXY/DINO-MC) |
| CMID | CMID: A Unified Self-Supervised Learning Framework for Remote Sensing Image Understanding | TGRS2023 | [paper](https://ieeexplore.ieee.org/abstract/document/10105625) | [link](https://github.com/NJU-LHRS/official-CMID) |
| Presto | Lightweight, Pre-trained Transformers for Remote Sensing Timeseries | Arxiv2023 | [paper](https://arxiv.org/abs/2304.14065) | [link](https://github.com/nasaharvest/presto) |
| AST | AST: Adaptive Self-supervised Transformer for Optical Remote Sensing Representation | ISPRS JPRS2023 | [paper](https://doi.org/10.1016/j.isprsjprs.2023.04.003) |  |
| TOV | TOV: The original vision model for optical remote sensing image understanding via self-supervised learning | JSTARS2023 | [paper](https://ieeexplore.ieee.org/abstract/document/10110958) | [link](https://github.com/GeoX-Lab/G-RSIM/tree/main/TOV_v1) |
| CACo | Change-Aware Sampling and Contrastive Learning for Satellite Images | CVPR2023 | [paper](https://openaccess.thecvf.com/content/CVPR2023/html/Mall_Change-Aware_Sampling_and_Contrastive_Learning_for_Satellite_Images_CVPR_2023_paper.html) | [link](https://github.com/utkarshmall13/CACo) |
| IaI-SimCLR | Multi-Modal Multi-Objective Contrastive Learning for Sentinel-1/2 Imagery | CVPRW2023 | [paper](https://openaccess.thecvf.com/content/CVPR2023W/EarthVision/html/Prexl_Multi-Modal_Multi-Objective_Contrastive_Learning_for_Sentinel-12_Imagery_CVPRW_2023_paper.html) |  |
| - | A Self-Supervised Cross-Modal Remote Sensing Foundation Model with Multi-Domain Representation and Cross-Domain Fusion | IGARSS2023 | [paper](https://ieeexplore.ieee.org/abstract/document/10282433) |  |
| SatLas | SatlasPretrain: A Large-Scale Dataset for Remote Sensing Image Understanding | ICCV2023 | [paper](https://doi.org/10.1109/iccv51070.2023.01538) | [link](https://github.com/allenai/satlas) |
| GFM | Towards Geospatial Foundation Models via Continual Pretraining | ICCV2023 | [paper](https://doi.org/10.1109/iccv51070.2023.01541) | [link](https://github.com/mmendiet/GFM) |
| Scale-MAE | Scale-MAE: A Scale-Aware Masked Autoencoder for Multiscale Geospatial Representation Learning | ICCV2023 | [paper](https://doi.org/10.1109/iccv51070.2023.00378) | [link](https://github.com/bair-climate-initiative/scale-mae) |
| Prithvi | Foundation Models for Generalist Geospatial Artificial Intelligence | Arxiv2023 | [paper](https://arxiv.org/abs/2310.18660) | [link](https://huggingface.co/ibm-nasa-geospatial) |
| RingMo-Sense | RingMo-Sense: Remote Sensing Foundation Model for Spatiotemporal Prediction via Spatiotemporal Evolution Disentangling | TGRS2023 | [paper](https://ieeexplore.ieee.org/abstract/document/10254320) |  |
| EarthPT | EarthPT: a time series foundation model for Earth Observation | NeurIPS2023 CCAI workshop | [paper](https://arxiv.org/abs/2309.07207) | [link](https://github.com/aspiaspace/EarthPT) |
| CROMA | CROMA: Remote Sensing Representations with Contrastive Radar-Optical Masked Autoencoders | NeurIPS2023 | [paper](https://arxiv.org/abs/2311.00566) | [link](https://github.com/antofuller/CROMA) |
| Cross-Scale MAE | Cross-Scale MAE: A Tale of Multiscale Exploitation in Remote Sensing | NeurIPS2023 | [paper](https://openreview.net/pdf?id=5oEVdOd6TV) | [link](https://github.com/aicip/Cross-Scale-MAE) |
| USat | USat: A Unified Self-Supervised Encoder for Multi-Sensor Satellite Imagery | Arxiv2023 | [paper](https://arxiv.org/abs/2312.02199) | [link](https://github.com/stanfordmlgroup/USat) |
| AIEarth | Analytical Insight of Earth: A Cloud-Platform of Intelligent Computing for Geospatial Big Data | Arxiv2023 | [paper](https://arxiv.org/abs/2312.16385) | [link](https://engine-aiearth.aliyun.com/#/) |
| GeRSP | Generic Knowledge Boosted Pretraining for Remote Sensing Images | TGRS2024 | [paper](https://doi.org/10.1109/tgrs.2024.3354031) | [link](https://github.com/floatingstarZ/GeRSP) |
| SMLFR | Generative ConvNet Foundation Model With Sparse Modeling and Low-Frequency Reconstruction for Remote Sensing Image Interpretation | TGRS2024 | [paper](https://ieeexplore.ieee.org/abstract/document/10378718) | [link](https://github.com/HIT-SIRS/SMLFR) |
| RingMo-lite | RingMo-Lite: A Remote Sensing Lightweight Network With CNN-Transformer Hybrid Framework | IEEE TGRS2024 | [paper](https://doi.org/10.1109/tgrs.2024.3360447) |  |
| U-BARN | Self-Supervised Spatio-Temporal Representation Learning of Satellite Image Time Series | JSTARS2024 | [paper](https://ieeexplore.ieee.org/document/10414422) | [link](https://src.koda.cnrs.fr/iris.dumeur/ssl_ubarn) |
| SpectralGPT | SpectralGPT: Spectral Remote Sensing Foundation Model | TPAMI2024 | [paper](https://doi.org/10.1109/tpami.2024.3362475) | [link](https://github.com/danfenghong/IEEE_TPAMI_SpectralGPT) |
| SwiMDiff | SwiMDiff: Scene-Wide Matching Contrastive Learning With Diffusion Constraint for Remote Sensing Image | TGRS2024 | [paper](https://doi.org/10.1109/tgrs.2024.3371481) |  |
| DOFA | Neural Plasticity-Inspired Multimodal Foundation Model for Earth Observation | Arxiv2024 | [paper](https://arxiv.org/abs/2403.15356) | [link](https://github.com/zhu-xlab/DOFA) |
| - | Masked Feature Modeling for Generative Self-Supervised Representation Learning of High-Resolution Remote Sensing Images | IEEE JSTARS2024 | [paper](https://doi.org/10.1109/jstars.2024.3385420) |  |
| BFM | A Billion-scale Foundation Model for Remote Sensing Images | IEEE JSTARS2024 | [paper](https://doi.org/10.1109/jstars.2024.3401772) |  |
| Clay | Clay Foundation Model | Arxiv2024 |  | [link](https://clay-foundation.github.io/model/) |
| Hydro | Hydro--A Foundation Model for Water in Satellite Imagery | Arxiv2024 |  | [link](https://github.com/isaaccorley/hydro-foundation-model) |
| S2MAE | S2MAE: A Spatial-Spectral Pretraining Foundation Model for Spectral Remote Sensing Data | CVPR2024 | [paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Li_S2MAE_A_Spatial-Spectral_Pretraining_Foundation_Model_for_Spectral_Remote_Sensing_CVPR_2024_paper.pdf) |  |
| SatMAE++ | Rethinking Transformers Pre-training for Multi-Spectral Satellite Imagery | CVPR2024 | [paper](https://doi.org/10.1109/cvpr52733.2024.02627) | [link](https://github.com/techmn/satmae_pp) |
| msGFM | Bridging Remote Sensors with Multisensor Geospatial Foundation Models | CVPR2024 | [paper](https://doi.org/10.1109/cvpr52733.2024.02631) | [link](https://github.com/boranhan/Geospatial_Foundation_Models) |
| SkySense | SkySense: A Multi-Modal Remote Sensing Foundation Model Towards Universal Interpretation for Earth Observation Imagery | CVPR2024 | [paper](https://openaccess.thecvf.com/content/CVPR2024/html/Guo_SkySense_A_Multi-Modal_Remote_Sensing_Foundation_Model_Towards_Universal_Interpretation_CVPR_2024_paper.html) | [link](https://github.com/Jack-bo1220/SkySense) |
| MTP | MTP: Advancing Remote Sensing Foundation Model via Multi-Task Pretraining | IEEE JSTARS2024 | [paper](https://doi.org/10.1109/jstars.2024.3408154) | [link](https://github.com/ViTAE-Transformer/MTP) |
| RS-DFM | RS-DFM: A Remote Sensing Distributed Foundation Model for Diverse Downstream Tasks | Arxiv2024 | [paper](https://arxiv.org/abs/2406.07032) |  |
| OFA-Net | One for All: Toward Unified Foundation Models for Earth Vision | IGARSS2024 | [paper](https://doi.org/10.1109/igarss53475.2024.10641637) |  |
| - | Lightweight and Efficient: A Family of Multimodal Earth Observation Foundation Models | IGARSS2024 | [paper](https://doi.org/10.1109/igarss53475.2024.10641132) |  |
| MM-VSF | Towards Knowledge Guided Pretraining Approaches for Multimodal Foundation Models: Applications in Remote Sensing | Arxiv2024 | [paper](https://arxiv.org/abs/2407.19660) |  |
| LeMeViT | LeMeViT: Efficient Vision Transformer with Learnable Meta Tokens for Remote Sensing Image Interpretation | IJCAI2024 | [paper](https://arxiv.org/abs/2405.09789) | [link](https://github.com/ViTAE-Transformer/LeMeViT/tree/main?tab=readme-ov-file) |
| SAR-JEPA | Predicting Gradient is Better: Exploring Self-Supervised Learning for SAR ATR with a Joint-Embedding Predictive Architecture | ISPRS JPRS2024 | [paper](https://www.sciencedirect.com/science/article/pii/S0924271624003514) | [link](https://github.com/waterdisappear/SAR-JEPA) |
| DeCUR | DeCUR: decoupling common & unique representations for multimodal self-supervision | ECCV2024 | [paper](https://doi.org/10.1007/978-3-031-73397-0_17) | [link](https://github.com/zhu-xlab/DeCUR) |
| MMEarth | MMEarth: Exploring Multi-Modal Pretext Tasks For Geospatial Representation Learning | ECCV2024 | [paper](https://doi.org/10.1007/978-3-031-73039-9_10) | [link](https://vishalned.github.io/mmearth/) |
| OmniSat | OmniSat: Self-Supervised Modality Fusion for Earth Observation | ECCV2024 | [paper](https://doi.org/10.1007/978-3-031-73390-1_24) | [link](https://github.com/gastruc/OmniSat?tab=readme-ov-file) |
| MA3E | Masked Angle-Aware Autoencoder for Remote Sensing Images | ECCV2024 | [paper](https://doi.org/10.1007/978-3-031-73242-3_15) | [link](https://github.com/benesakitam/MA3E) |
| SoftCon | Multi-Label Guided Soft Contrastive Learning for Efficient Earth Observation Pretraining | TGRS2024 | [paper](https://ieeexplore.ieee.org/abstract/document/10726860) | [link](https://github.com/zhu-xlab/softcon?tab=readme-ov-file) |
| PIS | Pretrain a Remote Sensing Foundation Model by Promoting Intra-instance Similarity | TGRS2024 | [paper](https://ieeexplore.ieee.org/abstract/document/10697182) | [link](https://github.com/ShawnAn-WHU/PIS) |
| FG-MAE | Feature Guided Masked Autoencoder for Self-Supervised Learning in Remote Sensing | IEEE JSTARS2024 | [paper](https://doi.org/10.1109/jstars.2024.3493237) | [link](https://github.com/zhu-xlab/FGMAE) |
| - | A Multimodal Unified Representation Learning Framework With Masked Image Modeling for Remote Sensing Images | IEEE TGRS2024 | [paper](https://doi.org/10.1109/tgrs.2024.3494244) |  |
| OReole-FM | OReole-FM: successes and challenges toward billion-parameter foundation models for high-resolution satellite imagery | SIGSPATIAL2024 | [paper](https://doi.org/10.1145/3678717.3691292) |  |
| SatVision-TOA | SatVision-TOA: A Geospatial Foundation Model for Coarse-Resolution All-Sky Remote Sensing Imagery | Arxiv2024 | [paper](https://arxiv.org/abs/2411.17000) | [link](https://github.com/nasa-nccs-hpda/pytorch-caney) |
| Prithvi-EO-2.0 | Prithvi-EO-2.0: A Versatile Multi-Temporal Foundation Model for Earth Observation Applications | Arxiv2024 | [paper](https://arxiv.org/abs/2412.02732) | [link](https://huggingface.co/ibm-nasa-geospatial/Prithvi-EO-2.0-300M) |
| A2-MAE | A2-MAE: A spatial-temporal-spectral unified remote sensing pre-training method based on anchor-aware masked autoencoder | IEEE TGRS2025 | [paper](https://doi.org/10.1109/tgrs.2025.3571123) |  |
| FoMo | FoMo: Multi-Modal, Multi-Scale and Multi-Task Remote Sensing Foundation Models for Forest Monitoring | AAAI2025 | [paper](https://doi.org/10.1609/aaai.v39i27.35002) | [link](https://github.com/RolnickLab/FoMo-Bench) |
| PIEViT | Pattern Integration and Enhancement Vision Transformer for Self-Supervised Learning in Remote Sensing | IEEE TGRS2025 | [paper](https://doi.org/10.1109/tgrs.2025.3541390) |  |
| SARATR-X | SARATR-X: Toward Building a Foundation Model for SAR Target Recognition | IEEE TIP2025 | [paper](https://ieeexplore.ieee.org/abstract/document/10856784) | [link](https://github.com/waterdisappear/SARATR-X) |
| SatMamba | SatMamba: Development of Foundation Models for Remote Sensing Imagery Using State Space Models | Arxiv2025 | [paper](https://arxiv.org/abs/2502.00435) | [link](https://github.com/mdchuc/HRSFM) |
| DynamicVis | DynamicVis: Dynamic Visual Perception for Efficient Remote Sensing Foundation Models | Arxiv2025 | [paper](https://arxiv.org/abs/2503.16426) | [link](https://github.com/KyanChen/DynamicVis) |
| SUMMIT | SUMMIT: A SAR foundation model with multiple auxiliary tasks enhanced intrinsic characteristics | IJAEO2025 | [paper](https://doi.org/10.1016/j.jag.2025.104624) |  |
| SenPa-MAE | SenPa-MAE: Sensor Parameter Aware Masked Autoencoder for Multi-Satellite Self-Supervised Pretraining | LNCS2025 | [paper](https://doi.org/10.1007/978-3-031-85187-2_20) | [link](https://github.com/JonathanPrexl/SenPa-MAE) |
| HyperSIGMA | HyperSIGMA: Hyperspectral Intelligence Comprehension Foundation Model | IEEE TPAMI2025 | [paper](https://arxiv.org/abs/2406.11519) | [link](https://github.com/WHU-Sigma/HyperSIGMA?tab=readme-ov-file) |
| HyperSL | HyperSL: A Spectral Foundation Model for Hyperspectral Image Interpretation | IEEE TGRS2025 | [paper](https://ieeexplore.ieee.org/abstract/document/10981753) | [link](https://github.com/kkweil/HyperSL) |
| TiMo | TiMo: Spatiotemporal Foundation Model for Satellite Image Time Series | Arxiv2025 | [paper](https://arxiv.org/abs/2505.08723) | [link](https://github.com/MiliLab/TiMo) |
| Panopticon | Panopticon: Advancing Any-Sensor Foundation Models for Earth Observation | CVPRW2025 (EarthVision Best Paper) | [paper](https://arxiv.org/abs/2503.10845) | [link](https://github.com/Panopticon-FM/panopticon) |
| HyperFree | HyperFree: A Channel-adaptive and Tuning-free Foundation Model for Hyperspectral Remote Sensing Imagery | CVPR2025 | [paper](https://rsidea.whu.edu.cn/HyperFree.pdf) | [link](https://github.com/Jingtao-Li-CVer/HyperFree) |
| SpectralEarth | SpectralEarth: Training Hyperspectral Foundation Models at Scale | IEEE JSTARS2025 | [paper](https://doi.org/10.1109/jstars.2025.3581451) | [link](https://github.com/zhu-xlab/softcon) |
| WV-Net | WV-Net: A foundation model for SAR WV-mode satellite imagery trained using contrastive self-supervised learning on 10 million images | AIES2025 | [paper](https://arxiv.org/abs/2406.18765) |  |
| AnySat | AnySat: One Earth Observation Model for Many Resolutions, Scales, and Modalities | CVPR2025 | [paper](https://arxiv.org/abs/2412.14123) | [link](https://github.com/gastruc/AnySat) |
| TerraFM | TerraFM: A Scalable Foundation Model for Unified Multisensor Earth Observation | Arxiv2025 | [paper](https://arxiv.org/abs/2506.06281) | [link](https://github.com/mbzuai-oryx/TerraFM) |
| Galileo | Galileo: Learning Global & Local Features of Many Remote Sensing Modalities | ICML2025 TerraBytes Workshop | [paper](https://arxiv.org/abs/2502.09356) | [link](https://github.com/nasaharvest/galileo) |
| DeepAndes | DeepAndes: A Self-Supervised Vision Foundation Model for Multispectral Remote Sensing Imagery of the Andes | IEEE JSTARS2025 | [paper](https://doi.org/10.1109/jstars.2025.3619423) | [link](https://github.com/geopacha/DeepAndes) |
| RingMamba | RingMamba: Remote Sensing Multisensor Pretraining With Visual State Space Model | IEEE TGRS2025 | [paper](https://doi.org/10.1109/tgrs.2025.3603998) | [link](https://github.com/ningerhhh/RIFR) |
| RingMo-Aerial | RingMo-Aerial: An Aerial Remote Sensing Foundation Model With Affine Transformation Contrastive Learning | IEEE TPAMI2025 | [paper](https://doi.org/10.1109/tpami.2025.3602237) |  |
| SeaMo | SeaMo: A Multi-Seasonal and Multimodal Remote Sensing Foundation Model | Information Fusion2025 | [paper](https://www.sciencedirect.com/science/article/pii/S1566253525004075) |  |
| MoSAiC | MoSAiC: Multi-Modal Multi-Label Supervision-Aware Contrastive Learning for Remote Sensing | IEEE Sensors Journal 2025 | [paper](https://arxiv.org/abs/2507.08683) |  |
| CGEarthEye | CGEarthEye: A High-Resolution Remote Sensing Vision Foundation Model Based on the Jilin-1 Satellite Constellation | Arxiv2025 | [paper](https://arxiv.org/abs/2507.00356) |  |
| AlphaEarth | AlphaEarth Foundations: An embedding field model for accurate and efficient global mapping from sparse label data | Arxiv2025 | [paper](https://arxiv.org/abs/2507.22291) | [link](https://deepmind.google/blog/alphaearth-foundations-helps-map-our-planet-in-unprecedented-detail/) |
| SkySense++ | A semantic-enhanced multi-modal remote sensing foundation model for Earth observation | Nature Machine Intelligence 2025 | [paper](https://www.nature.com/articles/s42256-025-01078-8) | [link](https://github.com/kang-wu/SkySensePlusPlus?tab=readme-ov-file) |
| CtxMIM | CtxMIM: Context-Enhanced Masked Image Modeling for Remote Sensing Image Understanding | ACM TOMM2025 | [paper](https://doi.org/10.1145/3769084) |  |
| ViTP | Visual Instruction Pretraining for Domain-Specific Foundation Models | Arxiv2025 | [paper](https://arxiv.org/abs/2509.17562) | [link](https://huggingface.co/GreatBird/ViTP) |
| SatDiFuser | Can Generative Geospatial Diffusion Models Excel as Discriminative Geospatial Foundation Models? | ICCV2025 | [paper](https://arxiv.org/abs/2503.07890) | [link](https://github.com/yurujaja/SatDiFuser) |
| FedSense | Towards Privacy-preserved Pre-training of Remote Sensing Foundation Models with Federated Mutual-guidance Learning | ICCV2025 | [paper](https://arxiv.org/abs/2503.11051) |  |
| Copernicus-FM | Towards a Unified Copernicus Foundation Model for Earth Vision | ICCV2025 | [paper](https://arxiv.org/abs/2503.11849) | [link](https://github.com/zhu-xlab/Copernicus-FM) |
| TerraMind | TerraMind: Large-Scale Generative Multimodality for Earth Observation | ICCV2025 | [paper](https://arxiv.org/abs/2504.11171) | [link](https://github.com/IBM/terramind) |
| SelectiveMAE | Harnessing Massive Satellite Imagery with Efficient Masked Image Modeling | ICCV2025 | [paper](https://arxiv.org/abs/2406.11933) | [link](https://github.com/Fengxiang23/SelectiveMAE) |
| SMARTIES | SMARTIES: Spectrum-Aware Multi-Sensor Auto-Encoder for Remote Sensing Images | ICCV2025 | [paper](https://arxiv.org/abs/2506.19585) | [link](https://gsumbul.github.io/SMARTIES/) |
| SkySense V2 | SkySense V2: A Unified Foundation Model for Multi-modal Remote Sensing | ICCV2025 | [paper](https://arxiv.org/abs/2507.13812) |  |
| RS-vHeat | RS-vHeat: Heat Conduction Guided Efficient Remote Sensing Foundation Model | ICCV2025 | [paper](https://arxiv.org/abs/2411.17984) |  |
| RoMA | RoMA: Scaling up Mamba-based Foundation Models for Remote Sensing | NeurIPS2025 | [paper](https://arxiv.org/abs/2503.10392) | [link](https://github.com/MiliLab/RoMA) |
| GeoLink | GeoLink: Empowering Remote Sensing Foundation Model with OpenStreetMap Data | NeurIPS2025 | [paper](https://arxiv.org/abs/2509.26016) | [link](https://github.com/bailubin/GeoLink_NeurIPS2025) |
| CrossEarth | CrossEarth: Geospatial Vision Foundation Model for Domain Generalizable Remote Sensing Semantic Segmentation | IEEE TPAMI2025 | [paper](https://doi.org/10.1109/tpami.2025.3649001) | [link](https://github.com/Cuzyoung/CrossEarth) |
| PhySwin | PhySwin: An Efficient and Physically-Informed Foundation Model for Multispectral Earth Observation | NeurIPS2025 | [paper](https://openreview.net/forum?id=zrBucj9BwG) |  |
| FlexiMo | FlexiMo: A Flexible Remote Sensing Foundation Model | IEEE TGRS2026 | [paper](https://doi.org/10.1109/tgrs.2026.3656362) |  |
| MAPEX | MAPEX: Modality-Aware Pruning of Experts for Remote Sensing Foundation Models | IEEE TGRS2026 | [paper](https://doi.org/10.1109/tgrs.2026.3652100) | [link](https://github.com/HSG-AIML/MAPEX) |
| - | A Complex-Valued SAR Foundation Model Based on Physically Inspired Representation Learning | IEEE TIP2026 | [paper](https://doi.org/10.1109/tip.2026.3652417) |  |
| MAESTRO | MAESTRO: Masked AutoEncoders for Multimodal, Multitemporal, and Multispectral Earth Observation Data | WACV2026 | [paper](https://openaccess.thecvf.com/content/WACV2026/papers/Labatie_MAESTRO_Masked_AutoEncoders_for_Multimodal_Multitemporal_and_Multispectral_Earth_Observation_WACV_2026_paper.pdf) | [link](https://github.com/IGNF/MAESTRO) |
| RingMoE | RingMoE: Mixture-of-Modality-Experts Multi-Modal Foundation Models for Universal Remote Sensing Image Interpretation | IEEE TPAMI2026 | [paper](https://doi.org/10.1109/tpami.2025.3643453) |  |
| Alliance | Alliance: All-in-One Spectral-Spatial-Frequency Awareness Foundation Model | IEEE TPAMI2026 | [paper](https://doi.org/10.1109/tpami.2025.3639595) |  |
| THOR | THOR: A Versatile Foundation Model for Earth Observation Climate and Society Applications | Arxiv2026 | [paper](https://arxiv.org/abs/2601.16011) | [link](https://github.com/FM4CS/THOR) |
| AgriFM | AgriFM: A multi-source temporal remote sensing foundation model for Agriculture mapping | RSE2026 | [paper](https://doi.org/10.1016/j.rse.2026.115234) | [link](https://github.com/flyakon/AgriFM) |
| SIGMAE | SIGMAE: A Spectral-Index-Guided Foundation Model for Multispectral Remote Sensing | Arxiv2026 | [paper](https://arxiv.org/abs/2603.07463) | [link](https://github.com/zxk688/SIGMAE) |
| CrossEarth-SAR | CrossEarth-SAR: A SAR-Centric and Billion-Scale Geospatial Foundation Model for Domain Generalizable Semantic Segmentation | Arxiv2026 | [paper](https://arxiv.org/abs/2603.12008) | [link](https://github.com/VisionXLab/CrossEarth-SAR) |
| NeighborMAE | NeighborMAE: Exploiting Spatial Dependencies between Neighboring Earth Observation Images in Masked Autoencoders Pretraining | CVPR2026 | [paper](https://arxiv.org/abs/2603.02522) |  |
| MOMO | MOMO: Mars Orbital Model Foundation Model for Mars Orbital Applications | CVPR2026 | [paper](https://arxiv.org/abs/2604.02719) | [link](https://github.com/kerner-lab/MOMO) |
| TESSERA | TESSERA: Temporal Embeddings of Surface Spectra for Earth Representation and Analysis | CVPR2026 | [paper](https://arxiv.org/abs/2506.20380) | [link](https://github.com/ucam-eo/tessera) |
| OlmoEarth | OlmoEarth: Stable Latent Image Modeling for Multimodal Earth Observation | CVPR2026 | [paper](https://arxiv.org/abs/2511.13655) | [link](https://github.com/allenai/olmoearth_pretrain) |
| RAMEN | RAMEN: Resolution-Adjustable Multimodal Encoder for Earth Observation | CVPR2026 | [paper](https://arxiv.org/abs/2512.05025) | [link](https://github.com/nicolashoudre/RAMEN) |
| SARMAE | SARMAE: Masked Autoencoder for SAR Representation Learning | CVPR2026 | [paper](https://arxiv.org/abs/2512.16635) | [link](https://github.com/MiliLab/SARMAE) |

### 9.2 Vision-Language Foundation Models

| Model | Title | Venue / year | Paper | Code / weights |
| --- | --- | --- | --- | --- |
| - | Charting New Territories: Exploring the Geographic and Geospatial Capabilities of Multimodal LLMs | Arxiv2023 | [paper](https://arxiv.org/abs/2311.14656) | [link](https://github.com/jonathan-roberts1/charting-new-territories) |
| - | Remote Sensing ChatGPT: Solving Remote Sensing Tasks with ChatGPT and Visual Models | Arxiv2024 | [paper](https://arxiv.org/abs/2401.09083) | [link](https://github.com/HaonanGuo/Remote-Sensing-ChatGPT) |
| SkyCLIP | SkyScript: A Large and Semantically Diverse Vision-Language Dataset for Remote Sensing | AAAI2024 | [paper](https://arxiv.org/abs/2312.12856) | [link](https://github.com/wangzhecheng/SkyScript) |
| GeoRSCLIP | RS5M and GeoRSCLIP: A Large Scale Vision-Language Dataset and A Large Vision-Language Model for Remote Sensing | IEEE TGRS2024 | [paper](https://arxiv.org/abs/2306.11300) | [link](https://github.com/om-ai-lab/RS5M) |
| RemoteCLIP | RemoteCLIP: A Vision Language Foundation Model for Remote Sensing | IEEE TGRS2024 | [paper](https://arxiv.org/abs/2306.11029) | [link](https://github.com/ChenDelong1999/RemoteCLIP) |
| EarthGPT | EarthGPT: A Universal Multimodal Large Language Model for Multisensor Image Comprehension in Remote Sensing Domain | IEEE TGRS2024 | [paper](https://doi.org/10.1109/tgrs.2024.3409624) | [link](https://github.com/wivizhang/EarthGPT) |
| GRAFT | Remote Sensing Vision-Language Foundation Models without Annotations via Ground Remote Alignment | ICLR2024 | [paper](https://openreview.net/pdf?id=w9tc699w3Z) |  |
| EarthMarker | EarthMarker: A Visual Prompting Multi-modal Large Language Model for Remote Sensing | IEEE TGRS2024 | [paper](https://arxiv.org/abs/2407.13596) | [link](https://github.com/wivizhang/EarthMarker) |
| RingMoGPT | RingMoGPT: A Unified Remote Sensing Foundation Model for Vision, Language, and Grounded Tasks | IEEE TGRS2024 | [paper](https://ieeexplore.ieee.org/document/10777289) |  |
| RS-LLaVA | RS-LLaVA: Large Vision Language Model for Joint Captioning and Question Answering in Remote Sensing Imagery | RS2024 | [paper](https://www.mdpi.com/2072-4292/16/9/1477) | [link](https://github.com/BigData-KSU/RS-LLaVA) |
| GeoChat | GeoChat: Grounded Large Vision-Language Model for Remote Sensing | CVPR2024 | [paper](https://openaccess.thecvf.com/content/CVPR2024/html/Kuckreja_GeoChat_Grounded_Large_Vision-Language_Model_for_Remote_Sensing_CVPR_2024_paper.html) | [link](https://github.com/mbzuai-oryx/GeoChat) |
| SkySenseGPT | SkySenseGPT: A Fine-Grained Instruction Tuning Dataset and Model for Remote Sensing Vision-Language Understanding | Arxiv2024 | [paper](https://arxiv.org/abs/2406.10100) | [link](https://github.com/Luo-Z13/SkySenseGPT) |
| RSCLIP | Pushing the Limits of Vision-Language Models in Remote Sensing without Human Annotations | Arxiv2024 | [paper](https://arxiv.org/abs/2409.07048) |  |
| GeoText | Towards Natural Language-Guided Drones: GeoText-1652 Benchmark with Spatial Relation Matching | ECCV2024 | [paper](https://arxiv.org/abs/2311.12751) | [link](https://github.com/MultimodalGeo/GeoText-1652) |
| LHRS-Bot | LHRS-Bot: Empowering Remote Sensing with VGI-Enhanced Large Multimodal Language Model | ECCV2024 | [paper](https://arxiv.org/abs/2402.02544) | [link](https://github.com/NJU-LHRS/LHRS-Bot) |
| GeoGround | GeoGround: A Unified Large Vision-Language Model for Remote Sensing Visual Grounding | Arxiv2024 | [paper](https://arxiv.org/abs/2411.11904) | [link](https://github.com/zytx121/GeoGround) |
| RSUniVLM | RSUniVLM: A Unified Vision Language Model for Remote Sensing via Granularity-oriented Mixture of Experts | Arxiv2024 | [paper](https://arxiv.org/abs/2412.05679) |  |
| REO-VLM | REO-VLM: Transforming VLM to Meet Regression Challenges in Earth Observation | Arxiv2024 | [paper](https://arxiv.org/abs/2412.16583) |  |
| UniRS | UniRS: Unifying Multi-temporal Remote Sensing Tasks through Vision Language Models | Arxiv2024 | [paper](https://arxiv.org/abs/2412.20742) |  |
| VHM | VHM: Versatile and Honest Vision Language Model for Remote Sensing Image Analysis | AAAI2025 | [paper](https://ojs.aaai.org/index.php/AAAI/article/view/32683) | [link](https://github.com/opendatalab/VHM) |
| - | Quality-Driven Curation of Remote Sensing Vision-Language Data via Learned Scoring Models | Arxiv2025 | [paper](https://arxiv.org/abs/2503.00743) |  |
| DOFA-CLIP | DOFA-CLIP: Multimodal Vision-Language Foundation Models for Earth Observation | Arxiv2025 | [paper](https://arxiv.org/abs/2503.06312) | [link](https://github.com/xiong-zhitong/GeoLB-SigLIP) |
| Falcon | Falcon: A Remote Sensing Vision-Language Foundation Model | Arxiv2025 | [paper](https://arxiv.org/abs/2503.11070) | [link](https://github.com/TianHuiLab/Falcon) |
| GeoRSMLLM | GeoRSMLLM: A Multimodal Large Language Model for Vision-Language Tasks in Geoscience and Remote Sensing | Arxiv2025 | [paper](https://arxiv.org/abs/2503.12490) |  |
| OmniGeo | OmniGeo: Towards a Multimodal Large Language Models for Geospatial Artificial Intelligence | Arxiv2025 | [paper](https://arxiv.org/abs/2503.16326) |  |
| DGTRS-CLIP | DGTRSD & DGTRS-CLIP: A Dual-Granularity Remote Sensing Image-Text Dataset and Vision Language Foundation Model for Alignment | Arxiv2025 | [paper](https://arxiv.org/abs/2503.19311) | [link](https://github.com/MitsuiChen14/DGTRS) |
| EagleVision | EagleVision: Object-level Attribute Multimodal LLM for Remote Sensing | Arxiv2025 | [paper](https://arxiv.org/abs/2503.23330) | [link](https://github.com/XiangTodayEatsWhat/EagleVision) |
| SkyEyeGPT | SkyEyeGPT: Unifying Remote Sensing Vision-Language Tasks via Instruction Tuning with Large Language Model | ISPRS JPRS2025 | [paper](https://doi.org/10.1016/j.isprsjprs.2025.01.020) | [link](https://github.com/ZhanYang-nwpu/SkyEyeGPT) |
| SegEarth-R1 | SegEarth-R1: Geospatial Pixel Reasoning via Large Language Model | Arxiv2025 | [paper](https://arxiv.org/abs/2504.09644) | [link](https://github.com/earth-insights/SegEarth-R1) |
| EarthGPT-X | EarthGPT-X: A Spatial MLLM for Multi-level Multi-Source Remote Sensing Imagery Understanding with Visual Prompting | Arxiv2025 | [paper](https://arxiv.org/abs/2504.12795) | [link](https://github.com/wivizhang/EarthGPT-X) |
| TEOChat | TEOChat: A Large Vision-Language Assistant for Temporal Earth Observation Data | ICLR2025 | [paper](https://arxiv.org/abs/2410.06234) | [link](https://github.com/ermongroup/TEOChat) |
| LISAt | LISAt: Language-Instructed Segmentation Assistant for Satellite Imagery | Arxiv2025 | [paper](https://arxiv.org/abs/2505.02829) |  |
| DynamicVL | DynamicVL: Benchmarking Multimodal Large Language Models for Dynamic City Understanding | Arxiv2025 | [paper](https://arxiv.org/abs/2505.21076) |  |
| RSGPT | RSGPT: A Remote Sensing Vision Language Model and Benchmark | ISPRS JPRS2025 | [paper](https://doi.org/10.1016/j.isprsjprs.2025.04.001) | [link](https://github.com/Lavender105/RSGPT) |
| LHRS-Bot-Nova | LHRS-Bot-Nova: Improved Multimodal Large Language Model for Remote Sensing Vision-Language Interpretation | ISPRS JPRS2025 | [paper](https://doi.org/10.1016/j.isprsjprs.2025.06.003) | [link](https://github.com/NJU-LHRS/LHRS-Bot) |
| EarthDial | EarthDial: Turning Multi-sensory Earth Observations to Interactive Dialogues | CVPR2025 | [paper](https://openaccess.thecvf.com/content/CVPR2025/html/Soni_EarthDial_Turning_Multi-sensory_Earth_Observations_to_Interactive_Dialogues_CVPR_2025_paper.html) | [link](https://github.com/hiyamdebary/EarthDial) |
| SkySense-O | SkySense-O: Towards Open-World Remote Sensing Interpretation with Vision-Centric Visual-Language Modeling | CVPR2025 | [paper](https://openaccess.thecvf.com/content/CVPR2025/papers/Zhu_SkySense-O_Towards_Open-World_Remote_Sensing_Interpretation_with_Vision-Centric_Visual-Language_Modeling_CVPR_2025_paper.pdf) | [link](https://github.com/zqcrafts/SkySense-O) |
| XLRS-Bench | XLRS-Bench: Could Your Multimodal LLMs Understand Extremely Large Ultra-High-Resolution Remote Sensing Imagery? | CVPR2025 | [paper](https://arxiv.org/abs/2503.23771) |  |
| GeoPix | GeoPix: Multi-Modal Large Language Model for Pixel-level Image Understanding in Remote Sensing | IEEE GRSM2025 | [paper](https://arxiv.org/abs/2501.06828) | [link](https://github.com/Norman-Ou/GeoPix) |
| Co-LLaVA | Co-LLaVA: Efficient Remote Sensing Visual Question Answering via Model Collaboration | RS2025 | [paper](https://doi.org/10.3390/rs17030466) |  |
| RLita | RLita: A Region-Level Image-Text Alignment Method for Remote Sensing Foundation Model | RS2025 | [paper](https://doi.org/10.3390/rs17101661) |  |
| EarthMind | EarthMind: Leveraging Cross-Sensor Data for Advanced Earth Observation Interpretation with a Unified Multimodal LLM | Arxiv2025 | [paper](https://arxiv.org/abs/2506.01667) | [link](https://github.com/shuyansy/EarthMind) |
| - | Remote Sensing Large Vision-Language Model: Semantic-augmented Multi-level Alignment and Semantic-aware Expert Modeling | Arxiv2025 | [paper](https://arxiv.org/abs/2506.21863) |  |
| GeoPixel | GeoPixel: Pixel Grounding Large Multimodal Model in Remote Sensing | ICML2025 | [paper](https://arxiv.org/abs/2501.13925) | [link](https://github.com/mbzuai-oryx/GeoPixel) |
| RingMo-Agent | RingMo-Agent: A Unified Remote Sensing Foundation Model for Multi-Platform and Multi-Modal Reasoning | Arxiv2025 | [paper](https://arxiv.org/abs/2507.20776) |  |
| Geo-R1 | Geo-R1: Improving Few-Shot Geospatial Referring Expression Understanding with Reinforcement Fine-Tuning | Arxiv2025 | [paper](https://arxiv.org/abs/2509.21976) |  |
| RSThinker | Towards Faithful Reasoning in Remote Sensing: A Perceptually-Grounded GeoSpatial Chain-of-Thought for Vision-Language Models | Arxiv2025 | [paper](https://arxiv.org/abs/2509.22221) |  |
| FUSAR-KLIP | FUSAR-KLIP: Towards Multimodal Foundation Models for Remote Sensing | Arxiv2025 | [paper](https://arxiv.org/abs/2509.23927) | [link](https://github.com/yangyifremad/SARKnowLIP) |
| GeoMag | GeoMag: A Vision-Language Model for Pixel-level Fine-Grained Remote Sensing Image Parsing | ACMMM2025 | [paper](https://doi.org/10.1145/3746027.3754559) |  |
| RemoteSAM | RemoteSAM: Towards Segment Anything for Earth Observation | ACMMM2025 | [paper](https://arxiv.org/abs/2505.18022) | [link](https://github.com/1e12Leon/RemoteSAM) |
| LRS-VQA | When Large Vision-Language Model Meets Large Remote Sensing Imagery: Coarse-to-Fine Text-Guided Token Pruning | ICCV2025 | [paper](https://arxiv.org/abs/2503.07588) | [link](https://github.com/VisionXLab/LRS-VQA) |
| UrbanLLaVA | UrbanLLaVA: A Multi-modal Large Language Model for Urban Intelligence with Spatial Reasoning and Understanding | ICCV2025 | [paper](https://arxiv.org/abs/2506.23219) | [link](https://github.com/tsinghua-fib-lab/UrbanLLaVA) |
| SARCLIP | SARCLIP: a multimodal foundation framework for SAR imagery via contrastive language-image pre-training | ISPRS JPRS2025 | [paper](https://doi.org/10.1016/j.isprsjprs.2025.10.011) | [link](https://huggingface.co/BiliSakura/SARCLIP-ViT-L-14) |
| FUSE-RSVLM | FUSE-RSVLM: Feature Fusion Vision-Language Model for Remote Sensing | Arxiv2025 | [paper](https://arxiv.org/abs/2512.24022) | [link](https://github.com/Yunkaidang/RSVLM) |
| Aquila | Aquila: A Hierarchically Aligned Vision-Language Model for Enhanced Remote Sensing Image Comprehension | Journal of Remote Sensing 2026 | [paper](https://doi.org/10.34133/remotesensing.1041) |  |
| RSCoVLM | Co-Training Vision-Language Models for Remote Sensing Multi-Task Learning | RS2026 | [paper](https://doi.org/10.3390/rs18020222) | [link](https://github.com/VisionXLab/RSCoVLM) |
| GeoReason | GeoReason: Aligning Thinking And Answering In Remote Sensing Vision-Language Models Via Logical Consistency Reinforcement Learning | Arxiv2026 | [paper](https://arxiv.org/abs/2601.04118) | [link](https://github.com/canlanqianyan/GeoReason) |
| RemoteReasoner | RemoteReasoner: Towards Unifying Geospatial Reasoning Workflow | AAAI2026 | [paper](https://arxiv.org/abs/2507.19280) |  |
| SkyMoE | SkyMoE: A Vision-Language Foundation Model for Enhancing Geospatial Interpretation with Mixture of Experts | AAAI2026 | [paper](https://arxiv.org/abs/2512.02517) |  |
| GeoEyes | GeoEyes: On-Demand Visual Focusing for Evidence-Grounded Understanding of Ultra-High-Resolution Remote Sensing Imagery | Arxiv2026 | [paper](https://arxiv.org/abs/2602.14201) | [link](https://github.com/nanocm/GeoEyes) |
| GeoSolver | GeoSolver: Scaling Test-Time Reasoning in Remote Sensing with Fine-Grained Process Supervision | Arxiv2026 | [paper](https://arxiv.org/abs/2603.09551) |  |
| GeoAlignCLIP | GeoAlignCLIP: Enhancing Fine-Grained Vision-Language Alignment in Remote Sensing via Multi-Granular Consistency Learning | Arxiv2026 | [paper](https://arxiv.org/abs/2603.09566) |  |
| RS-WorldModel | RS-WorldModel: a Unified Model for Remote Sensing Understanding and Future Sense Forecasting | Arxiv2026 | [paper](https://arxiv.org/abs/2603.14941) |  |
| Decoding-the-Delta | Decoding the Delta: Unifying Remote Sensing Change Detection and Understanding with Multimodal Large Language Models | Arxiv2026 | [paper](https://arxiv.org/abs/2604.14044) |  |
| RemoteShield | RemoteShield: Enable Robust Multimodal Large Language Models for Earth Observation | Arxiv2026 | [paper](https://arxiv.org/abs/2604.17243) |  |
| UniChange | UniChange: Unifying Change Detection with Multimodal Large Language Model | CVPR2026 | [paper](https://arxiv.org/abs/2511.02607) | [link](https://github.com/NKU-HLT/UniChange) |
| ZoomEarth | ZoomEarth: Active Perception for Ultra-High-Resolution Geospatial Vision-Language Tasks | CVPR2026 | [paper](https://arxiv.org/abs/2511.12267) |  |
| UniGeoSeg | UniGeoSeg: Towards Unified Open-World Segmentation for Geospatial Scenes | CVPR2026 | [paper](https://arxiv.org/abs/2511.23332) | [link](https://github.com/MiliLab/UniGeoSeg) |
| SegEarth-R2 | SegEarth-R2: Towards Comprehensive Language-guided Segmentation for Remote Sensing Images | CVPR2026 | [paper](https://arxiv.org/abs/2512.20013) | [link](https://github.com/earth-insights/SegEarth-R2) |
| FUSAR-GPT | FUSAR-GPT: A Spatiotemporal Feature-Embedded and Two-Stage Decoupled Visual Language Model for SAR Imagery | CVPR2026 | [paper](https://arxiv.org/abs/2602.19190) |  |
| SATtxt | Spectrally Distilled Representations Aligned with Instruction-Augmented LLMs for Satellite Imagery | CVPR2026 | [paper](https://arxiv.org/abs/2602.22613) | [link](https://github.com/ikhado/sattxt) |
| TerraScope | TerraScope: Pixel-Grounded Visual Reasoning for Earth Observation | CVPR2026 | [paper](https://arxiv.org/abs/2603.19039) |  |

### 9.3 Generative Foundation Models

| Model | Title | Venue / year | Paper | Code / weights |
| --- | --- | --- | --- | --- |
| GeoRSSD | RS5M: A Large Scale Vision-Language Dataset for Remote Sensing Vision-Language Foundation Model | Arxiv2023 | [paper](https://arxiv.org/abs/2306.11300) | [link](https://huggingface.co/Zilun/GeoRSSD) |
| - | Generate Your Own Scotland: Satellite Image Generation Conditioned on Maps | NeurIPSW2023 | [paper](https://arxiv.org/abs/2308.16648) | [link](https://github.com/toastyfrosty/map-sat) |
| CRS-Diff | CRS-Diff: Controllable Remote Sensing Image Generation with Diffusion Model | Arxiv2024 | [paper](https://arxiv.org/abs/2403.11614) | [link](https://github.com/Sonettoo/CRS-Diff) |
| DiffusionSat | DiffusionSat: A Generative Foundation Model for Satellite Imagery | ICLR2024 | [paper](https://arxiv.org/abs/2312.03606) | [link](https://github.com/samar-khanna/DiffusionSat) |
| HSIGene | HSIGene: A Foundation Model For Hyperspectral Image Generation | Arxiv2024 | [paper](https://arxiv.org/abs/2409.12470) | [link](https://github.com/LiPang/HSIGene) |
| Text2Earth | Text2Earth: Unlocking Text-driven Remote Sensing Image Generation with a Global-Scale Dataset and a Foundation Model | GRSM2025 | [paper](https://arxiv.org/abs/2501.00895) | [link](https://chen-yang-liu.github.io/Text2Earth/) |
| MetaEarth | MetaEarth: A Generative Foundation Model for Global-Scale Remote Sensing Image Generation | TPAMI2025 | [paper](https://arxiv.org/abs/2405.13570) | [link](https://jiupinjia.github.io/metaearth/) |
| EcoMapper | EcoMapper: Generative Modeling for Climate-Aware Satellite Imagery | ICML2025 | [paper](https://proceedings.mlr.press/v267/goktepe25a.html) | [link](https://github.com/maltevb/ecomapper) |
| OSMGen | OSMGen: Highly Controllable Satellite Image Synthesis using OpenStreetMap Data | NeurIPSW2025 | [paper](https://arxiv.org/abs/2511.00345) | [link](https://github.com/amir-zsh/OSMGen) |
| Any2RSI | Any2RSI: Controllable Remote Sensing Text-to-Image Generation via Any Control and Enriched Description | AAAI2026 | [paper](https://ojs.aaai.org/index.php/AAAI/article/view/38283) | [link](https://github.com/lwCVer/RFD) |
| GeoDiT | GeoDiT: Point-Conditioned Diffusion Transformer for Satellite Image Synthesis | Arxiv2026 | [paper](https://arxiv.org/abs/2603.02172) |  |
| MetaEarth3D | MetaEarth3D: Unlocking World-scale 3D Generation with Spatially Scalable Generative Modeling | Arxiv2026 | [paper](https://arxiv.org/abs/2604.22828) |  |

### 9.4 Vision-Location Foundation Models

| Model | Title | Venue / year | Paper | Code / weights |
| --- | --- | --- | --- | --- |
| CSP | CSP: Self-Supervised Contrastive Spatial Pre-Training for Geospatial-Visual Representations | ICML2023 | [paper](https://arxiv.org/abs/2305.01118) | [link](https://gengchenmai.github.io/csp-website/) |
| GeoCLIP | GeoCLIP: Clip-Inspired Alignment between Locations and Images for Effective Worldwide Geo-localization | NeurIPS2023 | [paper](https://arxiv.org/abs/2309.16020) | [link](https://vicentevivan.github.io/GeoCLIP/) |
| SatCLIP | SatCLIP: Global, General-Purpose Location Embeddings with Satellite Imagery | AAAI2025 | [paper](https://arxiv.org/abs/2311.17179) | [link](https://github.com/microsoft/satclip) |
| GAIR | GAIR: Location-Aware Self-Supervised Contrastive Pre-Training with Geo-Aligned Implicit Representations | Arxiv2025 | [paper](https://arxiv.org/abs/2503.16683) | [link](https://github.com/zpl99/GAIR) |
| RANGE | RANGE: Retrieval Augmented Neural Fields for Multi-Resolution Geo-Embeddings | CVPR2025 | [paper](https://arxiv.org/abs/2502.19781) |  |
| Geo² | Geo²: Geometry-Guided Cross-view Geo-Localization and Image Synthesis | CVPR2026 | [paper](https://arxiv.org/abs/2603.25819) |  |
| GeoBridge | GeoBridge: A Semantic-Anchored Multi-View Foundation Model Bridging Images and Text for Geo-Localization | CVPR2026 | [paper](https://arxiv.org/abs/2512.02697) | [link](https://github.com/MiliLab/GeoBridge) |

### 9.5 Vision-Audio Foundation Models

| Model | Title | Venue / year | Paper | Code / weights |
| --- | --- | --- | --- | --- |
| - | Self-supervised audiovisual representation learning for remote sensing data | JAG2022 | [paper](https://www.sciencedirect.com/science/article/pii/S1569843222003181) | [link](https://github.com/khdlr/SoundingEarth) |
| GeoBind | GeoBind: Binding Text, Image, and Audio through Satellite Images | IGARSS2024 | [paper](https://arxiv.org/abs/2404.11720) |  |
| PSM | PSM: Learning Probabilistic Embeddings for Multi-scale Zero-Shot Soundscape Mapping | ACM MM 2024 | [paper](https://arxiv.org/abs/2408.07050) | [link](https://github.com/mvrl/PSM) |
| Sat2Sound | Sat2Sound: A Unified Framework for Zero-Shot Soundscape Mapping | Arxiv2025 | [paper](https://arxiv.org/abs/2505.13777) |  |

## 10. Suggested Metadata Fields For The Next Step

To make this list more useful than a normal awesome-list, convert every model above into a YAML record with:

```yaml
name:
family:
organization:
year:
model_type:
modalities:
sensors:
spatial_resolution:
temporal_support:
parameters:
embedding_dim:
tasks:
training_data:
open_weights:
open_code:
license:
huggingface:
github:
paper:
project_page:
verified_status: unverified
notes:
```

Recommended `verified_status` values:

```text
metadata-only
weights-load
sample-inference-runs
benchmark-reproduced
broken-or-unavailable
```
