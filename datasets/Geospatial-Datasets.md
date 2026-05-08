# Geospatial Datasets — Curated Reference

A comprehensive reference for geospatial / Earth-observation datasets. Focused on large, well-documented datasets suitable for production use, foundation model training, and downstream fine-tuning.

**Fields per entry:** Organization · Year · Sensor · Resolution · Size · Classes · Coverage · License · Links

---

## 1. Pre-Training & Foundation Model Scale Datasets

Large-scale datasets (100k+ samples) used for self-supervised or supervised pre-training of geospatial foundation models.

### SSL4EO-S12
- **GitHub:** https://github.com/zhu-xlab/SSL4EO-S12
- **HuggingFace:** https://huggingface.co/datasets/wangyi111/SSL4EO-S12
- **Paper:** https://arxiv.org/abs/2211.07044
- **Organization:** TU Munich (Zhu Lab)
- **Year:** 2023
- **Task:** Self-supervised pre-training
- **Sensor:** Sentinel-1 (SAR), Sentinel-2 (MS)
- **Resolution:** 10 m
- **Size:** 3 million patches (1M locations × 4 seasons × 2 sensors)
- **Classes:** Unlabeled
- **Coverage:** Global
- **License:** CC-BY-4.0

### SSL4EO-L
- **GitHub:** https://github.com/zhu-xlab/SSL4EO-S12
- **Paper:** https://arxiv.org/abs/2306.09424
- **Organization:** TU Munich
- **Year:** 2023
- **Task:** Self-supervised pre-training
- **Sensor:** Landsat 4/5/7/8/9
- **Resolution:** 30 m
- **Size:** 5M patches (1M locations × 5 seasons)
- **Classes:** Unlabeled
- **Coverage:** Global
- **License:** CC0-1.0

### SatlasPretrain
- **Project:** https://satlas-pretrain.allen.ai
- **GitHub:** https://github.com/allenai/satlas
- **Paper:** https://arxiv.org/abs/2211.15660
- **Organization:** Allen Institute for AI
- **Year:** 2023
- **Task:** Multi-task pre-training (17 tasks)
- **Sensor:** NAIP (0.6 m), Sentinel-2 (10 m), Landsat (30 m)
- **Resolution:** 0.6–30 m
- **Size:** 302 million image chips
- **Classes:** 17 task categories (building, road, tree, crop, etc.)
- **Coverage:** USA (NAIP), Global (Sentinel-2/Landsat)
- **License:** Multi (CC-BY-4.0, ODbL, public domain)

### Major TOM Core (S2L2A, S2L1C, S1RTC, DEM)
- **HuggingFace:** https://huggingface.co/Major-TOM
- **GitHub:** https://github.com/ESA-PhiLab/Major-TOM
- **Paper:** https://arxiv.org/abs/2402.12095
- **Organization:** ESA Φ-lab
- **Year:** 2024
- **Task:** Pre-training, representation learning
- **Sensor:** Sentinel-2 L2A/L1C, Sentinel-1 RTC, Copernicus DEM
- **Resolution:** 10 m
- **Size:** ~4.49 million patches per modality (global grid)
- **Classes:** Unlabeled
- **Coverage:** Global
- **License:** CC-BY-SA-4.0

### Copernicus-Pretrain
- **HuggingFace:** https://huggingface.co/datasets/wangyi111/Copernicus-Pretrain
- **Paper:** https://arxiv.org/abs/2407.01485
- **Organization:** TU Munich
- **Year:** 2024
- **Task:** Multi-modal pre-training
- **Sensor:** Sentinel-1, Sentinel-2, Sentinel-3, Sentinel-5P, DEM
- **Resolution:** 10–1000 m
- **Size:** 18.7 million patches
- **Classes:** Unlabeled
- **Coverage:** Global
- **License:** CC-BY-4.0

### BigEarthNet
- **Project:** http://bigearth.net
- **GitHub:** https://github.com/kai-tub/bigearthnet-pipeline
- **Paper:** https://arxiv.org/abs/1902.06148
- **Organization:** TU Berlin
- **Year:** 2019 (v2: 2023)
- **Task:** Multi-label scene classification, pre-training
- **Sensor:** Sentinel-2 (v1); Sentinel-1 + Sentinel-2 (v2)
- **Resolution:** 10–60 m
- **Size:** 590,326 patches (v1); 549,488 patch pairs (v2)
- **Classes:** 19 CORINE land cover classes (43 raw)
- **Coverage:** 10 European countries
- **License:** CDLA-Permissive-1.0

### MMEarth
- **HuggingFace:** https://huggingface.co/datasets/torchgeo/MMEarth
- **GitHub:** https://github.com/vishalned/MMEarth-data
- **Paper:** https://arxiv.org/abs/2405.02771
- **Organization:** TU Munich / DLR
- **Year:** 2024
- **Task:** Multi-modal pre-training
- **Sensor:** Sentinel-1/2, ASTER DEM, ERA5, ESA WorldCover
- **Resolution:** 10 m
- **Size:** 1.2 million patches (100k–1M depending on modality)
- **Classes:** Unlabeled
- **Coverage:** Global
- **License:** CC-BY-4.0

### SeasoNet
- **HuggingFace:** https://huggingface.co/datasets/wangyi111/SeasoNet
- **Zenodo:** https://zenodo.org/record/5850307
- **Paper:** https://arxiv.org/abs/2205.02218
- **Organization:** DLR / TU Munich
- **Year:** 2023
- **Task:** Seasonal multi-label classification, pre-training
- **Sensor:** Sentinel-2
- **Resolution:** 10 m
- **Size:** 1,759,830 patches (across 4 seasons)
- **Classes:** 33 CORINE classes
- **Coverage:** Germany
- **License:** CC-BY-4.0

### SkyScript
- **GitHub:** https://github.com/wangzhecheng/SkyScript
- **Paper:** https://arxiv.org/abs/2312.12856
- **Organization:** Stanford University
- **Year:** 2024
- **Task:** Vision-language pre-training (image captioning)
- **Sensor:** NAIP, Planet, Sentinel-2, Landsat
- **Resolution:** 0.1–30 m
- **Size:** 5.2 million image-text pairs
- **Classes:** Free-text descriptions
- **Coverage:** Global
- **License:** MIT

### Million-AID
- **Project:** https://captain-whu.github.io/DiRS
- **Paper:** https://arxiv.org/abs/2006.12485
- **Organization:** Wuhan University
- **Year:** 2021
- **Task:** Scene classification, pre-training
- **Sensor:** Google Earth
- **Resolution:** 0.5–153 m
- **Size:** 1,000,000 images
- **Classes:** 51 scene categories (hierarchical)
- **Coverage:** Global
- **License:** Unspecified (research use)

### ChatEarthNet
- **GitHub:** https://github.com/zhu-xlab/ChatEarthNet
- **Paper:** https://arxiv.org/abs/2402.11325
- **Organization:** TU Munich
- **Year:** 2024
- **Task:** Vision-language pre-training
- **Sensor:** Sentinel-2
- **Resolution:** 10 m
- **Size:** 163,488 image-text pairs (derived from BigEarthNet)
- **Classes:** Free-text descriptions
- **Coverage:** Europe
- **License:** CC-BY-4.0

---

## 2. Scene Classification

### EuroSAT
- **GitHub:** https://github.com/phelber/EuroSAT
- **HuggingFace:** https://huggingface.co/datasets/blanchon/EuroSAT_RGB
- **Paper:** https://arxiv.org/abs/1709.00029
- **Organization:** DFKI
- **Year:** 2019
- **Task:** Scene classification
- **Sensor:** Sentinel-2 (13-band MS + RGB variant)
- **Resolution:** 10 m
- **Size:** 27,000 patches (64×64 px)
- **Classes:** 10 land-use categories
- **Coverage:** 34 European countries
- **License:** MIT

