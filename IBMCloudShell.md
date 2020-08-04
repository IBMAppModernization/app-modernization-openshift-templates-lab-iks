# Pre-work

This section will guide you through the pre-requisites and setup of the environment used in this workshop labs. It is broken up into the following steps:

1. [Sign up for IBM Cloud](#1-sign-up-for-ibm-cloud)
1. [Login to IBM Cloud](#2-login-to-ibm-cloud)
1. [Open Cloud Shell](#3-open-cloud-shell)
1. [Connect to OpenShift Cluster](#4-connect-to-openshift-cluster)

## 1. Sign up for IBM Cloud

You will need an IBM Cloud ID for the workshop. If you already have an IBM Cloud ID, proceed to the next section. To create an ID:

* Follow the steps outlined in [NEWACCOUNT](NEWACCOUNT.md).

## 2. Login to IBM Cloud

To login to IBM Cloud,

1. Go to https://cloud.ibm.com in your browser and login.

1. Make sure that you are in the correct account#.

    ![Account Number](../.gitbook/generic/account-number.png)

>Note: you may not have access to your OpenShift cluster if you are not in the right account#.

## 3. Open Cloud Shell

Most of the labs will run CLI commands. The IBM Cloud Shell is preconfigured with the full IBM Cloud CLI and tons of plug-ins and tools that you can use to manage apps, resources, and infrastructure.

1. From the [IBM Cloud Home Page](https://cloud.ibm.com), select the terminal icon in the upper right hand menu.

    ![Terminal Button](../.gitbook/generic/access-cloud-shell.png)

1. It might take a few moments to create the instance and a new session which automatically logs you in through the IBM Cloud CLI.

    ![Cloud Shell](../.gitbook/images/grant-cluster/cloud-shell.png)

    > *Note: Ensure the cloud shell is using the same account where your cluster is provisioned. Check that the account name shown in the top right of the screen, next to `Current account` is the correct one.*

## 4. Connect to OpenShift Cluster

1. In a new browser tab, go to https://cloud.ibm.com/kubernetes/clusters?platformType=openshift.

1. Select your cluster instance and open it.

1. Click `OpenShift web console` button on the top.

1. Click on your username in the upper right and select `Copy Login Command` option.

    ![Terminal Button](../.gitbook/generic/copy-openshift-cmd.png)

1. Click the `Display Token` link.

1. Copy the contents of the field `Log in with this token` to the clipboard. It provides a login command with a valid token for your username.

1. Go to the `Cloud Shell` tab.

1. Paste the `oc login command` in the IBM Cloud Shell terminal and run it.

1. After login to your cluster, set an environment variable for your cluster.

   ```shell
   export CLUSTER_NAME=<your_cluster_name>
   ```

1. Verify you connect to the right cluster.

   ```shell
   kubectl get pod
   ```


