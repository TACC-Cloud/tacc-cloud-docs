.. role:: raw-html-m2r(raw)
   :format: html
   
=======
TESTING
=======




.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **500 error stemming from Upstream server**

     .. code-block:: plaintext

        The most common version of this error is: The server, while acting as a gateway or proxy, received an invalid response from the upstream server it accessed in attempting to fulfill the request. This error tends to stem from the SSH keys that the storage system is registered with. You can check your SSH keys with a couple of different tests:

       1. Try to list files on this storage system
       2. Try to manually SSH to the host of the storage system with your key
       3. SSH to the host of the storage system, cd to ~.ssh/authorized_keys. Make sure the key is in this file, is correct, and has no group access.
       Other things to check:

       1. Find the root dir in your storage system’s definition. SSH to the storage system’s host and make sure you can SSH to that root dir as yourself.
       2. Check that there are no typos in your storage system definition. For example, make sure the host in your definition is the same host that your keys are on, and that your root dir is correct. 

|

.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **Password not accepted but I KNOW it’s right**

     .. code-block:: plaintext

        {
        "username": "$USERNAME",
        "internalUsername": null,
        "permission": {
          "read": true,
          "write": false
        },
        "_links": {
          "self": {
            "href": "https://agave.iplantc.org/jobs/v2/$JOB_ID/pems/$USERNAME"
          },
          "parent": {
            "href": "https://agave.iplantc.org/jobs/v2/$JOB_ID"
          },
          "profile": {
            "href": "https://agave.iplantc.org/profiles/v2/$USERNAME"
          }
        }
        }
|





.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **Outputs are failing to archive**

     .. code-block:: plaintext

        # General grant
        curl -sk -H "Authorization: Bearer $ACCESS_TOKEN" \
            -H "Content-Type: application/json" \
            -X POST --data-binary '{"permission":"READ","username":"$USERNAME"}' \
            https://agave.iplantc.org/jobs/v2/$JOB_ID/pems

        # Custom url grant
        curl -sk -H "Authorization: Bearer $ACCESS_TOKEN" \
            -H "Content-Type: application/json" \
            -X POST --data-binary '{"permission":"READ"}' \
            https://agave.iplantc.org/jobs/v2/$JOB_ID/pems/$USERNAME
|

.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **Error regarding improper ssh configurations**

     .. code-block:: plaintext

        {
        "username": "$USERNAME",
        "internalUsername": null,
        "permission": {
          "read": true,
          "write": false
        },
        "_links": {
          "self": {
            "href": "https://agave.iplantc.org/jobs/v2/$JOB_ID/pems/$USERNAME"
          },
          "parent": {
            "href": "https://agave.iplantc.org/jobs/v2/$JOB_ID"
          },
          "profile": {
            "href": "https://agave.iplantc.org/profiles/v2/$USERNAME"
          }
        }
        }
|





.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **Unable to authenticate to your system with default credential**

     .. code-block:: plaintext

        # General grant
        curl -sk -H "Authorization: Bearer $ACCESS_TOKEN" \
            -H "Content-Type: application/json" \
            -X POST --data-binary '{"permission":"READ","username":"$USERNAME"}' \
            https://agave.iplantc.org/jobs/v2/$JOB_ID/pems

        # Custom url grant
        curl -sk -H "Authorization: Bearer $ACCESS_TOKEN" \
            -H "Content-Type: application/json" \
            -X POST --data-binary '{"permission":"READ"}' \
            https://agave.iplantc.org/jobs/v2/$JOB_ID/pems/$USERNAME
|

.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **I’m trying to import a package on JupyterHub but it says it can’t be found**

     .. code-block:: plaintext

        {
        "username": "$USERNAME",
        "internalUsername": null,
        "permission": {
          "read": true,
          "write": false
        },
        "_links": {
          "self": {
            "href": "https://agave.iplantc.org/jobs/v2/$JOB_ID/pems/$USERNAME"
          },
          "parent": {
            "href": "https://agave.iplantc.org/jobs/v2/$JOB_ID"
          },
          "profile": {
            "href": "https://agave.iplantc.org/profiles/v2/$USERNAME"
          }
        }
        }
|