### RESISC45
- **TF Catalog:** https://www.tensorflow.org/datasets/catalog/resisc45
- **Paper:** https://arxiv.org/abs/1703.00121
- **Organization:** Northwestern Polytechnical University (NWPU)
- **Year:** 2017
- **Task:** Scene classification
- **Sensor:** Google Earth
- **Resolution:** 0.2–30 m (varied)
- **Size:** 31,500 images (700 per class, 256×256 px)
- **Classes:** 45 scene categories
- **Coverage:** Global
- **License:** CC-BY-NC-4.0

### PatternNet
- **Project:** https://sites.google.com/view/zhouwx/dataset
- **Paper:** https://arxiv.org/abs/1706.04768
- **Organization:** UC Merced / UCSB
- **Year:** 2018
- **Task:** Scene classification
- **Sensor:** Google Earth, USGS
- **Resolution:** 0.06–5 m
- **Size:** 30,400 images (800 per class, 256×256 px)
- **Classes:** 38 categories
- **Coverage:** USA
- **License:** CC-BY-4.0

### So2Sat LCZ42
- **HuggingFace:** https://huggingface.co/datasets/torchgeo/So2Sat
- **Zenodo:** https://mediatum.ub.tum.de/1454690
- **Paper:** https://arxiv.org/abs/1912.12171
- **Organization:** TU Munich / DLR
- **Year:** 2020
- **Task:** Local climate zone (urban) classification
- **Sensor:** Sentinel-1 (SAR), Sentinel-2 (MS)
- **Resolution:** 10 m
- **Size:** 400,673 patches (32×32 px per sensor)
- **Classes:** 17 local climate zones
- **Coverage:** 42 global cities
- **License:** CC-BY-4.0

### Functional Map of the World (fMoW)
- **GitHub:** https://github.com/fMoW/dataset
- **Paper:** https://arxiv.org/abs/1711.07846
- **Organization:** IARPA
- **Year:** 2017
- **Task:** Scene classification (temporal)
- **Sensor:** WorldView-2/3 (0.3 m), other commercial
- **Resolution:** 0.3–1 m
- **Size:** 1 million image chips
- **Classes:** 63 functional land-use categories
- **Coverage:** Global
- **License:** Community use license (free for research)

### AID (Aerial Image Dataset)
- **Project:** https://captain-whu.github.io/AID/
- **Paper:** https://arxiv.org/abs/1608.05167
- **Organization:** Wuhan University
- **Year:** 2017
- **Task:** Scene classification
- **Sensor:** Google Earth
- **Resolution:** 0.5–8 m
- **Size:** 10,000 images
- **Classes:** 30 aerial scene categories
- **Coverage:** Global
- **License:** Research use only

### UC Merced Land Use
- **Project:** http://weegee.vision.ucmerced.edu/datasets/landuse.html
- **Paper:** https://dl.acm.org/doi/10.1145/1869790.1869829
- **Organization:** UC Merced
- **Year:** 2010
- **Task:** Scene classification (benchmark)
- **Sensor:** USGS National Map (aerial)
- **Resolution:** 0.3 m (1 ft)
- **Size:** 2,100 images (100 per class, 256×256 px)
- **Classes:** 21 land-use categories
- **Coverage:** USA
- **License:** Public domain

---

## 3. Semantic Segmentation & Land Cover

### SEN12MS
- **Zenodo:** https://mediatum.ub.tum.de/1474000
- **GitHub:** https://github.com/zhu-xlab/SEN12MS
- **Paper:** https://arxiv.org/abs/1906.07789
- **Organization:** TU Munich
- **Year:** 2019
- **Task:** Land cover segmentation, multi-modal fusion
- **Sensor:** Sentinel-1 (SAR), Sentinel-2 (MS), MODIS
- **Resolution:** 10 m (upsampled)
- **Size:** 180,748 triplets (256×256 px)
- **Classes:** 17 IGBP / 33 LCCS land cover classes
- **Coverage:** All continents (all seasons)
- **License:** CC-BY-4.0

