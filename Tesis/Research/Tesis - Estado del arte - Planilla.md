2024-10-26
---
# Tesis - Estado del arte - Planilla

### Title: A patch-based convolutional neural network for remote sensing image classification
- Link: https://www.sciencedirect.com/science/article/abs/pii/S0893608017301806
- Authors: Atharva Sharma, Xiuwen Liu, Xiaojun Yang, Di Shi
- Year: 2017
- Abstract: Availability of accurate land cover information over large areas is essential to the global environment sustainability; digital classification using medium-resolution remote sensing data would provide an effective method to generate the required land cover information. However, low accuracy of existing per-pixel based classification methods for medium-resolution data is a fundamental limiting factor. While convolutional neural networks (CNNs) with deep layers have achieved unprecedented improvements in object recognition applications that rely on fine image structures, they cannot be applied directly to medium-resolution data due to lack of such fine structures. In this paper, considering the spatial relation of a pixel to its neighborhood, we propose a new deep patch-based CNN system tailored for medium-resolution remote sensing data. The system is designed by incorporating distinctive characteristics of medium-resolution data; in particular, the system computes patch-based samples from multidimensional top of atmosphere reflectance data. With a test site from the Florida Everglades area (with a size of 771 square kilometers), the proposed new system has outperformed pixel-based neural network, pixel-based CNN and patch-based neural network by 24.36%, 24.23% and 11.52%, respectively, in overall classification accuracy. By combining the proposed deep CNN and the huge collection of medium-resolution remote sensing data, we believe that much more accurate land cover datasets can be produced over large areas.
- Keywords: 
- Conclusions: 

### Title: Multisource Remote Sensing Data Classification Based on Convolutional Neural Network
- Link: https://ieeexplore.ieee.org/abstract/document/8068943
- Authors: Xiaodong Xu; Wei Li; Qiong Ran; Qian Du; Lianru Gao; Bing Zhang
- Year: 2017
- Abstract: As a list of remotely sensed data sources is available, how to efficiently exploit useful information from multisource data for better Earth observation becomes an interesting but challenging problem. In this paper, the classification fusion of hyperspectral imagery (HSI) and data from other multiple sensors, such as light detection and ranging (LiDAR) data, is investigated with the state-of-the-art deep learning, named the two-branch convolution neural network (CNN). More specific, a two-tunnel CNN framework is first developed to extract spectral-spatial features from HSI; besides, the CNN with cascade block is designed for feature extraction from LiDAR or high-resolution visual image. In the feature fusion stage, the spatial and spectral features of HSI are first integrated in a dual-tunnel branch, and then combined with other data features extracted from a cascade network. Experimental results based on several multisource data demonstrate the proposed two-branch CNN that can achieve more excellent classification performance than some existing methods.
- Keywords: Convolutional neural network (CNN), data fusion, deep learning, feature extraction, hyperspectral imagery (HSI)
- Conclusions: 

### Title: Convolutional Neural Networks for Large-Scale Remote-Sensing Image Classification
- Link: https://ieeexplore.ieee.org/abstract/document/7592858
- Authors: Emmanuel Maggiori; Yuliya Tarabalka; Guillaume Charpiat; Pierre Alliez
- Year: 2016
- Abstract: We propose an end-to-end framework for the dense, pixelwise classification of satellite imagery with convolutional neural networks (CNNs). In our framework, CNNs are directly trained to produce classification maps out of the input images. We first devise a fully convolutional architecture and demonstrate its relevance to the dense classification problem. We then address the issue of imperfect training data through a two-step training approach: CNNs are first initialized by using a large amount of possibly inaccurate reference data, and then refined on a small amount of accurately labeled data. To complete our framework, we design a multiscale neuron module that alleviates the common tradeoff between recognition and precise localization. A series of experiments show that our networks consider a large amount of context to provide fine-grained classification maps.
- Keywords: Classification , convolutional neural networks (CNNs) , deep learning , satellite images
- Conclusions: 

### Title: Land Use Classification in Remote Sensing Images by Convolutional Neural Networks
- Link: https://arxiv.org/abs/1508.00092
- Authors: Marco Castelluccio, Giovanni Poggi, Carlo Sansone, Luisa Verdoliva
- Year: 2015
- Abstract: We explore the use of convolutional neural networks for the semantic classification of remote sensing scenes. Two recently proposed architectures, CaffeNet and GoogLeNet, are adopted, with three different learning modalities. Besides conventional training from scratch, we resort to pre-trained networks that are only fine-tuned on the target data, so as to avoid overfitting problems and reduce design time. Experiments on two remote sensing datasets, with markedly different characteristics, testify on the effectiveness and wide applicability of the proposed solution, which guarantees a significant performance improvement over all state-of-the-art references.
- Keywords: Convolutional neural networks, remote sensing, land use classification
- Conclusions: 

