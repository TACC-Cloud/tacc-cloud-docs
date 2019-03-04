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

