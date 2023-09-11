# Steps to deploy Observability and Change Tracking tool for preCICE

Author: Nistha Bhawsinka

## Requirements

User needs to have docker-compose installed on their systems.

## Step 1: Creating a GitHub Personal Access Token

- Go to your GitHub profile.
- From the top right icon, navigate to settings.
- From the left menu bar, scroll to the bottom and select developer settings.
- Now click on 'Personal Access Tokens' > 'Tokens classic'.
- Choose 'Generate New Token' > 'Generate New Token (classic)' and give a suitable name along with an expiration date.
- Choose the permissions as stated in the below list.
  - Mandatory permissions:
    - Under repo, select: status, repo_deployment, public_repo, repo:invite
    - Under write:packages, select: read:packages
    - Under admin:org, select: read:org
    - Under user, select: read:user, user:email
    - Under project, select: 	read:project
  - Optional permissions:
    - notifications
    - read:discussion
    - read:enterprise
    - read:audit_log
- Click on 'Generate Token' button.
- Copy the generated token and save it in a secure way as it cannot be found on GitHub again.

## Step 2: Running the application

- Clone the repository using `git clone https://github.com/CodyGirl/master-thesis-precice-test.git`.
- Go to the root folder and rename `sample.env` to `.env`.
- Open the .env file in a editor and replace the `<github_personal_access_token>` with the personal access token created in the previous steps.
- Run `docker-compose up`.

This may take sometime dependening on the internet connection and RAM of the system. Make sure to have port 3000 free for this application to run successfully.

## Step 3: Visit application

- Open a web browser and navigate to localhost:3000
- Login using username and password mentioned in the .env file
- Current user has admin rights so, user can play around and explore what all can be done on the dashboard. However, changes can not be saved using the GUI for preventing tampering of the image.
