---
title: /workitems
position_number: 4.1
type: get
description: Get recently updated work items
parameters:
  - name: spaceId
    content: The space ID to retrieve work items from
  - name: count
    content: The number of work items to retrieve (max 50)
content_markdown: |-
  Retrieves a list of recenty updated work items

  200 Returns the list of recently updated work items
  {: .success}

  #### Error codes
  - 404: Not found (space was not found)
left_code_blocks:
  - code_block: |-
      curl \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/recent/workitems?spaceId=0a3abd6aeb71f400&count=10
    title: Example
    language: bash
right_code_blocks:
  - code_block: |-
      [
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
        },
      ]
    title: Response
    language: json
  - code_block: |-
      {
          "errors": [
              {
                  "message": "The specified space does not exist",
                  "status": 404,
                  "code": "SPACE_NOT_FOUND"
              }
          ]
      }
    title: Error
    language: json
---
