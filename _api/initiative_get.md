---
title: /initiative
position_number: 4.1
type: get
description:
parameters:
  - name: number
    content: The initiative number to retrieve
content_markdown: |-
  Retrieves an initiative by its number

  200 Returns the initative
  {: .success}

  #### Error codes
  - 404: Not found
left_code_blocks:
  - code_block: |-
      curl \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/initiative?number=1
    title: Example
    language: bash
right_code_blocks:
  - code_block: |-
      [
        {
            "id": "2463901f2d8d2000",
            "number": 1,
            "title": "Hey there",
            "description": "Hello /snippet \n\n",
            "actor": {
                "id": "246388c72bc4f400",
                "name": "@Ole",
                "type": "user"
            },
            "spaces": [
                {
                    "id": "24638e578e8d2000",
                    "name": "Acme"
                }
            ],
            "labels": [
                {
                    "id": "2463903e968d2000",
                    "name": "Omg",
                    "color": "brown"
                }
            ],
            "effort": null,
            "impact": null,
            "archivedAt": null,
            "updatedAt": "2024-03-19T11:19:26.923Z",
            "createdAt": "2024-03-18T12:04:45.329Z"
        }
      ]
    title: Response
    language: json
  - code_block: |-
      {
          "errors": [
              {
                  "message": "Could not find the specified initiative",
                  "status": 404,
                  "code": "INITIATIVE_NOT_FOUND"
              }
          ]
      }
    title: Error
    language: json
---
