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

You will need an API key for user authentication. To generate api key go to **Profile and settings** page and click **generate api key**. This API key does not expire.

![image](https://user-images.githubusercontent.com/16270682/207292743-9a43c235-c456-4ce5-a732-f4fc8867fe5f.png)

<img width="1288" alt="image (1)" src="https://user-images.githubusercontent.com/16270682/207292951-e36f2a60-7558-411a-9764-dad849403dca.png">

### 2.2 Create a local user 

Use the below command and Paste the API key generated in previous step to create a local user configuration for yourself.

```
./cpd-cli config users set cpd-admin-user --username admin --apikey api_key

```
where cpd-admin-user is the name you will keep for new local user configuration.

### 2.3 Set a new profile

Create a new profile using the below command to store the Cloud Pak for Data URL and its association with the local configuration

```
./cpd-cli config profiles set cpd-admin-profile --user cpd-admin-user --url cpd-profile-url

```

where cpd-admin-profile is the name you will set for the new profile and cpd-profile-url is the Cloud Pak for Data user profile URL.

##### Note: If you have multiple Cloud Pak for Data instances, you must set a new profile on every instance. You can also have profiles for other users in the same Cloud Pak for Data user profile URL.


You can now run cpd-cli commands with this profile using the --profile flag. For example:

```
./cpd-cli service-instance list --profile cpd-admin-profile

```

## Resources

To learn more about Cloud Pak for Data Command Line Interface visit https://www.ibm.com/docs/en/cloud-paks/cp-data/4.6.x?topic=administering-cpd-cli-cloud-pak-data-command-line-interface

for Common administrative tasks https://www.ibm.com/docs/en/cloud-paks/cp-data/4.6.x?topic=interface-common-administrative-tasks

