---
title: /comment
position_number: 2.1
type: post
description: Create a new comment
parameters:
  - name: workItemId
    content: The ID of the work item to comment on
  - name: body
    content: The body of the comment. Markdown supported

content_markdown: |-
  Creates a new comment on the specified work item

  201 Returns the created comment
  {: .success}

  #### Error codes
  - 404: Not found (the work item was not found)

left_code_blocks:
  - code_block: |-
      curl \
        -X POST \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/comment \
        -d '{"workItemId": "136975ca1bb5d800", "body": "Hey there!"}'
    title: Example
    language: curl
right_code_blocks:
  - code_block: |-
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
