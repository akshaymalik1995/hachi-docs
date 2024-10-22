# How to Enable Google Photos in Google Cloud Console and Download the Configuration File from Scratch
Google Photos API allows you to interact with users' Google Photos libraries, giving you the ability to organize, share, and even download their photos or albums via a programmatic interface. To work with the API, you first need to enable it in Google Cloud Console and set up proper authentication using OAuth 2.0. Here's a step-by-step guide to getting everything up and running.
## Step 1: Create a New Project in Google Cloud Console
If you don't already have a project in Google Cloud Console, the first thing you'll need to do is create one.
1. **Go to Google Cloud Console**: Open [Google Cloud Console](https://console.cloud.google.com/).
2. **Create a New Project**:
   - Click the project dropdown in the top left of the console.
   - Click on "New Project."
   - Provide a name for your project and select an organization (if required).
   - Click on **Create**.
   
Once the project is created, you'll be directed to its dashboard.
## Step 2: Enable Google Photos API
Now that your project is ready, you need to enable the Google Photos API.
1. **Navigate to the API Library**:
   - From the left sidebar, click on **APIs & Services** and select **Library**.
   - In the search bar, type **Google Photos Library API**.
   
2. **Enable the API**:
   - Click on the **Google Photos Library API** result.
   - Press the **Enable** button.
## Step 3: Configure OAuth Consent Screen
Before you can access users' Google Photos, you need to set up an OAuth consent screen.
1. **Go to the OAuth Consent Screen**:
   - From the left sidebar, click on **APIs & Services** and select **OAuth consent screen**.
   
2. **Choose the User Type**:
   - If you're just testing or building a personal app, you can select **External**.
   - If your app is for internal use within your organization, select **Internal**.
   
3. **Fill in App Information**:
   - Provide your **App Name**, **User Support Email**, and other required details.
   - Add **Scopes**. Scopes define what level of access your app has to user data. For Google Photos, the key scope is `https://www.googleapis.com/auth/photoslibrary.readonly` to allow read access to photos.
   
4. **Add Test Users**:
   - For testing purposes, you'll need to specify the email addresses of users who can access your app during the OAuth process.
   
5. **Save and Continue**: Once you've filled in all the required information, click **Save and Continue**.
## Step 4: Create OAuth Credentials
To interact with Google Photos API, you'll need OAuth 2.0 credentials.
1. **Go to the Credentials Page**:
   - From the left sidebar, select **APIs & Services**, then **Credentials**.
   
2. **Create New Credentials**:
   - Click on **+ Create Credentials** and select **OAuth 2.0 Client IDs**.
3. **Configure the OAuth Client**:
   - Choose **Web Application** as the application type.
   - Provide a name for your credentials.
   
4. **Add Authorized Redirect URIs**:
   - If you're building a web app, add your app's redirect URIs. These are the endpoints where Google will send the response to your authentication requests.
   - If you're just testing, you can use `http://localhost`.
5. **Create Credentials**:
   - Once you've configured everything, click **Create**.
6. **Download the Config File**:
   - After creating the credentials, you'll be provided with a **client ID** and **client secret**.
   - Click on the **Download JSON** button to download the credentials file. This file will contain your **client ID**, **client secret**, and other configuration details needed to authenticate users via OAuth.
This JSON file is crucial for interacting with the Google Photos API in your application.
