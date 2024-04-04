---
title: /feedback
position_number: 5.1
type: get
description:
parameters:
  - name: number
    content: The feedback number to retrieve
content_markdown: |-
  Retrieves an feedback by its number

  200 Returns the feedback
  {: .success}

  #### Error codes
  - 404: Not found
left_code_blocks:
  - code_block: |-
      curl \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/feedback/1
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
                  "message": "Could not find the specified feedback",
                  "status": 404,
                  "code": "FEEDBACK_NOT_FOUND"
              }
          ]
      }
    title: Error
    language: json
---
