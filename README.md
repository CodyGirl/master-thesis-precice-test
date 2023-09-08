
# Instructions

## GitHub Personal Access Token

- Navigate to your GitHub account
- From the top right icon, navigate to settings
- From the left menu bar, scroll to the bottom and select developer settings
- Now click on 'Personal Access Tokens' > 'Tokens classic'
- Choose 'Generate New Token' > 'Generate New Token (classic)' and give a suitable name along with an expiration date
- Now, carefully choose the permissions as stated in the below list. The permissions stated with a (*) are optional in nature:
  - repo:status, repo_deployment, public_repo, repo:invite
  - read:packages
  - read:org
  - notifications (*)
  - read:user, user:email
  - read:discussion (*)
  - read:enterprise (*)
  - read:audit_log (*)
  - read:project
- Click on 'Generate Token' button
- Copy the generated token and save in a text editor as it cannot be found on github again.

## Running the application

- Clone the repository using ```git clone https://github.com/CodyGirl/master-thesis-precice-test.git```
- Go to the root folder and rename `sample.env` to `.env`
- Open the .env file in a editor and replace the `<github_personal_access_token>` with the personal access token created in the previous steps
- Run ```docker-compose up```

This may take sometime dependening on the internet connection and RAM of the system.
Make sure to have port 3000 free for this application to run successfully.

## Visit application

- Open a web browser and navigate to localhost:3000
- Login using username and password mentioned in the .env file
- Current user has admin rights so, user can play around and explore what all can be done on the dashboard. However, changes can not be saved using the GUI for preventing tampering of the image.