### Title: Convolutional Neural Networks for Multimodal Remote Sensing Data Classification
- Link: https://ieeexplore.ieee.org/abstract/document/9598903
- Authors: Xin Wu; Danfeng Hong; Jocelyn Chanussot
- Year: 2021
- Abstract: In recent years, enormous research has been made to improve the classification performance of single-modal remote sensing (RS) data. However, with the ever-growing availability of RS data acquired from satellite or airborne platforms, simultaneous processing and analysis of multimodal RS data pose a new challenge to researchers in the RS community. To this end, we propose a deep-learning-based new framework for multimodal RS data classification, where convolutional neural networks (CNNs) are taken as a backbone with an advanced cross-channel reconstruction module, called CCR-Net. As the name suggests, CCR-Net learns more compact fusion representations of different RS data sources by the means of the reconstruction strategy across modalities that can mutually exchange information in a more effective way. Extensive experiments conducted on two multimodal RS datasets, including hyperspectral (HS) and light detection and ranging (LiDAR) data, i.e., the Houston2013 dataset, and HS and synthetic aperture radar (SAR) data, i.e., the Berlin dataset, demonstrate the effectiveness and superiority of the proposed CCR-Net in comparison with several state-of-the-art multimodal RS data classification methods. The codes will be openly and freely available at https://github.com/danfenghong/IEEE_TGRS_CCR-Net for the sake of reproducibility.
- Keywords:     Classification , convolutional neural networks (CNNs) , cross-channel , hyperspectral (HS) , light detection and ranging (LiDAR) , multimodal , reconstruction , remote sensing (RS) , synthetic aperture radar (SAR)
- Conclusions: 

### Title: Deep Convolutional Neural Network for Complex Wetland Classification Using Optical Remote Sensing Imagery
- Link: https://ieeexplore.ieee.org/abstract/document/8401505
- Authors: Mohammad Rezaee; Masoud Mahdianpari; Yun Zhang; Bahram Salehi
- Year: 2018
- Abstract: The synergistic use of spatial features with spectral properties of satellite images enhances thematic land cover information, which is of great significance for complex land cover mapping. Incorporating spatial features within the classification scheme have been mainly carried out by applying just low-level features, which have shown improvement in the classification result. By contrast, the application of high-level spatial features for classification of satellite imagery has been underrepresented. This study aims to address the lack of high-level features by proposing a classification framework based on convolutional neural network (CNN) to learn deep spatial features for wetland mapping using optical remote sensing data. Designing a fully trained new convolutional network is infeasible due to the limited amount of training data in most remote sensing studies. Thus, we applied fine tuning of a pre-existing CNN. Specifically, AlexNet was used for this purpose. The classification results obtained by the deep CNN were compared with those based on well-known ensemble classifiers, namely random forest (RF), to evaluate the efficiency of CNN. Experimental results demonstrated that CNN was superior to RF for complex wetland mapping even by incorporating the small number of input features (i.e., three features) for CNN compared to RF (i.e., eight features). The proposed classification scheme is the first attempt, investigating the potential of fine-tuning pre-existing CNN, for land cover mapping. It also serves as a baseline framework to facilitate further scientific research using the latest state-of-art machine learning tools for processing remote sensing data.
- Keywords:     AlexNet , convolutional neural network (CNN) , deep learning , random forest (RF) , spatial feature , wetland mapping
- Conclusions: 

### Title: Towards better exploiting convolutional neural networks for remote sensing scene classification
- Link: https://www.sciencedirect.com/science/article/abs/pii/S0031320316301509
- Authors: Keiller Nogueira, Otávio A.B. Penatti, Jefersson A. dos Santos
- Year: 2017
- Abstract: We present an analysis of three possible strategies for exploiting the power of existing convolutional neural networks (ConvNets or CNNs) in different scenarios from the ones they were trained: full training, fine tuning, and using ConvNets as feature extractors. In many applications, especially including remote sensing, it is not feasible to fully design and train a new ConvNet, as this usually requires a considerable amount of labeled data and demands high computational costs. Therefore, it is important to understand how to better use existing ConvNets. We perform experiments with six popular ConvNets using three remote sensing datasets. We also compare ConvNets in each strategy with existing descriptors and with state-of-the-art baselines. Results point that fine tuning tends to be the best performing strategy. In fact, using the features from the fine-tuned ConvNet with linear SVM obtains the best results. We also achieved state-of-the-art results for the three datasets used.
- Keywords: 
- Conclusions: 

