1. create env

''' cmd
python -m venv myenv
'''

2. activate env

'''
myenv/scripts/activate
'''

3. create your project folder -> go to the folder

4. create req file and install the req

'''
pip install -r requirements.txt
'''

5. download the data from and keep it in data_given folder

https://drive.google.com/drive/folders/18zqQiCJVgF7uzXgfbIJ-04zgz1ItNfF5?usp=sharing

6. initialize git

git init

7. initialize dvc

dvc init

8. track data with dvc

dvc add data_given/winequality.csv

9. track code with git

git add .

10. commit to git

git commit -m "first commit"

git add . && git commit -m "first commit"

11. create github repo

12. connect with remote repo

git remote add origin https://github.com/manas149/simple_app_mlops.git

13. rename the branch

git branch -M main  ## rename master to main

14. push to repo

git push origin main


15. write files in src and write stages in dvc.yaml :

data_load --> data_split --> train_and_evaluate

16. run this command to track changes

dvc repro

17. To see the changes

dvc params diff
dvc metrics show

18. create tox.ini file

19. create tests dir and test_config.py/ conftest.py/ __init__.py

20. to run tests 
pytest -v

21. run tox

22. when requirements file is updated
tox -r ## for rebuilding

23. create setup.py and write packages in it

24. run pip install -e .
to install local packages created inside setup.py

25. build your own package and make it shareable
python setup.py sdist bdist_wheel

26. to open jupyter in notebooks folder
jupyter-lab notebooks/  

27. create custom error and write it to tests/test_config.py

28. install flake8 for linting and add it to tox.ini and run tox -r

29. create prediction_service, webapp, app.py and their files

30. write templates files

31. write in to app.py

32. copy model from saved_models to prediction_service/models
cp saved_models/model.joblib prediction_service/model/

33. create the workflows for deploying this app on heroku (using github actions)
mkdir -p .github/workflows/ci-cd.yaml

34. deploy on heroku or something else

35. create Procfile and specify server

----------- ci-cd done --------------

36. now for model versioning we will use mlflows

37. write to prediction.py file -> in this create schecma_in.json file

38. update templates and app.py accordingly

39. write conftest.py file and test_config.py

40. copy schema_in.json from prediction_service to tests
cp prediction_service/schema_in.json tests/