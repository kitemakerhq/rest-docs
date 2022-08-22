---
title: /workitems
position_number: 5.2
type: get
description: List all work items for a space
parameters:
  - name: spaceId
    content: The space ID to query

content_markdown: |-
  Retrieves a list of work items for a space. This endpoint is primarily used by the Zapier integration

  200 Returns the list of work items for the space
  {: .success}

  #### Error codes
  - 404: Not found (space was not found)
left_code_blocks:
  - code_block: |-
      curl \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/metadata/workitems?spaceId=0a3abd6aeb71f400
    title: Example
    language: bash
right_code_blocks:
  - code_block: |-
      [
        {
            "id": "0bbba9fed6573800",
            "label": "Create new work items by pressing C or Shift+C"
        },
        {
            "id": "0d185aa8db871400",
            "label": "Github integration"
        },
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
