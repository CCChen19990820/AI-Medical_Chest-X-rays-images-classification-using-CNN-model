# AI-Medical_Chest-X-rays-images-classification-using-CNN-model

## Project content
This is a competition on kaggle. Use the NIH Chest X-ray Dataset, which is a public dataset, to train the model for Pathological classification.  

## Project flow
Data Preprocessing  
資料前處理使用keras內的ImageDataGenerator套件，對影像做處理，包括影像的縮放、旋轉、投射、位移、翻轉等，使訓練的資料更加多樣，能學習更多不同特徵。  
![image](https://user-images.githubusercontent.com/48405514/185313368-4559f3e6-fce9-47bb-84fb-a91e8673350d.png)  

Build model  
建立CNN模型、將training data丟進去做訓練、再使用testing做預測。  

Model result  
CNN model跑出的最後accuracy如上圖所示，平均accuracy約落在0.55左右，最高有到0.72(Edema)，最低則是0.47(Pneumothorax)，顯示CNN model應用在分類胸腔X光影像上的效果不是很理想，原因應為CNN model的down sampling層數太少，導致效果不佳，若使用VGG16、ResNet50應可有效提高accuracy。訓練好的model存在model.h5的檔案中。Code存在Chest X-rays images classification using CNN model.ipynb。  
![image](https://user-images.githubusercontent.com/48405514/185314056-6784e504-5a6c-4c64-83ea-814eef8becd7.png)
