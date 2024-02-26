## **SPACE SIEVE** (Using types of R-CNN Machine Learning Techniques to classify space debris from functioning satellites)


### **Team**

| Team Members                   | GitHub ID            |
|--------------------------------|----------------------|
| **Rishi Manohar Manoharan *(POC)***| ***RishiManohar*** |
| Rishikesh Ramesh               | *rishikesh-2809*     |
| Subhiksha Murugesan            | *Subhiksha0700*      |
| Nagul Pandian                  | *CruNt*              |
| Nithish Kumar Senthil Kumar    | *Nithish1201*        |

### **Introduction**

Our objective is to create a tool that can automatically classify objects in space as either operational satellites or as debris, based on the analysis of space images. This involves distinguishing between functional equipment and non-functional fragments or discarded parts floating in orbit.

By merging two datasets, we aim to use debris of different size, ensuring that our analysis remains robust against challenges posed by collisions and subsequent fragmentation of debris.

Everyone should care. Everyone who uses a smartphone, watches the weather forecast, or relies on GPS navigation should care because satellites help make all these things (and more) work smoothly. But space is getting crowded with broken parts and unused satellites. These can crash into the useful satellites, causing lots of problems. Adding more satellites to the already crowded space poses risks and complicates enhancing global communication networks. Additionally, this project plays a vital role in effectively addressing space debris by employing methodologies such as Active Debris Removal (ADR) and Solar Sails.

### **Literature Review**

The literature survey on space debris detection and classification reveals significant advancements and diverse methodologies. 

The first paper, *"Space Debris Detection with Fast Grid-Based Learning,"* demonstrates a deep learning-based approach emphasizing speed and accuracy in identifying space debris, achieving remarkable results in both synthetic and real data scenarios. The second paper, *"Space Objects Classification Techniques: A Survey,"* provides a comprehensive review of various techniques used for classifying space objects, highlighting the effectiveness of deep learning algorithms, particularly CNNs, in distinguishing between different types of space objects based on light curve data.

Our methodology advances beyond previous studies by implementing comprehensive preprocessing, including image resizing, augmentation, format standardization, and noise reduction, coupled with Mask-RCNN for refined object detection and segmentation. Additionally, we're developing a custom Convolutional Neural Network designed for the space debris classification task, setting a new standard for accuracy in the field.

### Stakeholders
1.⁠ **⁠Space Agencies:** Interested in monitoring and managing space debris to ensure the safety and longevity of satellite operations.

2.⁠ **⁠Telecommunication Companies:** Rely on satellite networks for communications; effective debris management is crucial to maintain service continuity and safeguard space infrastructure.

3.**Space Projects (NASA, SpaceX):** Engage in a variety of space exploration, satellite deployment, and research missions. Effective debris management is vital to protect their investments and ensure the success and safety of their missions.

4.**Satellite Raw Material Producers:** Supply materials for satellite manufacturing. They are impacted by the demand for more durable and debris-resistant satellite designs, influencing material innovation and production processes.

5.⁠ **⁠Government:** Invests in space infrastructure and seeks to minimize financial losses due to debris-related damages.

Our work aims to provide these stakeholders with more precise, reliable, and efficient tools for identifying, classifying, and managing space objects, thereby enhancing the overall safety and sustainability of space operations.


### **Data**

**SPARK2022 Dataset**

The SPARK2022 dataset is an invaluable asset for the field of spacecraft detection and trajectory estimation, hosted by the University of Luxembourg's CVI² at SnT. It provides:

- **URL:** [SPARK2022 Dataset](https://cvi2.uni.lu/spark-2022-dataset)
- **Content:** Roughly 110,000 high-resolution RGB images.
- **Classes:** 11, including 10 types of spacecraft and one category for space debris.
- **Features:** Images annotated with object bounding boxes and class labels.
- **Conditions:** Simulated under varied space conditions, including extreme scenarios and variable backgrounds, to ensure realism and applicability.

**Data Integrity:** The dataset's unique blend of synthetic and real data, gathered with state-of-the-art simulation technologies and real-world experiments from the Zero-G Lab, ensures high fidelity and applicability to space environments. It has undergone extensive quality assurance processes, including checks for accuracy and consistency.

**Reliability:** Developed in collaboration with leading space agencies, the dataset's authenticity and quality are guaranteed, making it a reliable foundation for machine learning models.

**Usability:** Accompanied by detailed metadata that facilitates a wide range of research applications, from object detection to complex scenario analysis.

The SPARK2022 dataset represents a cornerstone in pushing the envelope of what's achievable in space situational awareness and recognition, offering an unparalleled resource for researchers aiming to develop cutting-edge, vision-based algorithms.




### **Methods**

Our preprocessing involves resizing images for uniformity, augmenting data to introduce variety, converting all image files to a uniform format and applying noise reduction techniques for clarity. 

A key step is using Mask-RCNN for object detection and image segmentation, enabling precise localization and outlining of satellites and debris, essential for analyzing their distinct features.

The preprocessed data is passed to self-built Convolutional Neural Network to classify space debris from functioning satellites. Our evaluation metrics will focus on precision, recall, F1 scores to ensure our model's predictions are not only accurate but also reliable.

### **Project Plan**

| Period                                     | Milestone                                  |
|--------------------------------------------|--------------------------------------------|
| 27th February 2024 (Checkpoint 1)          | Proposal                                   |
| 25th March 2024 (Checkpoint 2)             | All preprocessing steps including Mask RCNN|
| 22nd April 2024 (Checkpoint 3)             | Final modelling with CNN                   |
| 1st May 2024                               | Final Report Submission.                   |



### **Risks**

**Misclassification of Miniature Satellites**

- **Risk:** Small satellites might be wrongly identified as debris due to their size, for example, a CubeSat is a square-shaped miniature satellite (10 cm × 10 cm × 10 cm).

- **Mitigation:** Enhance the dataset with varied images of miniature satellites and utilize expert input to improve differentiation.

**RCNN Detection Failures**

- **Risk:** If RCNN fails to detect objects, it could impair the CNN's subsequent analysis.

- **Mitigation:** Implement a multi-algorithm strategy for object detection to provide a backup if RCNN underperforms, ensuring continuous analysis flow.

**Augmented Data Misclassification**

- **Risk:** Augmented data might lead to unrealistic images, causing incorrect classifications.

- **Mitigation:** Set clear boundaries for data augmentation to maintain image integrity and periodically review model performance on augmented versus original data to ensure realism.


