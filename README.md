## ML-Model-Flask-Deployment
This is a demo project to elaborate how Machine Learn Models are deployed on production using Flask API

### Prerequisites
You must have Scikit Learn, Pandas (for Machine Leraning Model) and Flask (for API) installed.

### Project Structure
This project has four major parts :
1. model.py - This file contains the code for our Machine Learning model to predict employee salaries based on training data in 'hiring.csv' file.
2. app.py - This file contains Flask API that receives employee details through GUI or API calls, computes the precited value based on our model and returns it.
3. request.py - This file uses, requests module to call APIs already defined in app.py and dispalys the returned value.
4. templates - This folder contains the HTML template to allow user to enter employee detail and displays the predicted employee salary.
5. requirements.txt - This file contains, the list of all the liabraries with their respective versions, reuired to run the flask app successfully.

### Running the project
1. Ensure that you are in the project home directory. 
   Create virtual environment and run the following command to install all the required liabraries.
'''
pip install -r requirements.txt    
''' 
2. Create the machine learning model by running below command
```
python model.py
```
This would create a serialized version of our model into a file model.pkl

3. Run app.py using below command to start Flask API
```
python app.py
```
By default, flask will run on port 5000.

4. Navigate to URL http://localhost:5000

You should be able to view the homepage as below :
![alt text](http://www.thepythonblog.com/wp-content/uploads/2019/02/Homepage.png)

Enter valid numerical values in all 3 input boxes and hit Predict.

If everything goes well, you should  be able to see the predcited salary vaule on the HTML page!
![alt text](http://www.thepythonblog.com/wp-content/uploads/2019/02/Result.png)

4. You can also send direct POST requests to FLask API using Python's inbuilt request module
Run the beow command to send the request with some pre-popuated values -
```
python request.py
```
