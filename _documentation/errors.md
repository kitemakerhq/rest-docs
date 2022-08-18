---
title: Errors
position_number: 3
parameters:
  - name:
    content:
content_markdown: |-
  | Code | Name | Description |
  | --- | --- | --- |
  | 200 | OK | Success |
  | 201 | Created | Creation Successful |
  | 401 | Unauthorized | We couldn't authenticate you |

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
