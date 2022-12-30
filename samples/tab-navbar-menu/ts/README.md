---
page_type: sample
description: Sample personal tab navbar-menu.
products:
- office-teams
- office
- office-365
languages:
- typescript
- nodejs
extensions:
 contentType: samples
 createdDate: "29/12/2022 01:38:27 PM"
urlFragment: officedev-microsoft-teams-samples-tab-navbar-menu-ts
---

# Teams Personal Tab Navbar-Menu Sample TS

Add multiple actions to the upper right NavBar and build an overflow menu for extra actions in an app.

**Note:** NaveBar menu is only supported in Mobile Clients.

## Interaction with app - Mobile

![NavBarGif](Images/MenuGif.gif)

 ## Prerequisites

- Microsoft Teams is installed and you have an account (not a guest account)
-  [NodeJS](https://nodejs.org/en/)
-  [ngrok](https://ngrok.com/) or equivalent tunneling solution

## Setup

1. Setup NGROK

- Run ngrok - point to port 3978

    ```bash
    ngrok http -host-header=rewrite 3978
    ```
2. Setup for code
   - Clone the repository

    ```bash
    git clone https://github.com/OfficeDev/Microsoft-Teams-Samples.git
    ```

  - In a terminal, navigate to `samples/tab-navbar-menu/ts`
   
  - Install modules

      `npm install`

      `npm start`
      
   - The client will start running on 3978 port 

4. Setup Manifest for Teams
- __*This step is specific to Teams.*__
    - **Edit** the `manifest.json` contained in the ./AppPackage folder to replace your GuId and you see the place holder string `{{GuID}}` in the `manifest.json`
    - **Edit** the `manifest.json` for `validDomains` and replace `{{domain-name}}` with base Url of your domain. E.g. if you are using ngrok it would be `https://1234.ngrok.io` then your domain-name will be `1234.ngrok.io`.
    - **Zip** up the contents of the `AppPackage` folder to create a `manifest.zip` (Make sure that zip file does not contains any subfolder otherwise you will get error while uploading your .zip package)

- Upload the manifest.zip to Teams (in the Apps view click "Upload a custom app")
   - Go to Microsoft Teams. From the lower left corner, select Apps
   - From the lower left corner, choose Upload a custom App
   - Go to your project directory, the ./AppPackage folder, select the zip folder, and choose Open.
   - Select Add in the pop-up dialog box. Your app is uploaded to Teams.
   **Note** The navbar menu app is supported only persona scopes.
## Running the sample

**Install App:**

![InstallApp](Images/InstallApp.png)

**MainPage UI:**
![MainPage](Images/MainPage.png)

**Clik 3 small dots (Includes other app options and information):**
![Manu1](Images/Menu1.png)

**Click About Menu:**
![Menu2](Images/Menu2.png)

**Clik 3 small dots (Includes other app options and information):**
![Menu3](Images/Menu3.png)

**Click Contact Menu:**
![Menu4](Images/Menu4.png)

**Clik 3 small dots (Includes other app options and information):**
![Menu5](Images/Menu5.png)


## Further Reading.
[NavBar-Menu](https://learn.microsoft.com/en-us/microsoftteams/platform/concepts/design/personal-apps?view=msteams-client-js-1.12.1#use-a-personal-app-private-workspace)