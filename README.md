# anonymization-on-ml-models
Comp430 Term Project - Fall2022<br>

Github Repo Link: https://github.com/ggunes18/anonymization-on-ml-models<br>

How to run Anonymizers :gear::

1) Mondrian Anonymizer (IMPORTANT: It works only with Python 2.7)<br>
-Clone the repository using following command:<br>
``` git clone https://github.com/ggunes18/anonymization-on-ml-models.git ```<br>
-Then change directory to this repo.<br>
-In order to use Mondrian anonymizer, you should use cd command to get into the directory of Basic_Mondrian.<br>
``` cd Basic_Mondrian/ ```<br>
-Then run the anonymizer.py code with parameter c which stands for insurance. For instance:<br>
``` python anonymizer.py c ```<br>
-The anonymized data can be found in data/anonymized.data directory. Rename its extension from .data to .csv. Then add a header as age;sex;bmi;children;smoker;region;charges to the first line.<br>

Domain generalization Hierarchies can be found in data/insurance_****.txt files. The input dataset that is modified for mondrian anonymizer can be found in data/insurance-mondrian-input.csv. <br>
The default K value is 10. It can be changed by changing the DEFAULT_K variable in anonymizer.py.<br>

2) ARX Tool
- Download the ARX tool from: https://arx.deidentifier.org/downloads/<br>
-Give insurance_labeled.csv as input data for ARX.<br>
-Define domaing generalization hierarchies given in the ./ARX/DGHs/***.txt files for each attribute.<br>
-Label "charges" as sensitive attribute and other attributes as "quasi-identifier".<br>
-Define k and l parameters to anonymize the input dataset.<br>
-Perform anonymization.<br>

The ARX project file that was prepared for this project is ./ARX/anonymization.deid file.<br>

How to run Jupyter Notebook Files:<br>
1) Insurance ML Analysis with Original Data<br>
-Change directory to the directory of this repo.<br>
-From terminal open up jupyter notebook by using:<br>
``` jupyter notebook ```<br>
-Open the InsuranceMLAnalysis.ipynb<br>
-Run all of the cells to see the results of evaulation metrics.<br>

You can change the model by commenting out the current model and uncommenting another model.<br>

2) Insurance ML Analysis with Anonymized Data<br>
-Open the InsuranceMLAnalysisAnon.ipynb<br>
-In the pd.read_csv function pass the path of the anonymized file with appropriate seperator such as:<br>
"Mondrian_k_5_anon_insurance.csv"<br>
-Run all of the cells to see the results of evaluation metrics.<br>

You can change the model by commenting out the current model and uncommenting another model.<br>


References<br>
Basic Mondrian is cloned from https://github.com/qiyuangong/Basic_Mondrian. We modified it for our dataset.<br>
ARX Tool can be reached from https://arx.deidentifier.org/<br>
