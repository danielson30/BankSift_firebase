# How to Generate a Firebase Service Account Key

1. Go to the [Firebase Console](https://console.firebase.google.com/).
2. Select your project (banksift).
3. Click on the gear icon ⚙️ (Project settings) in the top left corner.
4. Go to the "Service accounts" tab.
5. Click on "Generate new private key" button.
6. Confirm by clicking "Generate key".
7. A JSON file will be downloaded to your computer. This file contains your service account credentials.
8. Keep this file secure and do not commit it to your repository!

# How to Add the Service Account as a GitHub Secret

1. Go to your GitHub repository.
2. Click on "Settings" at the top of the repository.
3. In the left sidebar, click on "Secrets and variables" and then "Actions".
4. Click on "New repository secret".
5. For the name, enter: `FIREBASE_SERVICE_ACCOUNT_BANKSIFT`
6. For the value, paste the entire content of the JSON file you downloaded (including the curly braces).
7. Click "Add secret".

After adding this secret, your GitHub Actions workflow should be able to deploy to Firebase Hosting successfully.
