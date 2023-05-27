create env

''' cmd
python -m venv myenv
'''

activate env

'''
myenv/scripts/activate
'''

create your project folder -> go to the folder

create req file and install the req

'''
pip install -r requirements.txt
'''

download the data from

https://drive.google.com/drive/folders/18zqQiCJVgF7uzXgfbIJ-04zgz1ItNfF5?usp=sharing

git init

dvc init

dvc add data_given/winequality.csv

git add .

git commit -m "first commit"

git add . && git commit -m "first commit"

create github repo

git remote add origin https://github.com/manas149/simple_app_mlops.git

git branch -M main  ## rename master to main

git push origin main


stages :

data_load --> data_split --> train_and_evaluate

dvc repro

dvc params diff
dvc metrics show