---
title: /spaces
position_number: 5.1
type: get
description: List all available spaces
parameters:

content_markdown: |-
  Retrieves a list of spaces for an organization. This endpoint is primarily used by the Zapier integration

  200 Returns the list of spaces for an organization
  {: .success}

  #### Error codes
  - 404: Not found (space was not found)
left_code_blocks:
  - code_block: |-
      curl \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/metadata/spaces
    title: Example
    language: bash
right_code_blocks:
  - code_block: |-
      [
        {
            "id": "0bbba9fed6573800",
            "label": "A new label"
        },
        {
            "id": "0d185aa8db871400",
            "label": "bug"
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
