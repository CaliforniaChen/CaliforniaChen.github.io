---
title: "TeethAlign3D Dataset"
collection: teaching
excerpt: "A benchmark dataset, called **TeethAlign3D**, is a 3D dental dataset for orthodontic treatment planning, containing 3D dental models of multiple cases and the tooth alignment target matrices. This dataset is mainly used for tooth alignment optimization and visual analysis in orthodontic treatment. It can be downloaded from [Zenodo](https://zenodo.org/records/15834700). <br/><img src='/../files/DatasetTeethAlign3D/teaser.jpg'>"
type: "Released with ICCV 2025 paper"
permalink: /datasets/TeethAlign3D
venue: "Free for non-commercial use"
date: 2025-07-01
location: #"City, Country"
---

Introducation
======
The dataset, called **TeethAlign3D**, is a 3D dental dataset for orthodontic treatment planning, containing 3D dental models of multiple cases and the tooth alignment target matrices. This dataset is mainly used for tooth alignment optimization and visual analysis in orthodontic treatment. It can be downloaded from [Zenodo](https://zenodo.org/records/15834700). Evaluations with this dataset can be found in our [ICCV 2025 paper](https://californiachen.github.io/publications/2025ICCV/).


Dataset Structure
======
TeethAlign3D/
├── data_738/
├── data_739/
├── ...
├── data_794/
│   ├── crown/
│   │   ├── up/         # Maxillary tooth crown model (from the labial perspective, from left to right)
│   │   │   ├── 1.stl     # The third molar on the upper left
│   │   │   ├── 2.stl     # The second molar on the upper left
│   │   │   ├── 3.stl     # The first molar on the upper left
│   │   │   ├── 4.stl     # The second premolar on the upper left
│   │   │   ├── 5.stl     # The first premolar on the upper left
│   │   │   ├── 6.stl     # The canine on the upper left
│   │   │   ├── 7.stl     # The lateral incisor on the upper left
│   │   │   ├── 8.stl     # The central incisor on the upper left
│   │   │   ├── 9.stl     # The central incisor on the upper right
│   │   │   ├── 10.stl   # The lateral incisor on the upper right
│   │   │   ├── 11.stl   # The canine on the upper right
│   │   │   ├── 12.stl   # The first premolar on the upper right
│   │   │   ├── 13.stl   # The second premolar on the upper right
│   │   │   ├── 14.stl   # The first molar on the upper right
│   │   │   ├── 15.stl   # The second molar on the upper right
│   │   │   └── 16.stl   # The third molar on the upper right
│   │   └── down/        # Mandibular Tooth Crown Model (from the labial view, from right to left)
│   │       ├── 17.stl    # The third molar on the lower right
│   │       ├── 18.stl    # The second molar on the lower right
│   │       ├── 19.stl    # The first molar on the lower right
│   │       ├── 20.stl    # The second premolar on the lower right
│   │       ├── 21.stl    # The first premolar on the lower right
│   │       ├── 22.stl    # The canine tooth on the lower right
│   │       ├── 23.stl    # The lateral incisor on the lower right
│   │       ├── 24.stl    # The central incisor on the lower right
│   │       ├── 25.stl    # The central incisor on the lower left
│   │       ├── 26.stl    # The lateral incisor on the lower left
│   │       ├── 27.stl    # The canine tooth on the lower left
│   │       ├── 28.stl    # The first premolar on the lower left
│   │       ├── 29.stl    # The second premolar on the lower left
│   │       ├── 30.stl    # The first molar on the lower left
│   │       ├── 31.stl    # The second molar on the lower left
│   │       └── 32.stl    # The third molar on the lower left
│   ├── tooth/
│   │   ├── up/          # Maxillary Closed Tooth Model
│   │   └── down/    # Mandibular Closed Dental Model
│   └── target_matrix.txt # Tooth Arrangement Target Transformation Matrix
└── ...

Data Content Description
======
1. Dental Crown Model (crown/)
Format: STL file format
Content: Triangular mesh model of the dental crown 

2. Complete Tooth Model (tooth/)
Format: STL file format
Content: Complete closed triangular mesh model of the tooth 

3. Target Matrix File (target_matrix.txt)
Format: Text file
Content: Target transformation matrix for each tooth after tooth arrangement
Format Description:
Tooth Number R00 R01 R02 0 R10 R11 R12 0 R20 R21 R22 0 Tx  Ty  Tz  1
 Where:
    - Tooth Number: Corresponding to the number of the STL file (1 - 32)
    - M11 - M44: 16 elements of the 4×4 homogeneous transformation matrix
Treatment of Missing Teeth: For missing teeth, the row with the tooth number will not be included in target_matrix.txt.
 

Tooth Numbering System
======
Maxillary Teeth (up/) - Numbered from left to right from the labial view
- 1 - 8: Left - side teeth (from the left third molar to the left central incisor)
- 9 - 16: Right - side teeth (from the right central incisor to the right third molar) 

Mandibular Teeth (down/) - Numbered from right to left from the labial view
- 17 - 24: Right - side teeth (from the right third molar to the right central incisor)
- 25 - 32: Left - side teeth (from the left central incisor to the left third molar)
 

Dataset Scale
======
- Number of Cases: 837 cases (data_001 to data_837)
- Each Case Includes:
    - Dental Crown STL files (up to 16 in the maxilla: 1 - 16, up to 16 in the mandible: 17 - 32)
    - Closed Tooth STL files (up to 16 in the maxilla: 1 - 16, up to 16 in the mandible: 17 - 32)
    - 1 target matrix file (contains transformation matrices for each tooth)
    Note:Our dataset supports and contains missing teeth. Their STL files and matrix rows in the target matrix are empty.
  
Application Scenarios
======
1. Orthodontic Treatment Planning: Optimize tooth alignment based on the target matrix
2. 3D Visualization: 3D display and analysis of tooth models
3. Biomechanical Analysis: Stress analysis of complete tooth models
4. Aesthetic Evaluation: Morphological aesthetic analysis of dental crown models
5. Machine Learning Training: Used for training AI models such as tooth segmentation and registration
 

Technical Specifications
======
- File Format: STL (Stereolithography)
- Mesh Type: Triangular mesh
- Coordinate System: Right - hand coordinate system
- Unit: Millimeter (mm)
- Accuracy: High - precision medical - grade scanned data
 

Potential uses:
======
1. Data Integrity: Ensure that the crown, tooth, and target_matrix.txt files for each case are complete.
2. File Association: The STL file number corresponds one - to - one with the tooth number in target_matrix.txt.
3. Coordinate System: All models use a unified coordinate system to facilitate the application of transformation matrices.
4. Missing Teeth Situation: There may be missing teeth in the case, the corresponding STL file may not exist, and the transformation matrix of the tooth will not be included in target_matrix.txt.
5. Data Verification: It is recommended to check the integrity of the STL file for each case before use to ensure the existence of the required tooth models.

Citation:
======
Zhenxing Dong, Jiazhou Chen*. &quot; Transformer-based Tooth Alignment Prediction with Occlusion and Collision Constraints.&quot; <i>ICCV</i>. 2025. 