### Title: SatCNN: satellite image dataset classification using agile convolutional neural networks 
- Link: https://www.tandfonline.com/doi/abs/10.1080/2150704X.2016.1235299
- Authors: Yanfei Zhong, Feng Fei, Yanfei Liu, Bei Zhao, Hongzan Jiao, Liangpei Zhang
- Year: 2016
- Abstract: With the launch of various remote-sensing satellites, more and more high-spatial resolution remote-sensing (HSR-RS) images are becoming available. Scene classification of such a huge volume of HSR-RS images is a big challenge for the efficiency of the feature learning and model training. The deep convolutional neural network (CNN), a typical deep learning model, is an efficient end-to-end deep hierarchical feature learning model that can capture the intrinsic features of input HSR-RS images. However, most published CNN architectures are borrowed from natural scene classification with thousands of training samples, and they are not designed for HSR-RS images. In this paper, we propose an agile CNN architecture, named as SatCNN, for HSR-RS image scene classification. Based on recent improvements to modern CNN architectures, we use more efficient convolutional layers with smaller kernels to build an effective CNN architecture. Experiments on SAT data sets confirmed that SatCNN can quickly and effectively learn robust features to handle the intra-class diversity even with small convolutional kernels, and the deeper convolutional layers allow spontaneous modelling of the relative spatial relationships. With the help of fast graphics processing unit acceleration, SatCNN can be trained within about 40 min, achieving overall accuracies of 99.65% and 99.54%, which is the state-of-the-art for SAT data sets.
- Keywords: 
- Conclusions: 

### Title: Classification and Segmentation of Satellite Orthoimagery Using Convolutional Neural Networks
- Link: https://www.mdpi.com/2072-4292/8/4/329
- Authors:  Martin Längkvist, Andrey Kiselev, Marjan Alirezaie, Amy Loutfi
- Year: 2016
- Abstract: The availability of high-resolution remote sensing (HRRS) data has opened up the possibility for new interesting applications, such as per-pixel classification of individual objects in greater detail. This paper shows how a convolutional neural network (CNN) can be applied to multispectral orthoimagery and a digital surface model (DSM) of a small city for a full, fast and accurate per-pixel classification. The predicted low-level pixel classes are then used to improve the high-level segmentation. Various design choices of the CNN architecture are evaluated and analyzed. The investigated land area is fully manually labeled into five categories (vegetation, ground, roads, buildings and water), and the classification accuracy is compared to other per-pixel classification works on other land areas that have a similar choice of categories. The results of the full classification and segmentation on selected segments of the map show that CNNs are a viable tool for solving both the segmentation and object recognition task for remote sensing data.
- Keywords: remote sensing; orthoimagery; convolutional neural network; per-pixel classification; segmentation; region merging
- Conclusions: 

### Title: Multi-Classification of Satellite Imagery Using Fully Convolutional Neural Network
- Link: https://ieeexplore.ieee.org/abstract/document/9111928
- Authors: Nyan Linn Tun; Alexander Gavrilov; Naing Min Tun
- Year: 2020
- Abstract: The article considers deep learning techniques, namely, the use of a deep neural network or convolutional neural network (CNN), which increases the efficiency of the application of remote sensing data for multi-classification due to feature learning. In this paper, we have established a classification model using deep convolutional neural networks that can reliably identify the corresponded objects. The explanation of the traditional convolutional neural network and the training process of the proposed convolutional neural network model are presented. The evaluation performances of the proposed model are conducted on the UC Merced Land Use dataset. The proposed model performs high classification accuracy in smallest times without high computation performance.
- Keywords: Remote sensing specific data, multi-classification, fully convolutional neural network
- Conclusions: 

