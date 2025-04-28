# InExEn Work Projects
Here showcases various research projects with detailed documentation on methodology, findings, and tools used.

## Table of Contents

1. [Lutetia](https://github.com/BelleJohn/Work-Experience-Demos/edit/main/InExEn_work_Projects/README.md#lutetia)
2. [ReID](https://github.com/BelleJohn/Work-Experience-Demos/edit/main/InExEn_work_Projects/README.md#-reid)
3. [Swarm Learning](https://github.com/BelleJohn/Work-Experience-Demos/edit/main/InExEn_work_Projects/README.md#-reid)

---

## 📌  Lutetia

### 📚 Description
Lutetia is a platform designed to improve the classification consistency of colorectal polyps and support physician training. By combining real and synthetic colonoscopy images, Lutetia is promising to facilitate expert consensus and provide tailored learning workflows for junior physicians. The project aims to address critical gaps in polyp classification reliability, which directly impacts treatment decisions and patient outcomes.

### 🛠 Methodology

- Data Collection & Annotation
  - Collected a dataset of real colonoscopy images.
  - Senior physicians annotated polyp types based on the Paris classification.
  - Consensus levels among annotators were calculated to establish gold-standard labels for training.

- Synthetic Image Generation
  - Developed an inpainting model capable of generating synthetic colonoscopy images.
  - Focused on creating realistic variations of different polyp types while preserving the original background context.

- Training Workflow Design
  - Designed a comparative training module:
    - One group of junior physicians is trained with AI-generated images.
    - Another group is trained with traditional teaching materials.
  - This setup allows for direct evaluation of the effectiveness of AI-generated data in improving classification accuracy and training outcomes.

### 📊 Results & Findings

- Current Status <br/>
The project is ongoing. Although the full annotation results from senior physicians were not collected before the project handover, the system's infrastructure—training platform, teaching workflow, and model training workflow, which have been developed and delivered to the team, enable smooth project continuation.

- Presentation
  - This work has been presented in the **2024 Deutsche Gesellschaft für Gastroenterologie, Verdauungs- und Stoffwechselkrankheiten(DGVS)** conference.

### 🔧 Technologies & Tools Used
- **Algorithm:** Classification, Grad-CAM Visualization.
- **Programming Languages:** Python.
- **Libraries & Frameworks:** PyTorch, Numpy, FastAPI, SQLAlchemy.
- **Development Tools:** VS Code, Bash terminal, Linux, Windows.
- **Version Control:** Git, GitHub
- **Database:** MariaDB, SQLite.

### 📂 Dataset & Resources

- Data source(s):
  - Real colonoscopy images collected from clinical practice.
  - Public datasets
- Relevant papers or references:
  - [High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752)
  - [Polyp Morphology: An Interobserver Evaluation for the Paris Classification Among International Experts](https://journals.lww.com/ajg/abstract/2015/01000/polyp_morphology__an_interobserver_evaluation_for.24.aspx)
  - [Comprehensive review of publicly available colonoscopic imaging databases for artificial intelligence research: availability, accessibility, and usability](https://www.sciencedirect.com/science/article/pii/S0016510722019526)

### 🚀 Future Work or what if I can start over?

- Complete the collection and analysis of senior physician annotations.
- Conduct full-scale evaluation comparing AI-trained and traditionally-trained junior physicians.
- Improve the inpainting model to better handle rare polyp types.

---

## 📌 ReID

### 📚 Description
𝐀𝐝𝐯𝐚𝐧𝐜𝐢𝐧𝐠 𝐀𝐈 𝐝𝐞𝐭𝐞𝐜𝐭𝐢𝐨𝐧 for reliable polyp re-identification in endoscopy. 

### 🛠 Methodology

Describe the approach, experimental setup, datasets, models, and analysis techniques used.

### 📊 Results & Findings

- Key insights and discoveries
- Performance metrics and evaluation
- Visualizations (if applicable)
- This work was presented at the 2024 Deutsche Gesellschaft für Gastroenterologie, Verdauungs- und Stoffwechselkrankheiten (DGVS) and the 2024 United European Gastroenterology (UEG) conferences.

### 🔧 Technologies & Tools Used
- **Algorithm:** Clustering, Classification, Segmentation.
- **Programming Languages:** Python.
- **Libraries & Frameworks:** PyTorch, SciPy, Numpy, Pandas.
- **Development Tools:** Jupyter Notebook, VS Code.
- **Version Control:** None.

### 📂 Dataset & Resources

- Data source(s)
- Preprocessing steps
- Relevant papers or references 

### 🚀 Future Work or what if I can start over?

Discuss potential improvements, next steps, and open questions for future research.

---

## 📌 Swarm Learning

### 📚 Description
This project explores the potential of Swarm Learning for AI-assisted polyp detection and diagnostic enhancement in endoscopic procedures. It aims to improve the performance and robustness of AI models by leveraging distributed learning across multiple institutions, without sharing patient data. Due to confidentiality constraints, I will only present the data cleaning and preprocessing aspects of this project.

### 🔧 Technologies & Tools Used
- **Algorithm:** Binary Classification.
- **Programming Languages:** Python.
- **Libraries & Frameworks:** PyTorch, SciPy.
- **Development Tools:** Jupyter Notebook, Linux.
- **Version Control:** Git, GitHub

### 📂 Dataset & Resources
- Private dataset collected from Universitätsklinikum Würzburg, Universitätsklinikum Hamburg, and Universitätsklinikum Aachen.
- Preprocessing steps
  - Blur Detection
  - Image Cropping:<br/>
  Cropped images to focus on relevant regions of interest, reducing noise and improving model performance. This step is done by my colleague, [Dr. Kafetzis](https://github.com/iokaf?page=2&tab=repositories). Dr. Kafetzis has developed an excellent cropping tool specifically designed to handle colonoscopy images from different imaging systems. If you would like access to the tool, please feel free to contact him directly.
  - Duplicate Removal: <br/>
  Identified and removed duplicate images to avoid redundancy and improve training efficiency.
  - Image Resizing: <br/>
  Standardized image dimensions to ensure compatibility across the training dataset and improve model convergence. This step is done in the model structure, not using an extra tool.
- Relevant papers/references:
  - [Swarm learning for decentralized artificial intelligence in cancer histopathology](https://www.nature.com/articles/s41591-022-01768-5)

### 🚀 Future Work or what if I can start over?

If I had the opportunity to start the Swarm Learning project again, I would:

1) Approach it by first establishing a clear standard for selecting training images to ensure consistent data quality for each center. 
2) Prioritize developing preprocessing tools to streamline image preparation and improve model performance.
3) Invest more time in deepening my understanding of distributed training models, including their limitations and potential areas for improvement. <br/>

Although I did not have full permissions to modify the underlying software and system, I could still proactively identify challenges and offer practical suggestions to help move the project forward. 


---


