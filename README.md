**CNN Architecture Comparison for Property Price Prediction**  
**Project Overview**

A comprehensive comparative analysis of 12 CNN architectures to identify the optimal feature extraction backbone for property price prediction using Zimbabwe real estate data.

Research Question
Which convolutional neural network architecture provides the most discriminative visual features when combined with tabular property data for accurate price prediction?

_Architectures Compared_  
12 strategically selected CNN models representing key evolutionary milestones:

**Architecture Family	Models**  
**ResNet**	ResNet50, ResNet152
**EfficientNet**	EfficientNetB0, EfficientNetB3
**DenseNet**	DenseNet121, DenseNet201
**Mobile**	MobileNetV2, NASNetMobile
**Inception**	InceptionV3, InceptionResNetV2
**Classic**	VGG16, Xception  

**Dataset**
1,610 property listings from Zimbabwe market

Structured features: Price, bedrooms, bathrooms, area measurements, location
Visual data: Property photographs (466 actual + 1,144 median-imputed)
Target variable: Property price (USD)

**Methodology**
**Data Preprocessing**  
Two-pass median imputation for missing images
Feature engineering: Area ratios, price per sqm, boolean flags
Text processing: Property type extraction from titles
Complete data preservation strategy

**Multi-Modal Fusion**  
Tabular features: 12 engineered attributes
Visual features: CNN embeddings from each architecture
Neural network with dual input streams
Early stopping and consistent train/val/test splits

**Results**
**Performance Ranking**  
Rank	Model	Test MAE	R²	Features
1	DenseNet201	$631,166.94	-0.064	1,932
2	ResNet50	$631,169.31	-0.064	2,060
3	InceptionV3	$631,187.06	-0.064	2,060
12	InceptionResNetV2	$631,210.00	-0.064	1,548  

**Key Findings**  
Minimal performance variation between architectures ($43 range)
Negative R² scores across all models
DenseNet family performed slightly better on average
Visual features provided limited predictive value beyond tabular data
