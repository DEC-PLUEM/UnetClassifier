# UnetClassifier
## **model overiew work flow**       

concept Layer : encoder{Resnet50} -> decoder -> **mask** -> flatten{**mask**} -> fully-connected layers{in=2^16,out=3} -> softmax

**log validate accuracy**


<img width="497" alt="image" src="https://github.com/Dont-HurtMe/UnetClassifier/assets/154254885/9a889e62-0d52-4dca-a500-6768e814ee23">



**evaluate (test-set)**
* entropyloss:0.7264 
* accuracy:0.9242 
* f1-score:0.9236
* precision:0.9245 
* recall:0.9242
* auc:0.9509 

**confusion matrix**
| label name| benign | malignant | normal |
| --- | --- | --- | --- |
| benign  | 237  | 3 | 2 |
| malignant  | 4 | 211  | 27  |
| normal  | 3 | 47  | 192  |

**detail training & evaluate in create-unet-classifier.ipnyb






