---
title: /labels
position_number: 5.4
type: get
description: List all labels for a space
parameters:
  - name: spaceId
    content: The space ID to query

content_markdown: |-
  Retrieves a list of labels for a space. This endpoint is primarily used by the Zapier integration

  200 Returns the list of labels for the space
  {: .success}

  #### Error codes
  - 404: Not found (space was not found)
left_code_blocks:
  - code_block: |-
      curl \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/metadata/labels?spaceId=0a3abd6aeb71f400
    title: Example
    language: bash
right_code_blocks:
  - code_block: |-
      [
        {
            "id": "0a31bd6aeb71f400",
            "label": "Main board"
        },
        {
            "id": "0f63e8cabd046800",
            "label": "User testing"
        }
      ]
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
