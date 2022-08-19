---
title: Errors
position_number: 3
parameters:
  - name:
    content:
content_markdown: |-
  These are the global errors which can occur. Any errors specific to the endpoint will be mentioned in that section

  | Code | Name | Description |
  | --- | --- | --- |
  | 400 | Bad request | Invalid parameters |
  | 401 | Unauthorized | We couldn't authenticate you |
  | 429 | Too many requests | Rate limit exceeded |

  All errors will return JSON in the following format:
left_code_blocks:
  - code_block: |-
      {
          "errors": [
              {
                  "message": "Could not find the specified work item",
                  "status": 404,
                  "code": "ISSUE_NOT_FOUND"
              }
          ]
      }
    title: Response
    language: json
right_code_blocks:
  - code_block:
    title:
    language:
---