### FLAIR #1 & #2 (IGN)
- **Project:** https://ignf.github.io/FLAIR/
- **GitHub:** https://github.com/IGNF/FLAIR-1, https://github.com/IGNF/FLAIR-2
- **Paper:** https://arxiv.org/abs/2310.13336
- **Organization:** IGN (Institut national de l'information géographique)
- **Year:** 2022 / 2023
- **Task:** Land cover semantic segmentation (FLAIR-2: aerial + Sentinel-2 fusion)
- **Sensor:** VHR aerial (0.2 m), Sentinel-2 (10 m)
- **Resolution:** 0.2 m aerial; 10 m Sentinel-2
- **Size:** 77,412 aerial patches (512×512 px) + time-series Sentinel-2
- **Classes:** 19 land cover categories
- **Coverage:** France (metropolitan)
- **License:** Open License Etalab 2.0

### OpenEarthMap
- **Project:** https://open-earth-map.org
- **GitHub:** https://github.com/bao18/open_earth_map
- **Paper:** https://arxiv.org/abs/2210.10732
- **Organization:** Kyushu University / RIKEN
- **Year:** 2022
- **Task:** Global land cover segmentation
- **Sensor:** Google Earth / VHR aerial
- **Resolution:** 0.25–0.5 m
- **Size:** 5,000 images, 97,203 annotated patches (1024×1024 px)
- **Classes:** 9 land cover categories
- **Coverage:** 97 regions across 44 countries (global)
- **License:** CC-BY-NC-SA-4.0

### Five Billion Pixels
- **Project:** https://x-ytong.github.io/project/Five-Billion-Pixels.html
- **Paper:** https://arxiv.org/abs/2209.01424
- **Organization:** Wuhan University
- **Year:** 2022
- **Task:** Large-scale land cover segmentation
- **Sensor:** Gaofen-2 (Chinese VHR satellite)
- **Resolution:** 4 m
- **Size:** ~5 billion pixel labels (150 × 150 km² scenes)
- **Classes:** 24 fine-grained categories
- **Coverage:** China
- **License:** Research use only

### ISPRS Potsdam & Vaihingen
- **Project (Potsdam):** https://www.isprs.org/education/benchmarks/UrbanClassification/2d-sem-label-potsdam.aspx
- **Project (Vaihingen):** https://www.isprs.org/education/benchmarks/UrbanClassification/default.aspx
- **Organization:** ISPRS
- **Year:** 2012 / 2014
- **Task:** Urban land cover segmentation (benchmark standard)
- **Sensor:** VHR aerial (RGB + NIR + DSM)
- **Resolution:** 5 cm (Potsdam), 9 cm (Vaihingen)
- **Size:** 38 patches (Potsdam), 33 patches (Vaihingen)
- **Classes:** 6 urban categories (building, tree, low veg., surface, car, background)
- **Coverage:** Potsdam & Vaihingen, Germany
- **License:** Free for non-commercial research

### DeepGlobe Land Cover
- **Project:** http://deepglobe.org
- **Paper:** https://arxiv.org/abs/1805.06561
- **Organization:** CVPR 2018 Challenge
- **Year:** 2018
- **Task:** Land cover segmentation
- **Sensor:** DigitalGlobe Vivid+ satellite
- **Resolution:** 0.5 m
- **Size:** 1,146 satellite images (2448×2448 px)
- **Classes:** 7 land cover types
- **Coverage:** Thailand, Indonesia, India
- **License:** CC-BY-NC-SA-4.0

### LandCoverNet
- **Radiant MLHub:** https://mlhub.earth/data/ref_landcovernet_v1
- **Paper:** https://arxiv.org/abs/2012.03111
- **Organization:** Radiant Earth Foundation
- **Year:** 2020
- **Task:** Annual land cover classification
- **Sensor:** Sentinel-2
- **Resolution:** 10 m
- **Size:** 1,980 chips (256×256 px), Africa subset (20 % of global)
- **Classes:** 7 land cover categories
- **Coverage:** Sub-Saharan Africa (global planned)
- **License:** CC-BY-4.0

### LoveDA
- **GitHub:** https://github.com/Junjue-Wang/LoveDA
- **Paper:** https://arxiv.org/abs/2110.08733
- **Organization:** Wuhan University
- **Year:** 2021
- **Task:** Domain-adaptive semantic segmentation (urban vs. rural)
- **Sensor:** Google Earth
- **Resolution:** 0.3 m
- **Size:** 5,987 images
- **Classes:** 7 land cover categories
- **Coverage:** 3 cities in China (Nanjing, Changchun, Wuhan)
- **License:** CC-BY-NC-SA-4.0

### WorldStrat
- **GitHub:** https://github.com/worldstrat/worldstrat
- **HuggingFace:** https://huggingface.co/datasets/worldstrat/worldstrat
- **Paper:** https://arxiv.org/abs/2207.06418
- **Organization:** University of Oxford
- **Year:** 2022
- **Task:** Super-resolution training, land use classification
- **Sensor:** SPOT (1.5 m HR), Sentinel-2 (10 m LR)
- **Resolution:** 1.5 m / 10 m paired
- **Size:** 10,000 km² coverage (~2,500 paired locations)
- **Classes:** 5 UNHCR humanitarian land-use categories
- **Coverage:** Stratified global sample (including underrepresented regions)
- **License:** CC-BY-4.0

---

## 4. Object Detection

### DOTA (Dataset for Object deTection in Aerial images) v1 / v2
- **Project:** https://captain-whu.github.io/DOTA/
- **Paper:** https://arxiv.org/abs/1711.10398 (v1), https://arxiv.org/abs/2102.12219 (v2)
- **Organization:** Wuhan University
- **Year:** 2018 / 2021
- **Task:** Oriented (rotated) object detection
- **Sensor:** Google Earth, Gaofen-2, JL-1
- **Resolution:** 0.3–1 m
- **Size:** 2,806 images / 15 classes (v1); 11,268 images / 18 classes (v2); 1.7M instance annotations (v2)
- **Classes:** 15 (v1) / 18 (v2): aircraft, ship, vehicle, baseball diamond, bridge, etc.
- **Coverage:** Global
- **License:** Non-commercial research

### xView (xView1)
- **Project:** http://xviewdataset.org
- **Paper:** https://arxiv.org/abs/1802.07856
- **Organization:** DIUx (Defense Innovation Unit)
- **Year:** 2018
- **Task:** Object detection
- **Sensor:** WorldView-3
- **Resolution:** 0.3 m
- **Size:** 1,413 images (> 1 million object instances)
- **Classes:** 60 categories (vehicles, aircraft, maritime, infrastructure)
- **Coverage:** Global
- **License:** CC-BY-NC-SA-4.0

### FAIR1M
- **Project:** http://gaofen-challenge.com
- **HuggingFace:** https://huggingface.co/datasets/blanchon/FAIR1M
- **Paper:** https://arxiv.org/abs/2103.05569
- **Organization:** Gaofen Challenge / CASIA
- **Year:** 2021
- **Task:** Fine-grained oriented object detection
- **Sensor:** Gaofen satellites + Google Earth
- **Resolution:** 0.3–0.8 m
- **Size:** 15,000+ images; 43,289 instances
- **Classes:** 37 fine-grained categories (5 super-categories)
- **Coverage:** Global
- **License:** CC-BY-NC-SA-3.0

### DIOR (Detection in Optical Remote sensing)
- **Project:** https://gcheng-nwpu.github.io/#Datasets
- **Paper:** https://arxiv.org/abs/1909.00133
- **Organization:** Northwestern Polytechnical University
- **Year:** 2020
- **Task:** Object detection
- **Sensor:** Google Earth
- **Resolution:** 0.5–30 m
- **Size:** 23,463 images; 192,518 instances
- **Classes:** 20 categories (airport, baseball field, bridge, etc.)
- **Coverage:** Global
- **License:** CC-BY-NC-4.0

### iSAID
- **Project:** https://captain-whu.github.io/iSAID/
- **Paper:** https://arxiv.org/abs/1905.12886
- **Organization:** IIAI & Wuhan University
- **Year:** 2019
- **Task:** Instance segmentation + object detection
- **Sensor:** Google Earth, JL-1 (high-res aerial)
- **Resolution:** 0.3–1 m
- **Size:** 2,806 images; 655,451 instances
- **Classes:** 15 categories (aircraft, ship, vehicle, building, etc.)
- **Coverage:** Global
- **License:** CC-BY-NC-4.0 (academic use)

### RarePlanes
- **AWS Open Data:** https://registry.opendata.aws/rareplanes/
- **Paper:** https://arxiv.org/abs/2006.02963
- **Organization:** CosmiQ Works / AI.Reverie
- **Year:** 2020
- **Task:** Aircraft detection & attribute recognition
- **Sensor:** WorldView-3 (real) + synthetic
- **Resolution:** 0.3 m
- **Size:** 253 real WV-3 images (14,700 planes); 50,000 synthetic images (630,000 planes)
- **Classes:** Aircraft with 10 attribute labels
- **Coverage:** 122 locations, 22 countries
- **License:** Apache-2.0

### xView2 Building Damage Assessment (xBD)
- **Project:** https://xview2.org
- **Paper:** https://arxiv.org/abs/1911.09296
- **Organization:** DIUx
- **Year:** 2019
- **Task:** Building damage assessment (change detection)
- **Sensor:** WorldView-3
- **Resolution:** 0.3–0.8 m
- **Size:** 4.7 million building polygons; 850 km² coverage
- **Classes:** 4 damage levels (no damage → destroyed)
- **Coverage:** 20 disaster zones across 7 disaster types (wildfire, flood, earthquake, etc.)
- **License:** CC-BY-NC-SA-4.0

### xView3 Dark Vessel Detection
- **Project:** https://iuu.xview.us
- **Paper:** https://arxiv.org/abs/2206.00897
- **Organization:** DIUx / Global Fishing Watch
- **Year:** 2021
- **Task:** Maritime vessel detection (IUU fishing)
- **Sensor:** Sentinel-1 (SAR)
- **Resolution:** 10–40 m
- **Size:** 1,000 Sentinel-1 scenes (> 750k vessel annotations)
- **Classes:** Vessels (fishing vs. non-fishing) + offshore infrastructure
- **Coverage:** Global ocean
- **License:** CC-BY-NC-SA-4.0

---

## 5. Change Detection

### LEVIR-CD+
- **GitHub:** https://github.com/justchenhao/LEVIR
- **Paper:** https://arxiv.org/abs/2006.11205
- **Organization:** Wuhan University
- **Year:** 2020
- **Task:** Building change detection
- **Sensor:** Google Earth (very high-res)
- **Resolution:** 0.5 m
- **Size:** 985 image pairs (1024×1024 px), bi-temporal
- **Classes:** 2 (changed / unchanged building)
- **Coverage:** 20 Texas cities, USA
- **License:** Unspecified (research use)

### OSCD (Onera Satellite Change Detection)
- **Project:** https://rcdaudt.github.io/oscd/
- **Paper:** https://arxiv.org/abs/1810.08452
- **Organization:** Onera / CentraleSupelec
- **Year:** 2018
- **Task:** Urban change detection
- **Sensor:** Sentinel-2 (13 bands)
- **Resolution:** 10 m
- **Size:** 24 city pairs (bi-temporal)
- **Classes:** 2 (change / no-change)
- **Coverage:** 24 global cities
- **License:** CC-BY-NC-SA-4.0

### S2Looking
- **GitHub:** https://github.com/AnonymousForACMMM/Dataset
- **Paper:** https://arxiv.org/abs/2107.09244
- **Organization:** CAS / Aerospace Information Research Institute
- **Year:** 2021
- **Task:** Building change detection (side-looking satellite)
- **Sensor:** SuperView-1 (very high-res)
- **Resolution:** 0.5–0.8 m
- **Size:** 5,000 image pairs
- **Classes:** 2 (new building / demolished building)
- **Coverage:** Global (diverse regions)
- **License:** CC-BY-NC-SA-4.0

### BRIGHT (Building damage Recognition with multi-sensor Imagery after Geophysical and climate-induced disTasters)
- **GitHub:** https://github.com/ChenHongruixuan/BRIGHT
- **Paper:** https://arxiv.org/abs/2501.06019
- **Organization:** TU Munich / DLR
- **Year:** 2025
- **Task:** Disaster building change detection
- **Sensor:** MAXAR, NAIP, Capella (SAR), Umbra (SAR)
- **Resolution:** 0.1–1 m
- **Size:** 3,239 bi-temporal image pairs
- **Classes:** 4 damage levels
- **Coverage:** 12 global disaster events
- **License:** CC-BY-4.0

### Dynamic EarthNet
- **Project:** https://www.earthnet.tech/docs/ds-earthnet2021/
- **Paper:** https://arxiv.org/abs/2111.04986
- **Organization:** Planet / DLR / TU Munich
- **Year:** 2021
- **Task:** Spatio-temporal semantic segmentation + change detection
- **Sensor:** PlanetScope
- **Resolution:** 3 m
- **Size:** 75 AOIs × weekly images over 2 years (approx. 7,500 scenes)
- **Classes:** 7 land cover categories
- **Coverage:** Global (stratified sample)
- **License:** CC-BY-4.0

---

## 6. Instance Segmentation & Building Footprints

### SpaceNet Series (1–8)
- **Project:** https://spacenet.ai
- **GitHub:** https://github.com/SpaceNetChallenge
- **Organization:** CosmiQ Works / AWS / Maxar
- **Year:** 2016–2022
- **Task:** Building footprint extraction, road detection, off-nadir, flood mapping
- **Sensor:** WorldView-2/3 (0.3–0.5 m), Planet Dove (4 m), Capella SAR
- **Resolution:** 0.3–4 m
- **Size:** 27,000–685,000 building footprints per challenge
- **Classes:** Building footprints, road networks
- **Coverage:** Global (Las Vegas, Paris, Shanghai, Khartoum, Moscow, Rotterdam, global, Louisiana)
- **License:** CC-BY-SA-4.0

| Challenge | Focus | Key Spec |
|-----------|-------|----------|
| SN1 | Building detection | Rio de Janeiro, WV-2, 0.5 m |
| SN2 | Multi-city buildings | 5 cities, WV-3, 685k footprints |
| SN3 | Road network | 5 cities, WV-3, 8,000 km roads |
| SN4 | Off-nadir buildings | Atlanta, WV-2, 27 viewing angles |
| SN5 | Road + travel time | 4 cities, WV-3 |
| SN6 | All-weather SAR | Rotterdam, WV-2 + Capella SAR |
| SN7 | Multi-temporal | 100 global sites, Planet 4 m |
| SN8 | Flood + road + building | Louisiana, Maxar |

### Microsoft Global ML Building Footprints
- **GitHub:** https://github.com/microsoft/GlobalMLBuildingFootprints
- **Blog:** https://planetarycomputer.microsoft.com/dataset/ms-buildings
- **Organization:** Microsoft
- **Year:** 2023
- **Task:** Building footprint extraction
- **Sensor:** Bing Maps satellite imagery
- **Resolution:** Varies
- **Size:** 1.3 billion building footprints worldwide
- **Classes:** Building footprints
- **Coverage:** Global (180+ countries)
- **License:** ODbL-1.0

### Google Open Buildings
- **Project:** https://sites.research.google/open-buildings/
- **Paper:** https://arxiv.org/abs/2107.12283
- **Organization:** Google Research
- **Year:** 2021 (v3: 2023)
- **Task:** Building footprint detection
- **Sensor:** Maxar, CNES/Airbus satellite imagery
- **Resolution:** Varies (sub-meter)
- **Size:** 2.5 billion building detections (v3)
- **Classes:** Building footprints with confidence scores
- **Coverage:** Africa (64%), South/Southeast Asia, Latin America
- **License:** CC-BY-4.0

### Inria Aerial Image Labeling
- **Project:** https://project.inria.fr/aerialimagelabeling/
- **Paper:** https://arxiv.org/abs/1910.05985
- **Organization:** Inria
- **Year:** 2017
- **Task:** Building segmentation
- **Sensor:** VHR aerial
- **Resolution:** 0.3 m
- **Size:** 360 images (180 training + 180 test, 5000×5000 px)
- **Classes:** Building / not building
- **Coverage:** 5 US cities + 5 Austrian cities
- **License:** CC-BY-NC-SA-4.0

---

## 7. Agricultural & Crop Mapping

### PASTIS (Panoptic Agricultural Satellite Time Series)
- **GitHub:** https://github.com/VSainteuf/pastis-benchmark
- **Paper:** https://arxiv.org/abs/2107.07933
- **Organization:** IGN / Inria
- **Year:** 2021
- **Task:** Panoptic crop segmentation (semantic + instance)
- **Sensor:** Sentinel-2 (time series)
- **Resolution:** 10 m
- **Size:** 2,433 patches (128×128 px); 124,422 agricultural parcels; 38–61 time steps
- **Classes:** 18 crop types + background
- **Coverage:** France
- **License:** CC-BY-4.0

### BreizhCrops
- **GitHub:** https://github.com/dl4sits/BreizhCrops
- **Paper:** https://arxiv.org/abs/1905.11893
- **Organization:** University of Würzburg / INRA
- **Year:** 2020
- **Task:** Crop type classification from time series
- **Sensor:** Sentinel-2 (time series, ~70 observations/year)
- **Resolution:** 10 m
- **Size:** 600,000+ parcel time series
- **Classes:** 9 crop categories
- **Coverage:** Brittany (Bretagne), France
- **License:** MIT

### CropHarvest
- **GitHub:** https://github.com/nasaharvest/cropharvest
- **HuggingFace:** https://huggingface.co/datasets/nasaharvest/cropharvest
- **Paper:** https://arxiv.org/abs/2206.08919
- **Organization:** NASA Harvest / McGill
- **Year:** 2021
- **Task:** Crop / non-crop binary + multi-class classification
- **Sensor:** Sentinel-1/2, SRTM DEM, ERA5 climate (all fused)
- **Resolution:** 10 m
- **Size:** 70,213 labelled pixels across 70+ countries
- **Classes:** 351 crop type labels (mapped to binary or coarse taxonomy)
- **Coverage:** Global (strongly multi-continental)
- **License:** CC-BY-SA-4.0

### Sen4AgriNet
- **GitHub:** https://github.com/Orion-AI-Lab/S4A
- **Paper:** https://arxiv.org/abs/2201.07771
- **Organization:** Orion AI Lab (NTUA)
- **Year:** 2022
- **Task:** Crop type mapping from time series
- **Sensor:** Sentinel-2 (time series)
- **Resolution:** 10 m
- **Size:** 247,421 patches (annual time series)
- **Classes:** 15+ crop categories
- **Coverage:** France, Greece
- **License:** CC-BY-4.0

### EuroCrops
- **GitHub:** https://github.com/maja601/EuroCrops
- **HuggingFace:** https://huggingface.co/datasets/torchgeo/EuroCrops
- **Paper:** https://arxiv.org/abs/2302.10202
- **Organization:** TU Munich
- **Year:** 2023
- **Task:** Crop type mapping (LPIS-derived labels + Sentinel-2)
- **Sensor:** Sentinel-2
- **Resolution:** 10 m
- **Size:** 23 million field parcels across 16 EU countries
- **Classes:** HCAT harmonised crop taxonomy (34 L1 classes)
- **Coverage:** 16 European countries
- **License:** CC-BY-SA-4.0

### ZueriCrop
- **GitHub:** https://github.com/0zgur0/ms-convSTAR
- **Paper:** https://arxiv.org/abs/2102.08820
- **Organization:** ETH Zurich / Agroscope
- **Year:** 2021
- **Task:** Crop type mapping (time series)
- **Sensor:** Sentinel-2 (time series)
- **Resolution:** 10 m
- **Size:** 116,000 patches (24×24 px); 71 time steps
- **Classes:** 48 crop categories
- **Coverage:** Zurich canton, Switzerland
- **License:** CC-BY-NC-4.0

### Kenya Crop Type (Radiant MLHub)
- **Radiant MLHub:** https://mlhub.earth/data/ref_african_crops_kenya_02
- **Organization:** Radiant Earth / PlantVillage
- **Year:** 2020
- **Task:** Crop type segmentation
- **Sensor:** Sentinel-2 (time series)
- **Resolution:** 10 m
- **Size:** 4,688 patches with ground truth labels
- **Classes:** 7 crop types (maize, cassava, etc.)
- **Coverage:** Western Kenya
- **License:** CC-BY-SA-4.0

---

## 8. SAR (Synthetic Aperture Radar)

### HRSID (High-Resolution SAR Images Dataset)
- **GitHub:** https://github.com/chaozhong2010/HRSID
- **Paper:** https://ieeexplore.ieee.org/document/9127795
- **Organization:** PLA Strategic Support Force
- **Year:** 2020
- **Task:** Ship detection & instance segmentation
- **Sensor:** Sentinel-1, TerraSAR-X, TanDEM-X (SAR)
- **Resolution:** 0.5–3 m
- **Size:** 5,604 images; 16,951 ship instances
- **Classes:** Ship / non-ship
- **Coverage:** Global waters
- **License:** CC-BY-NC-SA-4.0

### SAR-Ship Dataset
- **GitHub:** https://github.com/CAESAR-Radi/SAR-Ship-Dataset
- **Paper:** https://www.mdpi.com/2072-4292/11/7/765
- **Organization:** Chinese Academy of Sciences
- **Year:** 2019
- **Task:** Ship detection
- **Sensor:** Sentinel-1, GF-3 (SAR)
- **Resolution:** 1.7–25 m
- **Size:** 43,819 ship chips (256×256 px)
- **Classes:** Ship instances
- **Coverage:** Global
- **License:** CC-BY-NC-4.0

### SAR-Aircraft Dataset
- **GitHub:** https://github.com/hust-rslab/SAR-aircraft-data
- **Paper:** https://arxiv.org/abs/2107.11272
- **Organization:** Huazhong University of Science and Technology
- **Year:** 2021
- **Task:** Aircraft detection
- **Sensor:** SAR (C-band, X-band)
- **Resolution:** Medium–High
- **Size:** 2,966 patches; 7,835 aircraft instances
- **Classes:** Aircraft
- **Coverage:** Multiple airports
- **License:** CC-BY-NC-4.0

### MSTAR (Moving and Stationary Target Acquisition and Recognition)
- **Project:** https://www.sdms.afrl.af.mil/index.php?collection=mstar
- **Organization:** DARPA / Air Force Research Lab
- **Year:** 1995–1997
- **Task:** Automatic target recognition (ATR)
- **Sensor:** SAR (X-band, 1 ft resolution)
- **Resolution:** 0.3 m (1 ft)
- **Size:** 2.4 GB; ~14,000 target chips
- **Classes:** 10 military vehicle categories
- **Coverage:** USA test ranges
- **License:** Public domain (US government)

### CaFFe (Change detection And Flood mapping with Flood-SAR)
- **HuggingFace:** https://huggingface.co/datasets/torchgeo/CaFFe
- **Paper:** https://arxiv.org/abs/2209.09701
- **Organization:** DLR / University of Florence
- **Year:** 2022
- **Task:** Flood extent mapping
- **Sensor:** Sentinel-1 (SAR), multiple other SAR sources
- **Resolution:** 6–20 m
- **Size:** 19,092 image pairs
- **Classes:** 2 (flooded / non-flooded)
- **Coverage:** Global (diverse flood events)
- **License:** CC-BY-4.0

---

## 9. Cloud Detection & Atmospheric

### CloudSEN12+
- **HuggingFace:** https://huggingface.co/datasets/isp-uv-es/CloudSEN12Plus
- **Project:** https://cloudsen12.github.io
- **Paper:** https://arxiv.org/abs/2202.04090
- **Organization:** Image & Signal Processing Group (UV)
- **Year:** 2022
- **Task:** Cloud and cloud shadow segmentation
- **Sensor:** Sentinel-2 (all 13 bands)
- **Resolution:** 10–60 m
- **Size:** 49,400 patches (512×512 px) — largest cloud dataset
- **Classes:** 4 (clear, thick cloud, thin cloud, cloud shadow)
- **Coverage:** Global stratified sample
- **License:** CC-BY-4.0

### 95-Cloud / 38-Cloud
- **GitHub:** https://github.com/SorourMo/95-Cloud-An-Extension-to-38-Cloud-Dataset
- **Paper:** https://ieeexplore.ieee.org/document/9394710
- **Organization:** Concordia University
- **Year:** 2020
- **Task:** Cloud segmentation
- **Sensor:** Landsat 8
- **Resolution:** 30 m
- **Size:** 34,701 patches (384×384 px)
- **Classes:** Cloud mask
- **Coverage:** Global
- **License:** CC-BY-4.0

### L8 Biome Cloud Validation
- **Project:** https://landsat.usgs.gov/landsat-8-cloud-cover-assessment-validation-data
- **Paper:** https://www.sciencedirect.com/science/article/pii/S0034425717301293
- **Organization:** USGS
- **Year:** 2017
- **Task:** Cloud & cloud shadow segmentation (benchmark)
- **Sensor:** Landsat 8
- **Resolution:** 15–30 m
- **Size:** 96 Landsat scenes
- **Classes:** 4 categories (clear, cloud, cloud shadow, snow/ice)
- **Coverage:** 12 global biomes
- **License:** CC0-1.0

---

## 10. Time Series & Temporal

### SeCo (Seasonal Contrast)
- **GitHub:** https://github.com/ServiceNow/seasonal-contrast
- **HuggingFace:** https://huggingface.co/datasets/torchgeo/SeasonalContrast
- **Paper:** https://arxiv.org/abs/2103.16607
- **Organization:** ServiceNow Research
- **Year:** 2021
- **Task:** Self-supervised pre-training on seasonal data
- **Sensor:** Sentinel-2
- **Resolution:** 10 m
- **Size:** 1 million patches (100K locations × 5 season samples)
- **Classes:** Unlabeled
- **Coverage:** Global
- **License:** CC-BY-4.0

### SEN12MS-CR & SEN12MS-CR-TS (Cloud Removal)
- **Project:** https://patricktum.github.io/cloud_removal/
- **Paper (CR):** https://ieeexplore.ieee.org/document/9211498
- **Paper (CR-TS):** https://ieeexplore.ieee.org/document/9691348
- **Organization:** TU Munich
- **Year:** 2020 / 2022
- **Task:** Multi-temporal cloud removal / reconstruction
- **Sensor:** Sentinel-1 (SAR), Sentinel-2 (MS)
- **Resolution:** 10 m
- **Size:** 175 globally distributed AOIs; ~122k patches (CR-TS)
- **Classes:** Pixel-level reconstructed cloud-free imagery
- **Coverage:** Global
- **License:** CC-BY-4.0

### TimeMatch
- **GitHub:** https://github.com/jnyborg/timematch
- **Zenodo:** https://zenodo.org/record/6350734
- **Paper:** https://arxiv.org/abs/2111.02682
- **Organization:** University of Copenhagen
- **Year:** 2022
- **Task:** Cross-region crop type classification (domain adaptation)
- **Sensor:** Sentinel-2 (time series)
- **Resolution:** 10 m
- **Size:** 1.4 million parcel time series across 4 European regions
- **Classes:** 8 crop categories
- **Coverage:** Austria, Denmark, France, Lithuania
- **License:** CC-BY-4.0

### Digital Typhoon
- **GitHub:** https://github.com/kitamoto-lab/digital-typhoon
- **Paper:** https://arxiv.org/abs/2311.02665
- **Organization:** National Institute of Informatics, Japan
- **Year:** 2023
- **Task:** Typhoon intensity classification & regression
- **Sensor:** Himawari geostationary satellite (infrared)
- **Resolution:** 5 km (resampled to 512×512 px per typhoon)
- **Size:** 189,364 images spanning 1,099 typhoons (1978–2022)
- **Classes:** 8 intensity levels (Saffir-Simpson equivalent)
- **Coverage:** Western Pacific Ocean
- **License:** CC-BY-4.0

---

## 11. Foundation Model Embeddings (Pre-computed)

Pre-computed vector embeddings at global scale, ready to use for downstream tasks without running inference.

### Major TOM Embeddings
- **HuggingFace:** https://huggingface.co/Major-TOM
- **Organization:** ESA Φ-lab
- **Year:** 2024
- **Type:** Patch embeddings (Sentinel-2 / Sentinel-1)
- **Spatial resolution:** 2.14–3.56 km per patch
- **Coverage:** Global
- **License:** CC-BY-SA-4.0

### Clay Model Embeddings
- **HuggingFace:** https://huggingface.co/datasets/made-with-clay/Clay-Embeddings
- **Project:** https://clay-foundation.github.io/model/
- **Organization:** Clay Foundation
- **Year:** 2024
- **Type:** Patch embeddings (Sentinel-2, Sentinel-1, NAIP, Landsat)
- **Spatial resolution:** 5.12 km per patch
- **Coverage:** Global
- **License:** ODC-By-1.0

### Google Satellite Embedding Dataset
- **Blog:** https://medium.com/google-earth/ai-powered-pixels-introducing-googles-satellite-embedding-dataset-31744c1f4650
- **Organization:** Google / DeepMind (AlphaEarth Foundations)
- **Year:** 2025
- **Type:** Pixel-level embeddings
- **Spatial resolution:** 10 m
- **Coverage:** Global
- **License:** CC-BY-4.0

### Tessera Embeddings
- **HuggingFace:** https://huggingface.co/datasets/Tessera-Earth/Tessera-Embeddings
- **Organization:** Tessera Earth
- **Year:** 2024
- **Type:** Pixel-level embeddings (Sentinel-2)
- **Spatial resolution:** 10 m
- **Coverage:** Global
- **License:** CC0-1.0

---

## 12. Benchmarks & Multi-Task Evaluation

### SATIN (Satellite Task-INdependent benchmark)
- **Project:** https://satinbenchmark.github.io
- **Paper:** https://arxiv.org/abs/2304.11619
- **Organization:** University of Cambridge
- **Year:** 2023
- **Task:** Zero-shot CLIP evaluation across 27 diverse RS tasks
- **Sensor:** Multi-sensor
- **Size:** 27 datasets, 100+ categories
- **Coverage:** Global
- **License:** CC-BY-4.0

### pangaea-bench
- **GitHub:** https://github.com/yurujaja/pangaea-bench
- **Paper:** https://arxiv.org/abs/2405.15982
- **Organization:** TU Munich / ESA Φ-lab
- **Year:** 2024
- **Task:** Unified benchmark for geospatial foundation models (7 tasks)
- **Sensor:** Multi-sensor
- **Coverage:** Global
- **License:** CC-BY-4.0

### PhilEO Bench (ESA)
- **HuggingFace:** https://huggingface.co/PhilEO-Community
- **GitHub:** https://github.com/ESA-PhiLab/PhilEO-Bench
- **Paper:** https://arxiv.org/abs/2401.04464
- **Organization:** ESA Φ-lab
- **Year:** 2024
- **Task:** Downstream evaluation (building density, road segmentation, land cover)
- **Sensor:** Sentinel-2
- **Resolution:** 10 m
- **Coverage:** Global
- **License:** CC-BY-4.0

### GEO-Bench
- **GitHub:** https://github.com/ServiceNow/geo-bench
- **Paper:** https://arxiv.org/abs/2306.03831
- **Organization:** ServiceNow Research / Mila
- **Year:** 2023
- **Task:** Standardised benchmark for geospatial ML (6 classification + 6 segmentation tasks)
- **Sensor:** Multi-sensor
- **Coverage:** Global
- **License:** CC-BY-4.0

---

## 13. Large-Scale Additions From GitHub, Kaggle, and Hugging Face

Large datasets added after checking GitHub, Kaggle, Hugging Face, and official project pages. This section intentionally avoids tiny teaching datasets.

### EarthView
- **HuggingFace:** https://huggingface.co/datasets/satellogic/EarthView
- **GitHub:** https://github.com/satellogic/satellogic-earthview
- **Paper:** https://arxiv.org/abs/2501.08111
- **Organization:** Satellogic / collaborators
- **Year:** 2025
- **Task:** Self-supervised pre-training, multisensor representation learning
- **Sensor:** Satellogic, NEON, Sentinel-1, Sentinel-2
- **Resolution:** 0.1 m–20 m depending on subset
- **Size:** Tens of millions of samples across modalities; includes ~6M Satellogic, ~10M Sentinel-2, ~5.2M Sentinel-1, and ~1M NEON samples
- **Classes:** Unlabeled
- **Coverage:** Global / multi-continental
- **License:** See Hugging Face dataset card

### HLS Global Dataset / Prithvi-EO Training Data
- **Project:** https://hls.gsfc.nasa.gov
- **NASA Earthdata:** https://www.earthdata.nasa.gov/data/projects/hls
- **Paper:** https://arxiv.org/abs/2412.02732
- **Organization:** NASA IMPACT / NASA GSFC / IBM
- **Year:** 2024
- **Task:** Foundation model pre-training, time-series EO
- **Sensor:** Harmonized Landsat 8/9 and Sentinel-2
- **Resolution:** 30 m
- **Size:** Prithvi-EO-2.0 reports ~4.2M global time-series samples for training and 45,568 validation samples
- **Classes:** Unlabeled
- **Coverage:** Global
- **License:** NASA open data terms

### SSL4EO-S12 v1.1
- **HuggingFace:** https://huggingface.co/datasets/embed2scale/SSL4EO-S12-v1.1
- **GitHub:** https://github.com/zhu-xlab/SSL4EO-S12
- **Paper:** https://arxiv.org/abs/2503.00168
- **Organization:** TU Munich / Zhu Lab
- **Year:** 2025
- **Task:** Multimodal, multitemporal pre-training
- **Sensor:** Sentinel-1, Sentinel-2
- **Resolution:** 10 m
- **Size:** Large-scale global seasonal patch dataset
- **Classes:** Unlabeled
- **Coverage:** Global
- **License:** CC-BY-4.0

### RS5M
- **HuggingFace:** https://huggingface.co/datasets/omlab/RS5M
- **GitHub:** https://github.com/om-ai-lab/RS5M
- **Paper:** https://arxiv.org/abs/2306.11300
- **Organization:** OM AI Lab
- **Year:** 2024
- **Task:** Vision-language pre-training, image-text retrieval, zero-shot classification
- **Sensor:** Remote-sensing image collections from multiple sources
- **Resolution:** Mixed
- **Size:** 5 million image-text pairs
- **Classes:** Free-text captions
- **Coverage:** Global / mixed
- **License:** See repository and dataset card

### RSTeller
- **HuggingFace:** https://huggingface.co/datasets/SlytherinGe/RSTeller_legacy
- **GitHub:** https://github.com/SlytherinGe/RSTeller
- **Paper:** https://arxiv.org/abs/2408.14744
- **Organization:** RSTeller authors
- **Year:** 2024
- **Task:** Vision-language pre-training and instruction tuning
- **Sensor:** Remote-sensing imagery with generated rich linguistic annotations
- **Resolution:** Mixed
- **Size:** Large-scale image-text dataset; Hugging Face legacy shard includes millions of records
- **Classes:** Captions, region descriptions, instruction-style text
- **Coverage:** Global / mixed
- **License:** See dataset card

### BigEarthNet.txt
- **HuggingFace:** https://huggingface.co/datasets/BIFOLD-BigEarthNetv2-0/BigEarthNet.txt
- **Project:** https://txt.bigearth.net
- **Paper:** https://arxiv.org/abs/2603.29630
- **Organization:** BIFOLD / BigEarthNet team
- **Year:** 2026
- **Task:** Vision-language benchmarking, captioning, VQA, referring expression grounding
- **Sensor:** Sentinel-1, Sentinel-2
- **Resolution:** 10 m
- **Size:** 464,044 co-registered S1/S2 image pairs with ~9.6M text annotations
- **Classes:** Captions, VQA pairs, referring expressions
- **Coverage:** Europe
- **License:** See dataset card

### FIT-RS
- **HuggingFace:** https://huggingface.co/datasets/ll-13/FIT-RS
- **GitHub:** https://github.com/Luo-Z13/SkySenseGPT
- **Paper:** https://arxiv.org/abs/2406.10100
- **Organization:** SkySenseGPT authors
- **Year:** 2024
- **Task:** Fine-grained instruction tuning for remote-sensing VLMs
- **Sensor:** Remote-sensing image collections
- **Resolution:** Mixed
- **Size:** ~1.8M instruction-tuning samples
- **Classes:** Instruction-answer pairs
- **Coverage:** Mixed
- **License:** See dataset card

### RS-GPT4V
- **GitHub:** https://github.com/GeoX-Lab/RS-GPT4V
- **Paper:** https://arxiv.org/abs/2406.09385
- **Organization:** GeoX Lab
- **Year:** 2024
- **Task:** Multimodal instruction-following for remote-sensing image understanding
- **Sensor:** Remote-sensing imagery
- **Resolution:** Mixed
- **Size:** ~991k instruction samples
- **Classes:** Instruction-answer pairs
- **Coverage:** Mixed
- **License:** See repository

### SkyEye-968k
- **HuggingFace:** https://huggingface.co/datasets/ZhanYang-nwpu/SkyEye-968k
- **GitHub:** https://github.com/ZhanYang-nwpu/SkyEyeGPT
- **Paper:** https://arxiv.org/abs/2401.09712
- **Organization:** Northwestern Polytechnical University
- **Year:** 2024
- **Task:** Remote-sensing vision-language instruction tuning
- **Sensor:** Remote-sensing imagery
- **Resolution:** Mixed
- **Size:** 968k instruction-tuning samples
- **Classes:** Instruction-answer pairs
- **Coverage:** Mixed
- **License:** See dataset card

### MMRS-1M
- **GitHub:** https://github.com/wivizhang/EarthGPT
- **Paper:** https://arxiv.org/abs/2401.16822
- **Organization:** EarthGPT authors
- **Year:** 2024
- **Task:** Multisensor remote-sensing MLLM training
- **Sensor:** Multisensor remote-sensing imagery
- **Resolution:** Mixed
- **Size:** >1M multimodal instruction samples
- **Classes:** Instruction-answer pairs
- **Coverage:** Mixed
- **License:** See repository

### DDFAV
- **GitHub:** https://github.com/HaodongLi2024/rspope
- **Paper:** https://arxiv.org/abs/2411.02733
- **Organization:** DDFAV authors
- **Year:** 2024
- **Task:** Remote-sensing large vision-language model dataset and evaluation benchmark
- **Sensor:** Remote-sensing imagery
- **Resolution:** Mixed
- **Size:** 27.7k high-quality samples
- **Classes:** Vision-language instructions / evaluation labels
- **Coverage:** Mixed
- **License:** See repository

### VRSBench
- **HuggingFace:** https://huggingface.co/datasets/xiang709/VRSBench
- **GitHub:** https://github.com/lx709/VRSBench
- **Paper:** https://arxiv.org/abs/2406.12384
- **Organization:** VRSBench authors
- **Year:** 2024
- **Task:** Remote-sensing captioning, VQA, and visual grounding benchmark
- **Sensor:** Remote-sensing imagery
- **Resolution:** Mixed
- **Size:** 29,614 human-verified remote-sensing images
- **Classes:** Captions, question-answer pairs, grounding annotations
- **Coverage:** Mixed
- **License:** See dataset card

### DASP
- **HuggingFace:** https://huggingface.co/datasets/RichardErkhov/DASP
- **Organization:** Richard Erkhov
- **Year:** 2025
- **Task:** Large-scale cloud-free Sentinel-2 imagery for analysis and model training
- **Sensor:** Sentinel-2
- **Resolution:** 10–60 m depending on band
- **Size:** Curated from over 30 million Sentinel-2 images
- **Classes:** Unlabeled
- **Coverage:** Near-global Sentinel-2 land coverage
- **License:** CC-BY-SA-3.0

### Dynamic World
- **Project:** https://dynamicworld.app
- **GitHub:** https://github.com/google/dynamicworld
- **Paper:** https://www.nature.com/articles/s41597-022-01307-4
- **Organization:** Google / World Resources Institute
- **Year:** 2022
- **Task:** Near-real-time global land-cover labels
- **Sensor:** Sentinel-2
- **Resolution:** 10 m
- **Size:** Global near-real-time probability maps and class labels
- **Classes:** 9 land-cover classes
- **Coverage:** Global
- **License:** CC-BY-4.0

### ESA WorldCover
- **Project:** https://esa-worldcover.org/en/data-access
- **GitHub:** https://github.com/ESA-WorldCover
- **Organization:** ESA
- **Year:** 2020–2021 products
- **Task:** Global land-cover mapping
- **Sensor:** Sentinel-1, Sentinel-2
- **Resolution:** 10 m
- **Size:** Global 10 m land-cover maps
- **Classes:** 11 land-cover classes
- **Coverage:** Global
- **License:** CC-BY-4.0

### Hansen Global Forest Change
- **Project:** https://glad.earthengine.app/view/global-forest-change
- **EarthEngine:** https://developers.google.com/earth-engine/datasets/catalog/UMD_hansen_global_forest_change_2024_v1_12
- **Paper:** https://www.science.org/doi/10.1126/science.1244693
- **Organization:** University of Maryland GLAD
- **Year:** 2013–2024 updates
- **Task:** Forest extent and annual forest-loss monitoring
- **Sensor:** Landsat
- **Resolution:** 30 m
- **Size:** Global annual forest change product
- **Classes:** Tree cover, forest loss, forest gain
- **Coverage:** Global
- **License:** See Earth Engine catalog

### MapBiomas
- **Project:** https://brasil.mapbiomas.org/colecoes-mapbiomas/
- **GitHub:** https://github.com/mapbiomas/user-toolkit
- **EarthEngine:** https://gee-community-catalog.org/projects/mapbiomas/
- **Organization:** MapBiomas network
- **Year:** Annual collections
- **Task:** Annual land-use and land-cover time series
- **Sensor:** Landsat and other EO sources
- **Resolution:** 30 m; newer 10 m products for selected collections
- **Size:** Continental/national annual land-cover products
- **Classes:** Land-use and land-cover classes vary by collection
- **Coverage:** Brazil and other regional MapBiomas initiatives
- **License:** See project terms

### OpenSentinelMap
- **Paper:** https://openaccess.thecvf.com/content/CVPR2022W/EarthVision/papers/Johnson_OpenSentinelMap_A_Large-Scale_Land_Use_Dataset_Using_OpenStreetMap_and_Sentinel-2_CVPRW_2022_paper.pdf
- **Organization:** Vision Systems Inc. / collaborators
- **Year:** 2022
- **Task:** Large-scale land-use classification using OSM labels
- **Sensor:** Sentinel-2
- **Resolution:** 10 m
- **Size:** Large-scale Sentinel-2 land-use dataset derived from OpenStreetMap
- **Classes:** OSM-derived land-use classes
- **Coverage:** Large geographic coverage
- **License:** See paper/project terms

### BigEarthNet Kaggle Mirror
- **Kaggle:** https://www.kaggle.com/datasets/javidtheimmortal/bigearthnetsentinel1
- **Project:** https://bigearth.net
- **Paper:** https://arxiv.org/abs/1902.06148
- **Organization:** TU Berlin
- **Year:** 2019 / v2 2023
- **Task:** Multi-label scene classification
- **Sensor:** Sentinel-1, Sentinel-2
- **Resolution:** 10–60 m
- **Size:** 590,326 patches in v1; 549,488 S1/S2 patch pairs in v2
- **Classes:** CORINE-derived land-cover classes
- **Coverage:** Europe
- **License:** CDLA-Permissive-1.0 / see BigEarthNet terms

### DOTA Kaggle Mirror
- **Kaggle:** https://www.kaggle.com/datasets/chandlertimm/dota-data
- **Project:** https://captain-whu.github.io/DOTA/
- **Paper:** https://arxiv.org/abs/1711.10398
- **Organization:** Wuhan University
- **Year:** 2018+
- **Task:** Oriented object detection in aerial imagery
- **Sensor:** Aerial / satellite imagery
- **Resolution:** Mixed
- **Size:** Large-scale aerial object detection dataset
- **Classes:** Object detection classes including vehicles, ships, planes, courts, harbors, bridges
- **Coverage:** Global / mixed
- **License:** Research use; see DOTA terms

### DeepGlobe Land Cover Kaggle Mirror
- **Kaggle:** https://www.kaggle.com/datasets/balraj98/deepglobe-land-cover-classification-dataset
- **Paper:** https://arxiv.org/abs/1805.06561
- **Organization:** DeepGlobe Challenge
- **Year:** 2018
- **Task:** Land-cover semantic segmentation
- **Sensor:** DigitalGlobe
- **Resolution:** Sub-meter
- **Size:** Large high-resolution segmentation benchmark
- **Classes:** 7 land-cover classes
- **Coverage:** Global / mixed
- **License:** DeepGlobe / DigitalGlobe challenge terms

### SpaceNet Kaggle / Hugging Face Mirrors
- **Kaggle:** https://www.kaggle.com/datasets/sabermalek/spacenetsi
- **HuggingFace:** https://huggingface.co/datasets/aialliance/spacenet7
- **Project:** https://spacenet.ai/datasets/
- **GitHub:** https://github.com/SpaceNetChallenge
- **Organization:** SpaceNet partners
- **Year:** 2016–2020
- **Task:** Building footprints, roads, off-nadir mapping, multi-temporal urban analysis
- **Sensor:** WorldView, Planet, other high-resolution imagery
- **Resolution:** Sub-meter to few-meter
- **Size:** Multi-city, multi-challenge large benchmark series
- **Classes:** Buildings, roads, urban change
- **Coverage:** Multiple global cities
- **License:** CC-BY-SA-4.0 / challenge-specific terms

### xView Kaggle Mirror
- **Kaggle:** https://www.kaggle.com/datasets/ollypowell/xview-yolo-dataset
- **Project:** http://xviewdataset.org
- **Paper:** https://arxiv.org/abs/1802.07856
- **Organization:** DIU / xView team
- **Year:** 2018
- **Task:** Large-scale object detection in overhead imagery
- **Sensor:** WorldView-3
- **Resolution:** 0.3 m
- **Size:** >1M object instances across >1,400 km²
- **Classes:** 60 object classes
- **Coverage:** Global / mixed
- **License:** Registration required; Kaggle mirror is converted YOLO format

---

## 14. Data Platforms & Hubs

Large-scale platforms hosting curated geospatial datasets — starting points for discovery.

| Platform | URL | Highlights |
|----------|-----|-----------|
| Radiant MLHub | https://mlhub.earth | Labelled EO datasets, open API, free |
| Microsoft Planetary Computer | https://planetarycomputer.microsoft.com | Landsat, Sentinel, NAIP, MODIS, STAC catalog |
| Google Earth Engine | https://developers.google.com/earth-engine/datasets | 900+ public datasets, petabyte-scale |
| AWS Registry of Open Data | https://registry.opendata.aws/?search=satellite | Sentinel-2, NAIP, SpaceNet, Landsat archives |
| Copernicus Data Space | https://dataspace.copernicus.eu | Official ESA Sentinel archive (free access) |
| USGS EarthExplorer | https://earthexplorer.usgs.gov | Landsat, SRTM DEM, aerial photography |
| NASA Earthdata | https://search.earthdata.nasa.gov | MODIS, VIIRS, SMAP, GPM, and more |
| HuggingFace (geospatial) | https://huggingface.co/datasets?modality=geospatial | 320+ geospatial datasets, growing rapidly |
| TorchGeo Datasets | https://torchgeo.readthedocs.io | 150+ benchmark datasets with PyTorch loaders |

---

## 15. Surveys & Dataset Lists

- Awesome Satellite Imagery Datasets (chrieke): https://github.com/chrieke/awesome-satellite-imagery-datasets
- Satellite Image Deep Learning (robmarkcole): https://github.com/robmarkcole/satellite-image-deep-learning
- RS Foundation Model Datasets (Jack-bo1220): https://github.com/Jack-bo1220/Awesome-Remote-Sensing-Foundation-Models
- EarthNets Dataset Survey: https://earthnets.github.io
- Survey of GeoAI Datasets (2024): https://arxiv.org/abs/2403.02935
