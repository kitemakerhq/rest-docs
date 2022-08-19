---
title: /label
position_number: 3.1
type: post
description: Create a new label
parameters:
  - name: spaceId
    content: The space ID to create the label in
  - name: labelName
    content: The name of the label to create
  - name: color
    content: (Optional) The color to assign the label in hte format aa33ff. Defaults to a random color

content_markdown: |-
  Creates a new label in the specified space

  201 Returns the created label
  {: .success}

  #### Error codes
  - 404: Not found (space was not found)

left_code_blocks:
  - code_block: |-
      curl \
        -X POST \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/label \
        -d '{"spaceId":"a229cc2147a78000","labelName": "Infrastructure", "color": "ff00aa"}'
    title: Example
    language: curl
right_code_blocks:
  - code_block: |-
      {
        "id": "18c20f3a90e21400",
        "name": "Infrastructure",
        "color": "ff00aa",
        "spaceId": "a229cc2147a78000"
      }
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
