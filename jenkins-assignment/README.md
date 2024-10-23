# Jenkins CI/CD for JavaScript Application

## Jenkins Freestyle Project for Todo List App

This guide provides step-by-step instructions on how I set up a Jenkins CI/CD pipeline for the Todo List application. 

### Step 1: Fork the Repository
1. Go to the [Todo List App Repository](https://github.com/sanoojes/simple-todo-app).
2. Click on the **Fork** button in the top right corner to create a copy in your GitHub account.

### Step 2: Install Jenkins
1. I am on a **Windows machine**, and I followed this guide to install Jenkins: [Jenkins Installation on Windows](https://phoenixnap.com/kb/install-jenkins-on-windows).
2. During the installation, I figured I needed to have JAVA installed and specifically JDK 21. I followed this guide to set up JDK 21: [Install JDK 21](https://youtu.be/XdgNWJlVeEg?si=FFQrQjEVTefiew9H).
3. Once the JDK is installed, I proceeded to finish installation for Jenkins still folowing the guide above. 
4. After the installations, I proceeded to `http://localhost:8080` to access Jenkins.

### Step 3: Create a Jenkins Freestyle Project
1. In the Jenkins dashboard, click on "New Item".
2. Choose "Freestyle project."
3. Name your job (e.g., "Build Todo App").

### Step 4: Configure Source Control
1. In the job configuration, locate the **Source Code Management** section.
2. Choose "Git."
3. Enter the URL of your forked repository.

### Step 5: Add Build Steps
1. In the job configuration, scroll down to the **Build** section.
2. Click on "Add build step" and I since I was on Windows I selected "Execute Windows batch command"
3. In the command box, add the commands to build your app:
```
echo "Building HTML/CSS/JS project"
```

### Step 6: Archive the Build Artifacts
**Post-build Actions:**
1. Add a post-build action to "Archive the artifacts".
2. Specify the files to archive. For example:
```
*.html, *.css, *.js
# This will archive all files in the workspace
```

### Step 7: Save and Verify Build
**Save the Job**
Build Now: Click on "Build Now" to run the job and build your application.
After the build completes, check the console output for any errors.
Access the archived artifacts from the build's page in Jenkins to see the files generated during the build process.
 
