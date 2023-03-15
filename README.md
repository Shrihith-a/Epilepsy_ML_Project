
# **Epilepsy Machine Learning Project**

### **Problem Statement**
#### Epilepsy is a nervous system disorder that affects movement. The dataset contains 195 records of various people with 23 features that contain biomedical measurements. Your model will be used to differentiate healthy people from people having the disease. Target Column is 'status'. Identify the model with the best params.
====================================================================================
#### ****Source Link for Data: https://github.com/edyoda/data-science-complete-tutorial/blob/master/Data/epilepsy.data****
====================================================================================

### ***1. Setup.py***
#### a. Setting setup tools by providing details of setup in Python
#### b. To get the requirements and package information and App version number

```python
# C. Import required packages

from setuptools import find_packages,setup
from typing import List

HYPEN_E_DOT='-e .'
def get_requirements(file_path:str)->List[str]:
    '''
    this function will return the list of requirements
    '''
    requirements=[]
    with open(file_path) as file_obj:
        requirements=file_obj.readlines()
        requirements=[req.replace("\n","") for req in requirements]

        if HYPEN_E_DOT in requirements:
            requirements.remove(HYPEN_E_DOT)
    
    return requirements

setup(
name='Epilepsy ML Project',
version='0.0.1',
author='Shrihith A',
author_email='ashrihith93@gmail.com',
packages=find_packages(),
install_requires=get_requirements('requirements.txt')
)
```

### ***2. requirements.txt***
#### a. Required packages for Projects is mentioned
#### b. requirements.txt
```text
pandas
numpy
seaborn
matplotlib
scikit-learn
catboost
xgboost
dill
-e .
```

### ***3. Create anaconda virtual Environment***
#### a. Creating virtual environment is a best practice 
```python
conda create -p venv python==3.9 -y
conda activate venv
```

### ***4. Install required packages mentioned in requirements***
a. install required packages inside venv environment
b. These below command install all the required packages
```pip
pip install pandas numpy seaborn matplotlib scikit-learn catboost xgboost dill
```

