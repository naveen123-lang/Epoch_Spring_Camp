# &#x09;	TECHNICAL REPORT OF TASK 4



1. ### Architectural Diagram of Multi model

<img width="1768" height="1606" alt="graphviz" src="https://github.com/user-attachments/assets/95b74ae0-1279-4970-870e-ac9c8685f915" />



* I used a Late fusion model which have more weightage in predictions to CNN model rather than a LSTM model.
* First I will tell about my CNN model, It's a standard CNN model in which I used 3 convolutional -> ReLU -> Max pooling loops and later passed through a Linear network for predictions. With this three loops I was able to capture a very good amount of information from the spectrogram images so my unimodal of CNN gave a good accuracy of 82-83%.
* Second about the LSTM model , this turned out to be a very poor model for emotion recognition part using text transcripts , because all the emotions ended with same text which gave no information to the model and it performed bad in this.
* Lastly , about the fusion model the main reason for me to use a late fusion model was the problem in LSTM which was useless in this case for identification of emotion , by using a late fusion model I managed to give a large weightage to CNN and less weightage to LSTM model which can help in better performance of the fusion model.
* Practically, it's easy to code and understand a late fusion model that was also an important reason to choose it.



### 2\. Result Table 

|              CNN MODEL|                LSTM MODEL|             LATE FUSION MODEL|
|-|-|-|
|              88.89%|                  12.5%|                 73.95%|
| Able to capture the features better|Wasn't able to learn anything , actually we can't do anything the task was not suitable for this might have worked if we used it for image features.|Mostly reliable on CNN model so better accuracy|



### 3\. Training and Validation Loss Plots



##### \-> CNN MODEL

<img width="1058" height="682" alt="Screenshot 2026-05-12 214846" src="https://github.com/user-attachments/assets/e4cd72bd-1cd9-4649-8dd7-9e88c01af7e2" />




##### \-> LSTM MODEL

<img width="1083" height="681" alt="Screenshot 2026-05-12 214818" src="https://github.com/user-attachments/assets/84b000b3-94b2-4d11-916e-59289b9fec72" />























