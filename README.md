# Simple REACT PWA Reference & Quick Start Guide 
              #### - Deploy and host a ReactJS app
	      #### - with AWS Amplify Console
			  <hr/>
			  
## Prerequisites
 - npm
 - node
 - React
 - firebase
 - AWS Account
 - aws cli
 - git
 - aws git configuration
 - AWS CodeCommit Configuration


###  1. Confirm environmental setup

- npm install -g firebase-tools
- node -v;

###  2. Create a new React application

- create-react-app simple-pwa;
- cd simple-pwa
- npm start;

### 3. Build React application

- sudo npm run-script build
- serve -s build

### 4. Deploy on FireBase

- firebase login
- sudo firebase init
- firebase deploy

### 5. Create new repo in AWS-CodeCommit

 - Login to AWS console
 - Go to CodeCommit service
 - create new repository name 'simplereact'

### 6. push local directories files to CodeCommit Repo with git hub commands

 - cd simple-pwa
 - git add .
 - git commit -m 'commit all files'
 - git push https://git-codecommit.XXXXX.amazonaws.com/v1/repos/simplereact --all


### 6. Deploy on AWS using Amplify

 - a. Log in to the AWS Amplify Console
 - b. Deploy your app to AWS Amplify
     - Select Get Started under Deploy.
     - Select GitHub as the repository service and select Next.
     - Choose the repository you created earlier and the master branch, then select Next.
     - Accept the default build settings and select Next.
     - Review the final details and select Save and Deploy.
     - AWS Amplify Console will now build your source code and deploy your app at https://<branchname>.<appid>.amplifyapp.com
     - Once the build completes, select the thumbnail to see your web app up and running live.

### 7. Automatically deploy code changes 

   - a. Edit the src/App.js file.    
   - b. Git push changes in CodeCommit Repository
     - git add .
     - git commit -m "test in statuscheck"
     - git push https://git-codecommit.XXXXX.amazonaws.com/v1/repos/simplereact master
   - c. Once the build is complete, select the thumbnail on the AWS Amplify console to view your updated app.
