
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
- **DeepGlobe Land Cover Classification Dataset**
  - [Dataset Link](https://www.kaggle.com/datasets/balraj98/deepglobe-land-cover-classification-dataset)
    ```
    @InProceedings{DeepGlobe18,
     author = {Demir, Ilke and Koperski, Krzysztof and Lindenbaum, David and Pang, Guan and Huang, Jing and Basu,
     Saikat and Hughes, Forest and Tuia, Devis and Raskar, Ramesh},
     title = {DeepGlobe 2018: A Challenge to Parse the Earth Through Satellite Images},
     booktitle = {The IEEE Conference on Computer Vision and Pattern Recognition (CVPR) Workshops},
     month = {June},
     year = {2018}
    }
    ```

- **Toronto City Large-Scale 3D Indoor Spaces Dataset**
  - [Dataset Link](https://www.cs.toronto.edu/~vmnih/data/)
    ```
    @phdthesis{MnihThesis,
     author = {Volodymyr Mnih},
     title = {Machine Learning for Aerial Image Labeling},
     school = {University of Toronto},
     year = {2013}
    }
    ```

- **Helicopter Landing Dataset**
  - [Dataset Link](https://universe.roboflow.com/govind-a-qfk4g/helicopter-landing)
    ```
     @misc{ helicopter-landing_dataset,
      title = { Helicopter Landing Dataset },
      type = { Open Source Dataset },
      author = { Govind A },
      howpublished = { \url{ https://universe.roboflow.com/govind-a-qfk4g/helicopter-landing } },
      url = { https://universe.roboflow.com/govind-a-qfk4g/helicopter-landing },
      journal = { Roboflow Universe },
      publisher = { Roboflow },
      year = { 2023 },
      month = { dec },
      note = { visited on 2024-01-23 },
    }
  ```
## Models & Methodology
### Helicopter Landing Zone Detection using YOLO V8

The approach involves estimating aerial depth maps using YOLO on RGB images, leveraging datasets like KITTI. The system focuses on the farthest depth data, utilizing a classifier with Inception modules for potential landing zone classification. YOLO is trained on synthetic aerial images generated from urban scenarios.

### Road Mapping on Unfamiliar Terrains using U-Net

The proposed methodology utilizes a U-Net model trained on SAR patches and OSM road data masks. The DeepGlobe Road Extraction Dataset and the Massachusetts Roads Dataset were utilized for training the model. Soft Dice loss and Jaccard index are employed to address class imbalance. The model, demonstrated in challenging desert landscapes, showcases robustness and scalability using free Sentinel-1 data for cost-effective global road mapping.


## Results
### Landing Sites Identified
<img width="450" alt="Screenshot 2024-01-15 011939" src="https://github.com/GOVINDFROMINDIA/Space-Paper/assets/79012314/fa1774d4-a661-48da-8a00-8402014fba4f">

### Landing Sites Identified Road Segments Extracted
<img width="490" alt="Screenshot 2024-01-15 164150" src="https://github.com/GOVINDFROMINDIA/Space-Paper/assets/79012314/c30576ac-14af-4ced-860c-bc74964fe4db">

## Conclusion
The paper proposes a revolutionary method to emergency response in disaster-stricken areas by amalgamating the combined power of YOLOv8 for landing site identification and U-Net for road segmentation. The system offers a comprehensive solution for navigating treacherous landscapes and facilitating swift rescue operations. The fine-tuned U-Net model demonstrated an accuracy about 94.28% and the YOLOv8 model gave an accuracy of about 90% .The U-Net model, for more accuracy in a specific area of interest could be fine-tuned with the area-specific datasets with specific geographic targets like desserts, plateaus, suburbs etc. Likewise we can improve the proposed system to a specific region the user requires for better results. Overall, with the promising results in terms of accuracy and efficiency, this system has the potential to save countless lives by streamlining emergency response efforts and minimizing response times by enabling a robust clarification of any unfamiliar terrain

## Reference
[1] Kobusingye, Olive C., et al. ”Emergency medical services.” Disease Control Priorities in Developing Countries. 2nd edition (2006).
[2] Alstrup, Karen, et al. ”Association of helicopter vs
ground emergency medical transportation with 1-year
mortality in Denmark.” JAMA network open 4.1
(2021): e2033318-e2033318.
[3] Serrano, Kanny Krizzy D., and Argel A. Bandala.
”YOLO-Based Terrain Classification for UAV Safe
Landing Zone Detection.” 2023 IEEE Region 10 Symposium (TENSYMP). IEEE, 2023.
[4] Chang, Chew Wai, et al. ”Land cover classification of
very high spatial resolution satellite imagery.” 2013
IEEE International Geoscience and Remote Sensing
Symposium-IGARSS. IEEE, 2013.
[5] Zhang, Zhengxin, Qingjie Liu, and Yunhong Wang.
”Road extraction by deep residual u-net.” IEEE Geoscience and Remote Sensing Letters 15.5 (2018): 749-
753.
[6] Sun, Tao, et al. ”Stacked u-nets with multi-output for
road extraction.” Proceedings of the IEEE Conference
on Computer Vision and Pattern Recognition Workshops. 2018.
[7] R. Wang, M. Cai, Z. Xia and Z. Zhou, ”Remote
Sensing Image Road Segmentation Method Integrating CNN-Transformer and UNet,” in IEEE Access,
vol. 11, pp. 144446-144455, 2023, doi: 10.1109/ACCESS.2023.3344797.
[8] B. K. Biji and S. S, ”A Model for Relief Transportation
Network in Disaster Management,” 2022 Second International Conference on Next Generation Intelligent
Systems (ICNGIS), Kottayam, India, 2022, pp. 1-5,
doi: 10.1109/ICNGIS54955.2022.10079783.
[9] Killada, Narendra V., Shrinivas Badiger, and Bejoy K.
Thomas. ”Flood in Krishna Basin.” Agony of floods:
Flood induced water conflicts in India (2012): 101.
[10] Lindell, Michael K., Sudha Arlikatti, and Shih-Kai
Huang. ”Immediate behavioral response to the June 17,
2013 flash floods in Uttarakhand, North India.” International journal of disaster risk reduction 34 (2019):
129-146.
[11] Ruiz-Ponce, Pablo, et al. ”Poseidon: A data augmentation tool for small object detection datasets in maritime
environments.” Sensors 23.7 (2023): 3691.
[12] Demir, Ilke, et al. ”Deepglobe 2018: A challenge to
parse the earth through satellite images.” Proceedings
of the IEEE Conference on Computer Vision and
Pattern Recognition Workshops. 2018.
[13] Mnih, Volodymyr. Machine learning for aerial image
labeling. University of Toronto (Canada), 2013.
[14] Yeung, Henry Wing Fung, et al. ”Deep-learning-based
solution for data deficient satellite image segmentation.” Expert Systems with Applications 191 (2022):
116210.
[15] Suprapto, Bhakti Yudho, et al. ”The Detection System
of Helipad for Unmanned Aerial Vehicle Landing Using YOLO Algorithm.” Jurnal Ilmiah Teknik Elektro
Komputer dan Informatika 7.2 (2021): 193-206.
[16] Abdollahi, Abolfazl, et al. ”Deep learning approaches
applied to remote sensing datasets for road extraction:
A state-of-the-art review.” Remote Sensing 12.9 (2020):
1444.
[17] Alsabhan, Waleed, and Turky Alotaiby. ”Automatic
building extraction on satellite images using Unet
and ResNet50.” Computational Intelligence and Neuroscience 2022 (2022).
[18] Adegun, Adekanmi Adeyinka, et al. ”State-of-the-Art
Deep Learning Methods for Objects Detection in Remote Sensing Satellite Images.” Sensors 23.13 (2023):
5849.
[19] Han, Tong, et al. ”Improving the Detection and Positioning of Camouflaged Objects in YOLOv8.” Electronics 12.20 (2023): 4213.
[20] Sultonov, Furkat, et al. ”Mixer U-Net: An improved
automatic road extraction from UAV imagery.” Applied
Sciences 12.4 (2022): 1953.
[21] N. Y. Q. Abderrahim, S. Abderrahim and A. Rida,
”Road Segmentation using U-Net architecture,” 2020
IEEE International conference of Moroccan Geomatics
(Morgeo), Casablanca, Morocco, 2020, pp. 1-4, doi:
10.1109/Morgeo49228.2020.9121887
[22] Antony, Dhanyamol, and Subu Surendran. ”Satellite
image registration and image stitching.” International
Journal of Computer Science Engineering Technology
4.2 (2013): 62-66.


