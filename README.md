### **DoB – Detection of Buildings – Third-year Software Engineering – Deep Learning**

---


#### **The source codes and the final report of the project are all available on [GitHub](https://github.com/Andrius-Sukys/DL-DetectionOfBuildings).**

#### **The datasets, predictions and output models due to their big size of the project are all available on [Google Drive](https://drive.google.com/drive/folders/1jMvX0dYo60M-s_ZaNAo_Fe_TC1f5Tut7?usp=sharing).**

---

`DoB - ImageNet weights.ipynb`

> Variation using standard ImageNet weigths of mean = [0.485, 0.456, 0.406], std = [0.229, 0.224, 0.225].

`DoB - mean = [0, 0, 0], std = [1, 1, 1].ipynb`

 > Variation using weigths of mean = [0, 0, 0], std = [1, 1, 1].

`DoB - Test Environment.ipynb`

> Project created to test the models. The models are available on [Google Drive](https://drive.google.com/drive/folders/1jMvX0dYo60M-s_ZaNAo_Fe_TC1f5Tut7?usp=sharing).
> 
> In order to test a model, download a selected model from Google Drive, upload it to path `../models/` of your project and run the REST API interface.
> 
> Do not forget to upload the included file `segmentator.html` to root folder of the project, otherwise the test environment will not work!

`DoB - Report.pdf`

> The final report of the project, including description, tools, methods, results, references and everything else.

---

#### **Team Bag – Andrius Šukys, Benas Skripkiūnas, Greta Virpšaitė**

---

**The Objective.** The main purpose of the task was to create a UNet-based binary semantic segmentation model that would be able to recognize buildings in the given satellite pictures as accurately as possible.

**The Process.** Two models were run in parallel:
* one with common ImageNet weights of *`mean = [0.485, 0.456, 0.406], std = [0.229, 0.224, 0.225]`* which in turn made it a fine-tuning task,

* the other model was given weights of *`mean = [0, 0, 0], std = [1, 1, 1]`* to train the model from scratch.

Both models were trained on thresholds from 0.1 to 0.9 (with step of 0.1) to determine which threshold works best for the aforementioned given weights. Then the models of both weight sets using their best threshold values were compared in practice using a test dataset.

**The Results.** The results of the aforementioned process were analyzed in the final report.

