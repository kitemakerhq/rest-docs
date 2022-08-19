---
title: /comments
position_number: 4.2
type: get
description: Get recently updated comments
parameters:
  - name: spaceId
    content: The space ID to retrieve comments from
  - name: count
    content: The number of comments to retrieve (max 50)
content_markdown: |-
  Retrieves recenty updated comments

  200 Returns a list of recently updated comments
  {: .success}

  #### Error codes
  - 404: Not found (space was not found)
left_code_blocks:
  - code_block: |-
      curl \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/recent/comments?spaceId=0a3abd6aeb71f400&count=10
    title: Example
    language: bash
right_code_blocks:
  - code_block: |-
      [
        {
          "id": "1369791039b5d801",
          "body": "Hey there!",
          "actor": {
            "id": "1335a51729286400",
            "name": "Zapier integration",
            "type": "application"
          },
          "entity": {
            "id": "136975ca1bb5d800",
            "number": 18,
            "space": "ACM",
            "spaceId": "136975ca1bb5d800",
            "title": "My Title"
          },
          "reply": false,
          "threadId": "1369791039b5d800",
          "createdAt": "2021-11-25T14:49:53.313Z",
          "updatedAt": "2021-11-25T14:49:53.313Z"
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
