---
title: /workitem
position_number: 1.1
type: get
description: Create Work Item
parameters:
  - name: spaceKey
    content: The key for the space of the work item
  - name: workItemNumber
    content: The work item number
content_markdown: |-
  Retrieves a work item specified by the space key and work item number

  200 Returns the work item
  {: .success}

  #### Error codes
  - 404: Not found
left_code_blocks:
  - code_block: |-
      curl \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/workitem?spaceKey=KM&workItemNumber=123
    title: Example
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "id": "136975ca1bb5d800",
        "actor": {
          "id": "1335a51729286400",
          "name": "Zapier integration",
          "type": "application"
        },
        "number": 123,
        "title": "My Title",
        "description": "Description",
        "status": {
          "id": "1335a4d06b286401",
          "name": "Done"
        },
        "space": {
          "id": "1335a4d05e286400",
          "name": "Acme"
        },
        "labels": [
          {
            "id": "1369315bce079800",
            "name": "important",
            "color": "e91e63"
          }
        ],
        "effort": "Large",
        "impact": "Medium",
        "createdAt": "2021-11-25T14:46:18.756Z",
        "updatedAt": "2021-11-25T14:46:18.756Z"
      }
    title: Response
    language: json
  - code_block: |-
      {
          "errors": [
              {
                  "message": "Could not find the specified work item",
                  "status": 404,
                  "code": "ISSUE_NOT_FOUND"
              }
          ]
      }
    title: Error
    language: json
---
