##LAB: Google Cloud Fundamentals: Getting Started with App Engine

#Objectives:
In this lab, you learn how to perform the following tasks:
	- Initialize App Engine.
	
	- Preview an App Engine application running locally in Cloud Shell.
	
	- Deploy an App Engine application, so that others can reach it.
	
	- Disable an App Engine application, when you no longer want it to be visible.
	
###Task 1 : Initialize App Engine.
##Steps:

 1. Initialize App Engine.
 
	gcloud app create --project=qwiklabs-gcp-04-e0871c8d547e
	
 2. Clone the source code repository for a sample application in the hello_world directory
 
 	git clone https://github.com/GoogleCloudPlatform/python-docs-samples
 	
 3. Navigate to the source directory
 
 	cd python-docs-samples/appengine/standard_python3/hello_world
 
###Task 2: Run Hello World application locally
##Steps :
 1. Execute the following command to download and update the packages list
 
	sudo apt-get update 
 
 2. Set up a virtual environment in which you will run your application
 
 	sudo apt-get install virtualenv
 	
    If prompted [Y/n], press Y and then Enter
    
    	virtualenv -p python3 venv
    	
 3. Activate the virtual environment
 
 	source venv/bin/activate
 	
 4. Navigate to your project directory and install dependencies
 
 	pip install  -r requirements.txt
 
 5. Run the application
 
 	python main.py
 
###Task 3: Deploy and run Hello World on App Engine
##Steps :
 1. Navigate to the source directory
 
 	cd ~/python-docs-samples/appengine/standard_python3/hello_world
 
 2. Deploy your Hello World application
 
 	gcloud app deploy
 	
    If prompted "Do you want to continue (Y/n)?", press Y and then Enter.
    
 3. Launch your browser to view the app at http://qwiklabs-gcp-04-e0871c8d547e.appspot.com
 	gcloud app browse
 
###Task 4: Disable the application

	gcloud main.py delete
	
	
	
	##### End of Lab
 	
 	
 	
 	
 	
 	
 	
 	
 	
 	
 	
 	
