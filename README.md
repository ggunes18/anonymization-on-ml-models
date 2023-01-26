# anonymization-on-ml-models
Comp430 Term Project - Fall2022


How to run Anonymizers :gear::

1) Mondrian Anonymizer (IMPORTANT: It works only with Python 2.7)
-Clone the repository using following command:\
``` git clone https://github.com/ggunes18/anonymization-on-ml-models.git ```
-Then change directory to this repo.\
-In order to use Mondrian anonymizer, you should use cd command to get into the directory of Basic_Mondrian.
``` cd Basic_Mondrian/ ```
-Then run the anonymizer.py code with parameter c which stands for insurance. For instance:
``` python anonymizer.py c ```
-The anonymized data can be found in data/anonymized.data directory. Rename its extension from .data to .csv. Then add a header as age;sex;bmi;children;smoker;region;charges to the first line.

Domain generalization Hierarchies can be found in data/insurance_****.txt files. The input dataset that is modified for mondrian anonymizer can be found in data/insurance-mondrian-input.csv. 
The default K value is 10. It can be changed by changing the DEFAULT_K variable in anonymizer.py.

How to run Jupyter Notebook Files:
1) Insurance ML Analysis with Original Data
-Change directory to the directory of this repo.
-From terminal open up jupyter notebook by using:
``` jupyter notebook ```
-Open the InsuranceMLAnalysis.ipynb
-Run all of the cells to see the results of evaulation metrics.

You can change the model by commenting out the current model and uncommenting another model.

2) Insurance ML Analysis with Anonymized Data
-Open the InsuranceMLAnalysisAnon.ipynb
-In the pd.read_csv function pass the path of the anonymized file such as:
"Mondrian_k_5_anon_insurance.csv"
-Run all of the cells to see the results of evaluation metrics.

You can change the model by commenting out the current model and uncommenting another model.
