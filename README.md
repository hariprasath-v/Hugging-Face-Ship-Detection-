# HuggingFace-Ship-Detection

### Competition hosted on <a href="https://hf.co/spaces/competitions/ship-detection">Huggingface</a>

### Problem
80% of the world’s cargo is transported by ocean. Congested ports can become a massive problem because they disrupt supply chains. Port congestion means that ships arrive at the port and cannot load or unload, as the terminal is already full. So, they can only queue up and wait for their turn to get a spot at the port.

The economic impact of port congestion can be significant, as it leads to delays in the delivery of goods, increased shipping costs, and a decline in trade and economic growth. Congestion can also lead to higher prices for consumers and decreased competitiveness for businesses. The impact of port congestion can be felt across the entire supply chain, affecting everything from manufacturing to retail.

Your goal in this competition is to use satellite imagery to detect ships in ports. The resulting algorithm will allow port managers to better allocate port resources for incoming and outgoing vessels, and make more informed decisions to manage and optimize the logistics.

Ultimately, more accurate detection of ships helps avoid port congestion and ensure functioning supply chains.

### Evaluation
#### Evaluation metric for this competition is mAP at IOU threshold of 0.5.

### Dataset

You can download the dataset <a href="https://huggingface.co/datasets/datadrivenscience/ship-detection">here</a>    

### Solution:

### Exploratory Data Analysis
#### The basic exploratory data analysis of the data,
* Basic image meta data analysis
* RGB color analysis
* Annotation area cluster
#### The above analysis had done by using,
* cv2 
* Image
* numpy
* seaborn
* matplotlib
* pandas

### Model
#### Created 5-kfold split data from entire train dataset.
#### Each fold trained seperately.
#### YOLOv5m6 model trained with the image size 1280, 4-batch, and 50 epochs.
#### YOLOv5x6 model trained with the image size 1280, 2-batch, and 50 epochs.
#### Ensemble model created from YOLOv5m6 and YOLOv5x6.

### RGB color analysis. 

![Alt text](https://github.com/hariprasath-v/HuggingFace-Ship-Detection/blob/main/EDA%20and%20Model%20interpretation%20visualization/RGB%20color%20analysis.PNG)


### YOLOv5m6 mAP 0.5:0.95

![Alt text](https://github.com/hariprasath-v/HuggingFace-Ship-Detection/blob/main/EDA%20and%20Model%20interpretation%20visualization/mAP_0.5-0.95__yolov5m6_1280px_batch_4_5_fold.png)

### YOLOv5x6 mAP 0.5:0.95

![Alt text](https://github.com/hariprasath-v/HuggingFace-Ship-Detection/blob/main/EDA%20and%20Model%20interpretation%20visualization/mAP_0.5-0.95__yolov5x6_1280px_batch_2_5_fold.png)

### Ensemble prediction

![Alt text](https://github.com/hariprasath-v/HuggingFace-Ship-Detection/blob/main/EDA%20and%20Model%20interpretation%20visualization/9.png)

![Alt text](https://github.com/hariprasath-v/HuggingFace-Ship-Detection/blob/main/EDA%20and%20Model%20interpretation%20visualization/103.png)


### File information

ship-detection-huggingface-competition-eda.ipynb[![Open in Kaggle](https://img.shields.io/static/v1?label=&message=Open%20in%20Kaggle&labelColor=grey&color=blue&logo=kaggle)](https://www.kaggle.com/code/hari141v/ship-detection-huggingface-competition-eda)
 
ship-detection-huggingface-competition-model.ipynb[![Open in Kaggle](https://img.shields.io/static/v1?label=&message=Open%20in%20Kaggle&labelColor=grey&color=blue&logo=kaggle)](https://www.kaggle.com/code/hari141v/ship-detection-huggingface-competition-model)
 
 
   
        

