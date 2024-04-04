---
title: /initiative
position_number: 4.2
type: post
description:
parameters:
  - name: title
    content: The title of the initiative
  - name: description
    content: (Optional) The description of the initiative. Markdown supported
  - name: color
    content: (Optional) The color of the initiative
  - name: labelIds[]
    content: (Optional) An array of label IDs to add to the initiative
  - name: effortId
    content: (Optional) The effort ID to assign to the initiative
  - name: impactId
    content: (Optional) The impact ID to assign to the initiative
  - name: spaceIds
    content: (Optional) Space IDs to add to the initiative
  - name: roadmapColumnIds
    content: (Optional) Add this initiative to these roadmap columns
content_markdown: |-
  Create a new initiative

  201 Returns the initative
  {: .success}

  #### Error codes
  - 404: Not found
left_code_blocks:
  - code_block: |-
      curl \
        -X POST \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/initiative \
        -d '{"title":"This is my title", "description": "Lorem ipsum dolor sit amet"}'
    title: Example
    language: bash
right_code_blocks:
  - code_block: |-
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