### Title: DeepSat V2: feature augmented convolutional neural nets for satellite image classification
- Link: https://www.tandfonline.com/doi/abs/10.1080/2150704X.2019.1693071
- Authors: Qun Liu, Saikat Basu, Sangram Ganguly, Supratik Mukhopadhyay, Robert DiBiano, Manohar Karki, Ramakrishna Nemani
- Year: 2019
- Abstract: Satellite image classification is a challenging problem that lies at the crossroads of remote sensing, computer vision, and machine learning. Due to the high variability inherent in satellite data, most of the current object classification approaches are not suitable for handling satellite datasets. The progress of satellite image analytics has also been inhibited by the lack of a single labeled high-resolution dataset with multiple class labels. In a preliminary version of this work, we introduced two new high resolution satellite imagery datasets (SAT-4 and SAT-6) and proposed DeepSat framework for classification based on “handcrafted” features and a deep belief network (DBN). The present paper is an extended version, we present an end-to-end framework leveraging an improved architecture that augments a convolutional neural network (CNN) with handcrafted features (instead of using DBN-based architecture) for classification. Our framework, having access to fused spatial information obtained from handcrafted features as well as CNN feature maps, have achieved accuracies of 99.90\% and 99.84\% respectively, on SAT-4 and SAT-6, surpassing all the other state-of-the-art results. A statistical analysis based on Distribution Separability Criterion substantiates the robustness of our approach in learning better representations for satellite imagery.
- Keywords: 
- Conclusions: 

### Title: Fully convolutional neural networks for remote sensing image classification
- Link: https://ieeexplore.ieee.org/abstract/document/7730322
- Authors: Emmanuel Maggiori; Yuliya Tarabalka; Guillaume Charpiat; Pierre Alliez
- Year: 2016
- Abstract: We propose a convolutional neural network (CNN) model for remote sensing image classification. Using CNNs provides us with a means of learning contextual features for large-scale image labeling. Our network consists of four stacked convolutional layers that downsample the image and extract relevant features. On top of these, a deconvolutional layer upsamples the data back to the initial resolution, producing a final dense image labeling. Contrary to previous frameworks, our network contains only convolution and deconvolution operations. Experiments on aerial images show that our network produces more accurate classifications in lower computational time.
- Keywords: Remote sensing images, classification, deep learning, convolutional neural networks
- Conclusions: 

### Title: Satellite Image Classification with Deep Learning
- Link: https://ieeexplore.ieee.org/abstract/document/8457969
- Authors: Mark Pritt; Gary Chern
- Year: 2018
- Abstract: Satellite imagery is important for many applications including disaster response, law enforcement, and environmental monitoring. These applications require the manual identification of objects and facilities in the imagery. Because the geographic expanses to be covered are great and the analysts available to conduct the searches are few, automation is required. Yet traditional object detection and classification algorithms are too inaccurate and unreliable to solve the problem. Deep learning is a family of machine learning algorithms that have shown promise for the automation of such tasks. It has achieved success in image understanding by means of convolutional neural networks. In this paper we apply them to the problem of object and facility recognition in high-resolution, multi-spectral satellite imagery. We describe a deep learning system for classifying objects and facilities from the IARPA Functional Map of the World (fMoW) dataset into 63 different classes. The system consists of an ensemble of convolutional neural networks and additional neural networks that integrate satellite metadata with image features. It is implemented in Python using the Keras and TensorFlow deep learning libraries and runs on a Linux server with an NVIDIA Titan X graphics card. At the time of writing the system is in 2nd place in the fMoW TopCoder competition. Its total accuracy is 83%, the $F_1$ score is 0.797, and it classifies 15 of the classes with accuracies of 95% or better.
- Keywords: artificial intelligence, AI, deep learning, machine learning, image understanding, recognition, classification, satellite imagery
- Conclusions: 

### Title: Performance Enhancement of Satellite Image Classification Using a Convolutional Neural Network
- Link: https://link.springer.com/chapter/10.1007/978-3-319-64861-3_63
- Authors: Noureldin Laban, Bassam Abdellatif, Hala M. Ebied, Howida A. Shedeed, Mohamed F. Tolba
- Year: 2017
- Abstract: With dramatically increasing of very resolution of satellite imaging sensors and the daily increasing of remote sensing databases, image classification has been gaining prominence in remote sensing applications. Convolutional neural networks (CNNs) techniques have already been outperforming other classification approaches in various domains. In this paper, we propose an enhance classification of satellite image using CNNs. high information content of satellite images alongside high computational calculations needed by CNNs, that make performance issues very crucial. The enhancement process is based on an efficient selection of adequate image scales that perform respectively, high classification accuracy with least computational burdens. We evaluate the proposed method on three state-of-the-art datasets: UC Merced Land Use Dataset, WHU-RS Dataset and Brazilian Coffee Scenes Dataset. The proposed method leads to a performance enhancement, as opposed to using original scales directly.
- Keywords: 
- Conclusions: 

