---
title: /organization
position_number: 1.0
type: get
description: Get organization information
parameters:

content_markdown: |-
  Retrieves information about the organization of which the access token is part of

  200 Returns the organization info
  {: .success}

left_code_blocks:
  - code_block: |-
      curl \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/organization
    title: Example
    language: bash
right_code_blocks:
  - code_block: |-
      {
          "id": "f221ac0765477000",
          "name": "Kitemaker",
          "createdAt": "2021-12-12T08:25:46.455Z",
          "updatedAt": "2022-07-16T09:23:19.800Z"
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
