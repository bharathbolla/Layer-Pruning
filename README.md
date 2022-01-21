# Layer Fine Tuning of Deep Networks

## Paper presented at CICT 2021 [CICT2021_Layer_Fine_Tuning.pdf](https://github.com/sabeesh90/Layer_Fine_Tuning/files/7781439/CICT2021_Layer_Fine_Tuning.pdf)
[CICT-2021_Presentation.pptx](https://github.com/sabeesh90/Layer_Fine_Tuning/files/7914969/CICT-2021_Presentation.pptx)

### Authors -Sabeesh Ethiraj , Bharath Kumar Bolla
<img src="https://user-images.githubusercontent.com/48343095/147504253-463ff874-0737-4771-be02-40d1bfd0f100.png"  width="600"  style = "float:right" height = "650"/>

inspired by our work on multimodal architectures, we further extended our work on the layer fine tuning of deep networks and thier effect on the accuracy of the model. Layer fine tuning involves sequentially making the top layers of a network trainable in increasing ratios until an appropriately high validation accuracy is achieved. Different Deep networks behave differently to this "sequential fine tuning". We have conducted experiments on popular transfer learning architectures trained on ImageNet. A representation of the fine tuning is shown below.  

<img src="https://user-images.githubusercontent.com/48343095/147483623-c17ed2eb-b626-4728-89f1-23906c2914a0.png"  width="500"  style = "float:right" height = "250"/>

<h2> Methodology </h2>
Tuning can be done for all the layers or selective layers as done in our research.

<img src="https://user-images.githubusercontent.com/48343095/147483966-d15c36b8-16f8-4f2b-ab7f-395da3ce8c65.png"  width="500"  style = "float:right" height = "250"/>

The following image shows the methdoology implemented in our paper.

<img src="https://user-images.githubusercontent.com/48343095/147484300-f76ecd29-2b38-4276-8aa7-d7f5edb6fcdf.png"  width="500"  style = "float:right" height = "250"/>
<img src="https://user-images.githubusercontent.com/48343095/147484302-6a460fcd-280d-4d91-bd31-49d4b99824e8.png"  width="600"  style = "float:right" height = "750"/>

The data set used here is the SDSS-4 DR-16 release dataset. 82 experiments as shown below are conducted.

<img src="https://user-images.githubusercontent.com/48343095/147485293-d4890f30-1a18-4d09-918d-3c9e876d11b8.png"  width="1100"  style = "float:right" height = "400"/>

The models are evaluated based on the following evaluation metrics

1) Accuracy – TP+ TN / TP+FP+TN+FN
2) Layer tuning ratio – Number of layers tuned / Total number of layers
3) Parameter tuning Ratio – number of parameters tuned / Total number of parameters

LOSS FUNCTION <br>
Categorical Cross Entropy 𝐶𝐸 = −∑𝑖->𝐶 [𝑡𝑖 𝑙𝑜𝑔(𝑠(𝑖))]

<h2> Results </h2>
Resnet50, MobileNetV2, NasnetMobile   - Dipping Accuracies
 
<img src="https://user-images.githubusercontent.com/48343095/147486264-93c6085e-c9ce-48b4-a2c0-3f88eb067bf7.png"  width="600"  style = "float:right" height = "250"/>
<img src="https://user-images.githubusercontent.com/48343095/147486277-84db4aec-a7b7-4bf7-9b7f-1037bb11d969.png"  width="600"  style = "float:right" height = "250"/>
<img src="https://user-images.githubusercontent.com/48343095/147486286-7019c092-4510-41bf-b0d0-b9e96c3705f2.png"  width="600"  style = "float:right" height = "250"/>

VGG16 - Flattening of Accuracies after initial rise

<img src="https://user-images.githubusercontent.com/48343095/147486837-4d97c910-168f-43b4-9e1e-9d80c4e8a93d.png"  width="600"  style = "float:right" height = "250"/>

DensetNet121, EfficientNetB2, Xception - Consistency of Accuracies

<img src="https://user-images.githubusercontent.com/48343095/147486944-194321c8-ca22-4811-a608-b32c63121fcf.png"  width="600"  style = "float:right" height = "250"/>
<img src="https://user-images.githubusercontent.com/48343095/147487046-49c16217-22d3-48dd-93d8-beea0dd09d43.png"  width="600"  style = "float:right" height = "250"/>
<img src="https://user-images.githubusercontent.com/48343095/147487057-7f3633a2-96c2-4f3b-ac5c-da83df1f94a3.png"  width="600"  style = "float:right" height = "250"/>

<h2> Summary of Architectures</h2>
It is seen that Pre trained models perform better at a specific number of trainable layers, we call this the 'narrow performance index' which determines the ideal number of traiinable layers for a given dataset outside of which may result in decreased performance / increased training time. 

<img src="https://user-images.githubusercontent.com/48343095/147488194-3fa14fb4-328e-4a84-a562-20a6396334bf.png"  width="600"  style = "float:right" height = "250"/>

Baseline Models 
  - Xception/EfficientNetB2 > 
  - MobileNetV2/NasNetMobile >
  - DenseNet121 > Resnet50/VGG16 
<img src="https://user-images.githubusercontent.com/48343095/147488571-11b9f1e2-7b34-4bce-9831-b33b3efa7355.png"  width="500"  style = "float:right" height = "125"/>
<img src="https://user-images.githubusercontent.com/48343095/147488587-3a787444-6e2f-4c25-9378-ab62484dd492.png"  width="600"  style = "float:right" height = "300"/>

Older & Mobile Architectures 
  - Overfitting of Training Curves Mnet > NasNet
  - Lower Accuracies except VGG16
 
Newer Architectures
  - Consistency of Accuracies
  - Immune to Change of Weights

DenseNet121
  - Highest Accuracy  - Efficient to Layer Fine Tuning
  - Least Layer Tuning Ratio & Parameter Tuning Ratio














