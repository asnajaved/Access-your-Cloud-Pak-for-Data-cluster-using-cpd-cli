# Access-your-Cloud-Pak-for-Data-cluster-using-cpd-cli

Cloud Pak for Data command-line interface (cpd-cli) is used to install and manage the Cloud Pak for Data software and to complete administrative tasks on your Red Hat® OpenShift® Container Platform cluster from your local machine.

In this hands-on guide we will learn how to access your Cloud Pak for Data Cluster using Cpd-cli

## Step 1: Installing cpd-cli

### 1.1 Downloading cpd-cli

Based on the version of your Cloud Pak for Data cluster, you can download the cpd-cli command line utility from: https://github.com/IBM/cpd-cli/releases.

### 1.2 Changing directory

Once you have downloaded cpd-cli extract it to a folder of your choice. Now using cmd or powershell (for windows) or Terminal (for MAC) change the directory to cpd-cli folder as shown below

![image](https://user-images.githubusercontent.com/16270682/207262269-829404c8-8451-4911-8658-8ada7e25f209.png)

## Step 2: Creating a profile

Before you can run certain management tasks on your Cloud Pak for Data cluster, you must create a profile to run cpd-cli commands.

### 2.1 Generate API Key

You will need an API key for user authentication 
