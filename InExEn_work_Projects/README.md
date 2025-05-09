# InExEn Work Projects
Here showcases various research projects with detailed documentation on methodology, findings, and tools used.

## Table of Contents

1. [Lutetia](#-lutetia)
2. [ReID - Advancing AI Detection for Reliable Polyp Re-identification in Colonoscopy](#-reid---advancing-ai-detection-for-reliable-polyp-re-identification-in-colonoscopy)
3. [Swarm Learning](#-swarm-learning)

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
- **Algorithm & Methods:** Classification, Active Learning, Grad-CAM Visualization.
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

## 📌 ReID - Advancing AI Detection for Reliable Polyp Re-identification in Colonoscopy

### 📚 Description
This project initially aimed to develop an add-on feature for an automatic colonoscopy report generation system, focusing on two core functions: **calculating the total number of polyps** and **extracting representative images**. To achieve this, a polyp identification framework was designed using a **Siamese neural network** in combination with **HDBSCAN clustering**, enabling the system to match and re-identify polyps across frames.

As a next step, the goal is to extend this capability into a real-time application that can be integrated directly into the colonoscopy workflow, assisting clinicians during examinations by providing immediate feedback on polyp detection and identification.

### 🛠 Methodology
- Data Collection & Annotation
  - Collected colonoscopy images from examination videos.
  - Annotated polyp number and time frame in examinations.
- Neural Network Design
  - Developed a classification model capable of extracting key/relevant features of colonoscopy images.
  - Reduced the distance between similar images while increasing the distance between dissimilar ones in a high-dimensional space.
- Work Pipeline Design with Clustering Method
  - Designed a workflow from importing video frames to output a final report.
  - Evaluated correctness and usability

### 📊 Results & Findings
- The pipeline was evaluated on 15 full colonoscopy examinations.
- Achieved the following average performance metrics:
  - Adjusted Mutual Information (AMI): 0.89
  - Accuracy: 0.83
  - F1 Score: 0.77
- Key observation: Shorter time gaps between polyps often lead to more similar surrounding structures, resulting in reduced prediction accuracy.
- Since the automatic report generation system can already detect the timing of interventions and the tools used, this information can be leveraged to improve re-identification using conditional strategies.
- While the results are promising, they have not yet reached a level suitable for practical application.

- **This work was presented at the 2024 Deutsche Gesellschaft für Gastroenterologie, Verdauungs- und Stoffwechselkrankheiten (DGVS) and the 2024 United European Gastroenterology (UEG) conferences.**
- **This work was presented at the 2023 Deutsche Gesellschaft für Gastroenterologie, Verdauungs- und Stoffwechselkrankheiten (DGVS) and the 2023 United European Gastroenterology (UEG) conferences.**

### 🔧 Technologies & Tools Used
- **Algorithm & Methods:** Clustering, Classification, Segmentation, Attention mechanisms, Siamese neural network.
- **Programming Languages:** Python.
- **Libraries & Frameworks:** PyTorch, SciPy, Numpy, Pandas.
- **Development Tools:** Jupyter Notebook, VS Code.
- **Version Control:** None.

### 📂 Dataset & Resources
- Data source(s): The data is a private dataset collected from 7 different examination centers.
- Preprocessing steps:
  - Image Cropping
  - Image Resizing
- Relevant papers or references
  - [Assisted documentation as a new focus for artificial intelligence in endoscopy: the precedent of reliable withdrawal time and image reporting](https://pmc.ncbi.nlm.nih.gov/articles/PMC11321719/)
  - [A deep learning-based system for real-time image reporting during esophagogastroduodenoscopy: a multicenter study](https://pubmed.ncbi.nlm.nih.gov/35272381/)
  - [ArcFace: Additive Angular Margin Loss for Deep Face Recognition](https://arxiv.org/abs/1801.07698)
  - [Exploring Simple Siamese Representation Learning](https://arxiv.org/abs/2011.10566)
  - [Person re-identification based on deep learning — An overview](https://www.sciencedirect.com/science/article/abs/pii/S1047320321002765)


### 🚀 Future Work or what if I can start over?

If I had the opportunity to start the project again, I would:

1) Explore the use of real-time detection by implementing [Meta's Segment Anything Model 2 (SAM 2)](https://ai.meta.com/sam2/), which I believe could help overcome the limitations of Tracktor++, especially in tracking objects that temporarily disappear.
2) Focus on improving the system’s ability to distinguish individual polyps, considering the challenge that polyps may appear with different shapes from various viewing angles.
3) Allocate more time to experimenting with advanced segmentation-tracking integration methods to better support real-time performance during colonoscopy.

Before I left the lab, I shared this idea and my work with my colleagues. I believe they are well-equipped to continue developing the technology and push it forward, even in my absence.

---

## 📌 Swarm Learning

### 📚 Description
This project explores the potential of Swarm Learning for AI-assisted polyp detection and diagnostic enhancement in endoscopic procedures. It aims to improve the performance and robustness of AI models by leveraging distributed learning across multiple institutions, without sharing patient data. Due to confidentiality constraints, I will only present the data cleaning and preprocessing aspects of this project.

### 🔧 Technologies & Tools Used
- **Algorithm & Methods:** Binary Classification.
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


