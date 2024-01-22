
# From Chaos to Clarity: Leveraging Satellite Imagery and Deep Learning for Emergency Response in War Torn & Disaster-Stricken Areas
## Abstract

In the aftermath of natural disasters or conflict-ridden areas, urgent decision-making is imperative for effective
emergency medical services (EMS). These situations demand timely interventions, situational assessments, and
efficient transport to health facilities, underscoring the importance of accurate road maps. However, rural or remote
areas often lack proper mapping infrastructure, particularly during calamities that disrupt regular routes. To address
this, our research leverages satellite imagery and deep learning, specifically employing U-Net Architecture and
YOLOv8. The curated dataset, drawn from the Bhoonidhi portal, prioritizes geographic diversity and features like
landing sites and flood-affected regions. Utilizing U-Net for precise road mapping and YOLOv8 for identifying
helicopter landing zones, our approach automates and expedites critical tasks, offering timely information for
emergency response. The synergy between these models enhances the overall efficiency of the system, ensuring
accurate identification of road networks and suitable landing zones. Testing in selected areas of Karnataka, Andhra
Pradesh, and Uttarakhand reveals the system’s adaptability to various road dynamics, addressing challenges in both
natural disasters and conflict scenarios. This paper proposes an innovative model, signifying a transformative leap
in disaster and conflict response, facilitating a seamless transition to clarity and potentially saving countless lives.

**Keywords:** Satellite Imagery, Helicopter Landing Site , U-Net Architecture, YOLOv8, Road Mapping, Image
Segmentation

## Datasets & Sources
-**DeepGlobe Land Cover Classification Dataset**
  - [Dataset Link](https://www.kaggle.com/datasets/balraj98/deepglobe-land-cover-classification-dataset)

- **Toronto City Large-Scale 3D Indoor Spaces Dataset**
  - [Dataset Link](https://www.cs.toronto.edu/~vmnih/data/)

- **Helicopter Landing Dataset**
  - [Dataset Link](https://universe.roboflow.com/govind-a-qfk4g/helicopter-landing)

## Models & Methodology
### Helicopter Landing Zone Detection using YOLO V8

The approach involves estimating aerial depth maps using YOLO on RGB images, leveraging datasets like KITTI. The system focuses on the farthest depth data, utilizing a classifier with Inception modules for potential landing zone classification. YOLO is trained on synthetic aerial images generated from urban scenarios.

### Road Mapping on Unfamiliar Terrains using U-Net

The proposed methodology utilizes a U-Net model trained on SAR patches and OSM road data masks. Soft Dice loss and Jaccard index are employed to address class imbalance. The model, demonstrated in challenging desert landscapes, showcases robustness and scalability using free Sentinel-1 data for cost-effective global road mapping.


## Results
### Landing Sites Identified
<img width="450" alt="Screenshot 2024-01-15 011939" src="https://github.com/GOVINDFROMINDIA/Space-Paper/assets/79012314/fa1774d4-a661-48da-8a00-8402014fba4f">

### Landing Sites Identified Road Segments Extracted
<img width="490" alt="Screenshot 2024-01-15 164150" src="https://github.com/GOVINDFROMINDIA/Space-Paper/assets/79012314/c30576ac-14af-4ced-860c-bc74964fe4db">

## Conclusion
The paper proposes a revolutionary method to emergency response in disaster-stricken areas by amalgamating the combined power of YOLOv8 for landing site identification and U-Net for road segmentation. The system offers a comprehensive solution for navigating treacherous landscapes and facilitating swift rescue operations. The fine-tuned U-Net model demonstrated an accuracy about 94.28% and the YOLOv8 model gave an accuracy of about 90% .The U-Net model, for more accuracy in a specific area of interest could be fine-tuned with the area-specific datasets with specific geographic targets like desserts, plateaus, suburbs etc. Likewise we can improve the proposed system to a specific region the user requires for better results. Overall, with the promising results in terms of accuracy and efficiency, this system has the potential to save countless lives by streamlining emergency response efforts and minimizing response times by enabling a robust clarification of any unfamiliar terrain