### Title: Satellite Imagery Feature Detection using Deep Convolutional Neural Network: A Kaggle Competition
- Link: https://arxiv.org/abs/1706.06169
- Authors: Vladimir Iglovikov, Sergey Mushinskiy, Vladimir Osin
- Year: 2017
- Abstract: This paper describes our approach to the DSTL Satellite Imagery Feature Detection challenge run by Kaggle. The primary goal of this challenge is accurate semantic segmentation of different classes in satellite imagery. Our approach is based on an adaptation of fully convolutional neural network for multispectral data processing. In addition, we defined several modifications to the training objective and overall training pipeline, e.g. boundary effect estimation, also we discuss usage of data augmentation strategies and reflectance indices. Our solution scored third place out of 419 entries. Its accuracy is comparable to the first two places, but unlike those solutions, it doesn't rely on complex ensembling techniques and thus can be easily scaled for deployment in production as a part of automatic feature labeling systems for satellite imagery analysis.
- Keywords: 
- Conclusions: 

### Title: Convolutional Neural Network Based Automatic Object Detection on Aerial Images
- Link: https://ieeexplore.ieee.org/abstract/document/7447728
- Authors: Igor Ševo; Aleksej Avramović
- Year: 2016
- Abstract: We are witnessing daily acquisition of large amounts of aerial and satellite imagery. Analysis of such large quantities of data can be helpful for many practical applications. In this letter, we present an automatic content-based analysis of aerial imagery in order to detect and mark arbitrary objects or regions in high-resolution images. For that purpose, we proposed a method for automatic object detection based on a convolutional neural network. A novel two-stage approach for network training is implemented and verified in the tasks of aerial image classification and object detection. First, we tested the proposed training approach using UCMerced data set of aerial images and achieved accuracy of approximately 98.6%. Second, the method for automatic object detection was implemented and verified. For implementation on GPGPU, a required processing time for one aerial image of size 5000 × 5000 pixels was around 30 s.
- Keywords: Aerial images, classification, convolutional neural networks (cNNs), object detection
- Conclusions: 

### Title: Orientation robust object detection in aerial images using deep convolutional neural network
- Link: https://ieeexplore.ieee.org/abstract/document/7351502
- Authors: Haigang Zhu; Xiaogang Chen; Weiqun Dai; Kun Fu; Qixiang Ye; Jianbin Jiao
- Year: 2015
- Abstract: Detecting objects in aerial images is challenged by variance of object colors, aspect ratios, cluttered backgrounds, and in particular, undetermined orientations. In this paper, we propose to use Deep Convolutional Neural Network (DCNN) features from combined layers to perform orientation robust aerial object detection. We explore the inherent characteristics of DC-NN as well as relate the extracted features to the principle of disentangling feature learning. An image segmentation based approach is used to localize ROIs of various aspect ratios, and ROIs are further classified into positives or negatives using an SVM classifier trained on DCNN features. With experiments on two datasets collected from Google Earth, we demonstrate that the proposed aerial object detection approach is simple but effective.
- Keywords: Aerial Object Detection, Orientation Robust, Deep Convolutional Neural Network
- Conclusions: 

### Title: Optimization Of Convolutional Neural Network For Object Recognition On Satellite Images
- Link: https://ieeexplore.ieee.org/abstract/document/8457056
- Authors: V. V. Khryashchev; A. A. Ostrovskaya; V. A. Pavlov; A. S. Semenov
- Year: 2018
- Abstract: Investigation about using convolutional neural networks for detection geo-objects on the satellite images from Landsat-8 was presented. U-NET convolutional neural network architecture for implementing the recognition algorithm was used. The neural network was trained by the marked image base “Urban Atlas”. Urban Atlas contains images of 21 classes, but in current research was used 3 classes: “Forest”, “Agriculture” and “Water”. Images obtained from the Landsat-8 satellites are used for estimation of automatic object detection quality. To analyze the accuracy of the object detection algorithm, the selected regions were compared with the areas by previously marked by experts. Two modification of object detector were proposed and analyzing.
- Keywords: image recognition, convolutional neural network, satellite images, object detection, deep learning
- Conclusions: 

