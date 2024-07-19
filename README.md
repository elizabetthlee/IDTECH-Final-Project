# IDTECH-Final-Brain-Tumor-Project

This code recognizes brain tumors from the given data set of MRI images and categorizes them  into 4 different classes (glioma, meningioma, pituitary, and no tumor)

The class numbers correspond to the following tumors:
1. Glioma
2. Meningioma
3. No tumor
4. Pituitary

## THE ALGORITHM
This project uses the code example from the Retraining Image Classification Module shown in the video. 
It uses the trained model to recognize the type of brain tumor in a specific image, then displays the confidence score and the class that it is recognized as. 
Examples:
![glioma_tumor](https://github.com/user-attachments/assets/ee3886a4-d5c6-4601-8800-442b5a378b82)
![meningioma_tumor](https://github.com/user-attachments/assets/c09f19bb-5915-46fb-a4a0-c5725d6afe7f)

-----------------------------------------------------------------------
## RUNNING THE PROJECT
The commands run in the terminal (shown in the video) are similar to the one used in the Retraining Image Classification module example, but some names at the end of the commands are changed to work with my project

After the project is trained, this is the command in order to identify the tumor images. (no_tumor/image.jpg no_tumor.jpg can be changed to correspond with the image file name.)
imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/no_tumor/image.jpg no_tumor.jpg

This is the dataset that I used for my project: https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri
The dataset has parentheses in the image file names, so they should be renamed before running specific images.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

This project could be modified to work with a data set that includes more types of brain tumors. Datasets of MRI scans are pretty limited online due to patient confidentiality. 
Due to a limited amount of time to train the model, it may not be perfectly accurate. However, further modifications will improve the program. 

[View a video example here] (https://drive.google.com/file/d/1CGFAE5nkdRkeKNdmVWrFMZfRiQ9Hxz5i/view?usp=sharing)

