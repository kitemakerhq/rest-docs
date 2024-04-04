---
title: /feedback
position_number: 5.2
type: post
description:
parameters:
  - name: title
    content: The title of the feedback
  - name: personEmail
    content: (Optional) The email of the person which this feedback is from
  - name: contents
    contents: (Optional) The contents of the feedback. Markdown supported
  - name: linkInsightToEntityIds[]
    content: (Optional) Creates insight from this feedback, linking it to a work item
content_markdown: |-
  Create a new feedback

  201 Returns the feedback
  {: .success}

  #### Error codes
  - 404: Not found
left_code_blocks:
  - code_block: |-
      curl \
        -X POST \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/feedback \
        -d '{"title":"This is my title"}'
    title: Example
    language: bash
right_code_blocks:
  - code_block: |-
      {
        "id": "24ba740439d5a000",
        "organizationId": "246388c6f3c4f400",
        "title": "Creating feedback from REST",
        "person": null,
        "company": null,
        "contents": "Hello there\n",
        "insights": [
            {
                "id": "24ba74042fd5a000",
                "feedbackId": "24ba740439d5a000",
                "createdAt": "2024-04-04T09:01:01.127Z",
                "updatedAt": "2024-04-04T09:01:01.127Z",
                "actor": {
                    "id": "246388c72bc4f400",
                    "name": "@Ole",
                    "type": "user"
                },
                "contents": "Hello there\n",
                "entityIds": [
                    "246da190d867d400"
                ]
            }
        ],
        "processed": false,
        "processedAt": null,
        "createdAt": "2024-04-04T09:01:01.088Z",
        "updatedAt": "2024-04-04T09:01:01.088Z"
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
