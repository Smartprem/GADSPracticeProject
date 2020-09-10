##LAB: Console and Cloud Shell

##Objectives
In this lab, you learn how to perform the following tasks:

	- Get access to Google Cloud.

	- Create a Cloud Storage bucket using the Cloud Console.

	- Create a Cloud Storage bucket using Cloud Shell.

	- Become familiar with Cloud Shell features.
	
##Task 1 : Create a bucket using the Cloud Console
	
	- Will be done on next task
	
##Task 2 : Create a Cloud Storage bucket using Cloud Shell
	
	gsutil mb gs://stevex_bucket
	
##Task 3: Explore more Cloud Shell features
##Steps :
 1. Upload a file
 	
 	cloudshell upload Resume.pdf
 
 2. Confirm that the file was uploaded
 	
 	ls
 
 3. Copy the file into one of the bucket created earlier in the lab
 
 	gsutil cp 'Resume.pdf' gs://stevex_bucket
 
### Task 4: Create a persistent state in Cloud Shell
##Steps :
 1. List available regions
 
 	gcloud compute regions list
 
 2. Select a region from the list and note the value in any text editor
 
 	14 - us-central1
 
 3. Create and verify an environment variable
 
 	- Create an environment variable:
 
 		INFRACLASS_REGION=us-central1
 
 	- Verify it with echo:
 
 		echo $INFRACLASS_REGION	
 
 	   Result : us-central1
 
 4. Append the environment variable to a file
 
 	- Create a subdirectory for materials used in this class:
 
 		mkdir infraclass
 
 	- Create a file called config in the infraclass directory:
 
 		touch infraclass/config
 
 	- Append the value of your Region environment variable to the config file:
 
 		echo INFRACLASS_REGION=$INFRACLASS_REGION >> ~/infraclass/config
 
 	- Create a second environment variable for your Project ID:
 
 		INFRACLASS_PROJECT_ID=qwiklabs-gcp-03-0e06954b708d
 
 	- Append the value of your Project ID environment variable to the config file:
 
 		echo INFRACLASS_PROJECT_ID=$INFRACLASS_PROJECT_ID >> ~/infraclass/config
 
 	- Use the source command to set the environment variables, and use the echo command to verify that the project variable was set:
 
 		source infraclass/config

	        echo $INFRACLASS_PROJECT_ID

	- Issue the echo command again:

	        echo $INFRACLASS_PROJECT_ID

 5. Modify the bash profile and create persistence

 	- Edit the shell profile:

 		nano .profile

 	- Add the following line to the end of the file:

 		source infraclass/config

 	- Press Ctrl+O, ENTER to save the file, and then press Ctrl+X to exit nano:

 	- Use the echo command to verify that the variable is still set:

 		echo $INFRACLASS_PROJECT_ID

 		 		
 		##### End of Lab
 
 