### Title: A Deep Convolutional Neural Network for Detecting Volcanic Thermal Anomalies from Satellite Images
- Link: https://www.mdpi.com/2072-4292/15/15/3718
- Authors:  Eleonora Amato, Claudia Corradino, Federica Torrisi, Ciro Del Negro
- Year: 2023
- Abstract: The latest generation of high-spatial-resolution satellites produces measurements of high-temperature volcanic features at global scale, which are valuable to monitor volcanic activity. Recent advances in technology and increased computational resources have resulted in an extraordinary amount of monitoring data, which can no longer be so readily examined. Here, we present an automatic detection algorithm based on a deep convolutional neural network (CNN) that uses infrared satellite data to automatically determine the presence of volcanic thermal activity. We exploit the potentiality of the transfer learning technique to retrain a pre-trained SqueezeNet CNN to a new domain. We fine-tune the weights of the network over a new dataset opportunely created with images related to thermal anomalies of different active volcanoes around the world. Furthermore, an ensemble approach is employed to enhance accuracy and robustness when compared to using individual models. We chose a balanced training dataset with two classes, one containing volcanic thermal anomalies (erupting volcanoes) and the other containing no thermal anomalies (non-erupting volcanoes), to differentiate between volcanic scenes with eruptive and non-eruptive activity. We used satellite images acquired in the infrared bands by ESA Sentinel-2 Multispectral Instrument (MSI) and NASA & USGS Landsat 8 Operational Land Imager and Thermal InfraRed Sensor (OLI/TIRS). This deep learning approach makes the model capable of identifying the appearance of a volcanic thermal anomaly in the images belonging to the volcanic domain with an overall accuracy of 98.3%, recognizing the scene with active flows and erupting vents (i.e., eruptive activity) and the volcanoes at rest. This model is generalizable, and has the capability to analyze every image captured by these satellites over volcanoes around the world.
- Keywords: CNN; detection; infrared; lava flow; transfer learning; ensemble learning; volcanic thermal anomaly
- Conclusions: 

### Title: Identificación y Mapeo de Paleocauces utilizando Imágenes Satelitales de Alta Resolución en la Llanura Costera de la Bahía Samborombón, Este de la Provincia de Buenos Aires, Argentina.
- Link: https://www.researchgate.net/publication/325827963_IDENTIFICACION_Y_MAPEO_DE_PALEOCAUCES_UTILIZANDO_IMAGENES_SATELITALES_DE_ALTA_RESOLUCION_EN_LA_LLANURA_COSTERA_DE_LA_BAHIA_SAMBOROMBON_ESTE_DE_LA_PROVINCIA_DE_BUENOS_AIRES_ARGENTINA
- Authors: Mariel Samanta Luengo, Graciela Salinas de Salmuni, Enrique Fucks, Isabel Vilanova Torre
- Year: 2016
- Abstract: Este trabajo es parte del proyecto "vegetación y ambientes del Holoceno en el sectorcontinental de la Bahía de Samborombón, Provincia de Buenos Aires: cambios del nivel del mar"que se desarrolla en la Facultad de Ciencias Naturales y Museo, de la Universidad NacionalMuseo de La Plata y se enmarca dentro de las actividades nacionales de cooperación de laComisión Nacional de Actividades Espaciales (CONAE). En la llanura costera de la BahíaSamborombón, donde los ríos Samborombón y Salado tienen sus desembocaduras en el ?río dela plata?, sus cauces presentan un diseño individual de tipo meandroso, encontrándose suevolución íntimamente relacionada con las diferentes geoformas del MIS1 (cordones litorales,cheniers, llanuras de mareas) de disposición transversal al escurrimiento. En el área de estudio, seevidencian paleocauces o cauces abandonados, demostrando movimientos laterales omigraciones, sobre la planicie de mareas litoral. Las comunidades vegetales dependen de latopografía y del carácter del sustrato y en consecuencia los cambios en la vegetación estándeterminados por la evolución geomorfológica local y/o regional, íntimamente asociada a loscambios climáticos globales y/o locales. En función de esto, las comunidades vegetales de losdistintos ambientes se modificaron en el tiempo y en el espacio en concordancia con la evolucióndel ambiente y la conformación de nuevos rasgos geomorfológicos. El objetivo de este estudio esel reconocimiento y análisis, mediante la herramienta de sensores remotos de los paleocauces delos ríos Samborombón y Salado, en la zona de su desembocadura, para la posteriorreconstrucción paleoambiental, relacionada con el descenso del nivel del mar durante elHoloceno Tardío. Se procesaron imágenes ópticas SPOT6 debido a su alta resolución espacial.Dado que en las geoformas presentes varía la cobertura vegetal, se aplicaron realces espectralesque resaltaron los cambios en la vegetación y humedad facilitando el mapeo de meandros abandonados, los que fueron controlados por datos de campo y dataciones radiocarbónicas, paraun mayor entendimiento de la evolución paleombiental.
- Keywords: 
- Conclusions: 

