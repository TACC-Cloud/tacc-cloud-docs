.. role:: raw-html-m2r(raw)
   :format: html
   
=====================
Troubleshooting Guide
=====================




This guide explains how to troubleshoot some issues that users may face when using Tapis or other TACC-Cloud resources. 

If you get through these steps and are still having issues, or are not able to do these steps, please email CICsupport@tacc.utexas.edu.

------


.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **500 error stemming from Upstream server**

     .. code-block:: plaintext

        The most common version of this error is "The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request". 
        This error tends to stem from the SSH keys that the storage system is registered with. If you have the ability to SSH to the storage system's host, you can check your SSH keys with a couple of different tests:

       1. Try to list files on this storage system
       2. Try to manually SSH to the host of the storage system with your key
       3. SSH to the host of the storage system, cd to ~.ssh/authorized_keys. Make sure the key is in this file, is correct, and has no group access rights.
       
       Other things to check:
       1. Find the root dir in your storage system’s definition. SSH to the storage system’s host and make sure you can cd to that root dir as yourself.
       2. Check that there are no typos in your storage system definition. For example, make sure the host in your definition is the same host that your keys are on, and that your root dir is correct. 

|

.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **Password not accepted but I KNOW it’s right**

     .. code-block:: plaintext

        Go to https://<tenant base url>/store and login with your credentials. 
        If you cannot login, please contact CICsupport with one of the above methods. 
        If you can login, Go to My Scriptions and click on the Client drop down box. 
        If you do not see a client in this box titled “DefaultApplication”, run the following command on the command line:

        curl -sku "<username>" -X POST -d "clientName=DefaultApplication" https://<tenant base url>/clients/v2

        This will prompt you for your password. 
        Once you’ve created this client, retry the action requiring your password from earlier.      
        
|





.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **Outputs are failing to archive**

     .. code-block:: plaintext

        Check you job.json to confirm that you do or do not have archive turned on as expected. Then, run the following command:

        curl -k -H “Authorization: Bearer $yourtoken” https://<tenant base url>/files/v2/listings/system/<system id>/<enter archive path here>
        If this command comes back successfully, this means you have access to the entire archive path and the entire path exists. Otherwise, you will receive an error letting you know of one of these issues.   
        
|

.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **Error regarding improper ssh configurations**

     .. code-block:: plaintext

        If you have the ability to SSH to the system's host, first SSH to the host and cd to ~.ssh/authorized_keys. Make sure the key is in this file, is correct, and has no group access. If you are on Stampede2 and you are confident your key is correct, you can try the following steps:

        Move you .ssh directory to .sshold
        Log out and log back in
        CAREFULLY add back any keys you need into your authorized_keys file 
        Deleting the ~/.ssh directory will cause TACC’s scripts to regenerate that directory with the SSH keys it needs.     
        
|





.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **Unable to authenticate to your system with default credential**

     .. code-block:: plaintext

        If you have the ability to SSH to the system's host, try SSHing to the system’s host with your SSH key or password. This will ensure the credentials are correct and MFA is not encountered. 
        If that doesn’t work, your SSH key or password is likely the problem. Otherwise, check your system’s definition for typos – particularly in the system’s name. There should be no trailing characters.  

|

.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **I’m trying to import a package on JupyterHub but it says it can’t be found**

     .. code-block:: plaintext

        We will likely need to install the package for you. Please head to the Request Forms page and send in a request.
        
|

