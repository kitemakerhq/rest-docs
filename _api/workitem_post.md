---
title: /workitem
position_number: 1.2
type: post
description: Create Work Item
parameters:
  - name: title
    content: The title of the work item
  - name: statusId
    content: The status ID (column) where the work item will be created
  - name: description
    content: (Optional) The description of the work item
  - name: labelIds[]
    content: (Optional) An array of label IDs to add to the work item
  - name: effort
    content: (Optional) The effort to assign to the work item. One of ['small', 'medium', 'large']
  - name: impact
    content: (Optional) The impact to assign to the work item. One of ['small', 'medium', 'large']
  - name: placement
    content: (Optional) The placement in the status column. One of ['top', 'bottom']. Defaults to 'top'

content_markdown: |-
  Creates a new work item and returns the content

  201 Returns the work item
  {: .success}

  #### Error codes
  - 404: Not found

left_code_blocks:
  - code_block: |-
      curl \
        -X POST \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/workitem \
        -d '{"title":"This is my title","statusId": "1adf8dc...", "description": "Lorem ipsum dolor sit amet"}'
    title: Example
    language: curl
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
                  "message": "The requested action could not be completed",
                  "status": 401,
                  "code": "UNAUTHORIZED"
              }
          ]
      }
    title: Error
    language: json
---
