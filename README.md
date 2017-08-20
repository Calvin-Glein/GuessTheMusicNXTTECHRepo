ReadMe for Guess The Music by Teamtation
Members:
Paolo de Jesus
Joanna Lau
Glenn Henrick Matias
Nao Portales
 
Step 1: Download Eclipse IDE 4.5 or later
You can get it here: https://www.eclipse.org/downloads/?

Step 2: Install the latest version of Google Cloud SDK
You can get it here: https://cloud.google.com/sdk/docs/

Step 3: Run the following command to add the gcloud component that includes the App Engine SDK for Java:
‘gcloud components install app-engine-java’

Note: You must run this command outside of the directory where you installed the Cloud SDK.

Step 4: Install Cloud for Eclipse
From inside Eclipse, Select Help > Eclipse Marketplace... and search for Google Cloud.

Step 5: Clone the Github repo for Guess The Music
‘https://github.com/Calvin-Glein/NXTTechMusicApp’

Step 6: Import the project to Eclipse
From inside Eclipse, Select File > Import > Existing Projects into Workspace then determine where you cloned the project

Step 7: Running the project locally and checking for conflicts
1.       Select the project in the Project Explorer or Package Explorer.
2.       Open the context menu. (Right click or Ctrl-click)
3.       Select Run As > App Engine
4.       Log messages appear in the console as the server starts up.
5.       Eclipse opens its internal web browser to your application. You can also open an external browser and navigate to http://localhost:8080.
6.       Check for error logs

Step 8: Create a Google Cloud Platform project
You need a Google Cloud Platform project with an App Engine application to deploy to. If you don't have one, use the Cloud Platform Console to set up your project. You can access it here
https://console.cloud.google.com/projectselector/appengine/create?lang=java&st=true&_ga=2.173824934.-467387190.1502949668
1.       Select or create a new Cloud Platform project.
2.       If you need to create an App Engine application for your project, you are prompted to select the region where you want your App Engine application located.
3.       The Dashboard opens after your App Engine application has been created in your project.
4.       Note the project ID. You'll need to supply this to Eclipse shortly.

Step 9: Enable the YouTube Data API v3 (https://developers.google.com/youtube/v3/getting-started used as reference)
1.       Go to the Google Developers Console: https://console.developers.google.com/ and select your project.
2.       Open the API Library in the Developers Console. Under YouTube APIs, click YouTube Data API.
3.       If it isn’t already enabled, click the enable button for YouTube Data API v3.

Step 10: Create an OAuth2.0 Client ID and an API Key for your app
1.       From the Google Developers Console (https://developers.google.com/youtube/v3/getting-started), click credentials.
2.       Click create credentials and select oAuth client ID. Select Web application. Fill in the required fields.  The oAuth client ID is used if you plan to create requests that require authentication.
3.       Copy your client ID. This will be used for the OAUTH2_CLIENT_ID variable in the auth.js file.
4.       Click create credentials again, and this time select API Key. An API key will be generated. The API key will be sufficient for requests that do not require authentication.
5.       Copy your API key. This will be used for the ‘gapi.client.setApiKey’ function found near the bottom of the auth.js file.
 
Step 11: Sign in to Google in Eclipse
In Eclipse, Select the File > Sign in to Google… menu item.
Your system browser, such as Firefox, will open outside of Eclipse and ask for the permissions it needs to manage your App Engine applications.
Click Allow and close the window. Eclipse is now signed into your account.

Step 12: Deploy the Project to App Engine
Prerequisites
1.       The appengine-web.xml file must be in the WEB-INF folder of your web application.
2.       The project must have the App Engine Project facet. If you created it using the wizard, it should already have this facet. Otherwise,
3.       Right click the project in the Package Explorer to bring up the context menu.
4.       Select Configure > Convert to App Engine Project.
To deploy the project to App Engine Standard Environment
1.       Right click the project in the Package Explorer the project to open the context menu.
2.       Select Deploy to App Engine Standard
3.       A dialog pops up.
4.       Select the account you want to deploy with, or add a new account.
5.       The list of projects the account has access to loads. Select the one you want to deploy to.
6.       Click OK.

Step 13: View the project in the browser
After executing step 11, in the console view, you can get the link of the project. Copy and paste it in the browser of your choice.
 
 

--Setup instructions on Firebase
Step 1: Create your Firebase Project
Log in to your Google account in https://console.firebase.google.com/ 
Add a new project.
Fill up the necessary fields and click on ‘Create Project’.

Step 2: Add Firebase to your web app
On the console, click on ‘Add Firebase to your web app’.
Copy the snippet provided.

Below are the list of files that has this snippet of code to connect to our database:
index.jsp
gameRoom.jsp
joinRoom.jsp
mobileRoom.jsp
play.jsp
step1CreateRoom.jsp

Locate the script where we initialized our Firebase and replace our code by pasting the snippet provided earlier to all the files above.
The project can now be used with Firebase!
 
 
 Sources: https://cloud.google.com/eclipse/docs/quickstart


