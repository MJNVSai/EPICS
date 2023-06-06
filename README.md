# EPICS

This project aims to present a compilation of the most outstanding deep learning strategies focused on the automatic generation of medical reports from X-Ray images.
![image](https://github.com/MJNVSai/EPICS/assets/94554110/ce086ed8-c5ec-48a2-941a-90652dc7af96)

# Problem Statement
The chest x-ray is the most commonly performed diagnostic x-ray examination. A chest xray produces images of the heart, lungs, airways, blood vessels, and the bones of the spine
and chest. Often time, it is the duty of a radiologist to conclude these x-rays so that to give
appropriate treatment to the patients. It is often time-consuming and tedious to get detailed
medical reports from these x-rays. In high population countries, a radiologist may come
across 100s of x-ray images. This project aims to present a compilation of the most
outstanding deep learning strategies focused on the automatic generation of medical reports
from X-Ray images. In order to handle this challenging problem, deep learning algorithms
have been include with models, to get promising results. So if a properly learned deep
learning model can automatically generate these medical reports, considerable work and
time can be saved. In this project an Encoder and decoder with attention model is used to
generate the text report and pretrained CheXnet model is used to obtain the image features.
The generated text report is evaluated by BLEU score.

# Pre - Processing Data
In this phase the text data are preprocessed to remove unwanted tags, texts, punctuation and numbers. Perform basic decontractions i.e words like won’t, can’t and so on will be converted to will not, can not and so on respectively. We will also check for the empty cell or NaN values and If there are any empty cells
in the image name column we will drop those cells.Each text column word counts are calculated and added to the data frame column.If there any empty
or NaN value in text data we will replace it with “No <Column Name>” (ex: No Impression) After the data preprocessing step, we have a total of 3851 rows
present in the final data points.

 # Architecture Diagram
![image](https://github.com/MJNVSai/EPICS/assets/94554110/780a2c5c-90eb-4133-962f-e4f2cf46dcf8)
  

 # Alogithms :
 - LSTM Algorithm
 - GRU Algorithm

# GRU Algorithm
1.  Update Gate(z) :It determines how much of the past knowledge needs to be passed along into the future. It is analogous to the Output Gate in an LSTM recurrent unit.
2.  Reset Gate(r):It determines how much of the past knowledge to forget. 
3.  Current memory Gate(h(t)): it is a sub-part of the Reset gate and to reduce the effect that previous information has on the current information that is being passed into the future.

  
# LSTM Algorithm
1.Forget Gate(f) :It determines to what extent to forget the previous data.
2.Input Gate(I):It determines the extent of information be written onto the Internal Cell State.
3.Input Modulation gate(g): It is considered as a sub-part of the input gate. It is used to modulate the information that the Input gate will write onto the Internal State Cell
4.Output Gate(o):It determines what output(next Hidden State) to generate from the current Internal Cell State.

# BLEU SCORE
Bilingual Evaluation Understudy is the abbreviation for this score. In this case, the BLEU score will be the metric. The BLEU score determines the how many words are predicted from the original sentence by comparing each word in the model predicted sentence to the reference sentence in dataset (also done in ngrams format). It gives back a number between 0 and 1. The two are quite comparable if the metric is close to 1

### BLEU Formula's
![image](https://github.com/MJNVSai/EPICS/assets/94554110/c44ac549-0302-4ce3-92c9-748ca3d3e9e9)

![image](https://github.com/MJNVSai/EPICS/assets/94554110/4c8a4fb2-7c53-40a4-a82e-404d60fb7ae4)

![image](https://github.com/MJNVSai/EPICS/assets/94554110/885931bd-3631-45e9-acc1-3ec42921fcc3)

# Result Analysis
![image](https://github.com/MJNVSai/EPICS/assets/94554110/e73c9c12-2b98-4d47-ba31-db2db0865ba0)

 **Report** : Hence generated a text report for given x-ray images with BLEU score 0.82
  

![image](https://github.com/MJNVSai/EPICS/assets/94554110/41f138e5-83a4-49b8-9a9b-d152d932080a)
**Report** :  Hence generated a text report for given x-ray images with BLEU score 0.79
  
  
# Conclusion :
We just saw an end-to-end deep learning case study of image captioning in the medical field. We understood the problem and the need for such applications. Here we generated a report on chest x-rays and generated report by model is measured by BLEU score. By building an Attention model, The results are promising and the impression statements are meaningful according to the X-ray image.










