.. role:: raw-html-m2r(raw)
   :format: html
   
=======
TESTING
=======




.. container:: foldable

     .. container:: header

        :fa:`caret-right`
        **Show curl**

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
        **Show json response**

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
        **Show curl**

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
        **Show json response**

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
        **Show curl**

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
        **Show json response**

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

