---
title: Authentication
position_number: 2
parameters:
  - name:
    content:
content_markdown: |-
  You need to be authenticated for all API requests. API keys can be created from the command menu `Ctrl/Cmd + k` » Manage developer settings » Applications

  Add the `X-API-KEY` header to the request with your token.

left_code_blocks:
  - code_block:
    title:
    language:
right_code_blocks:
  - code_block: |2-
       curl \
        -H "Accept: application/json" \ 
        -H "X-API-KEY: <TOKEN>" \
        https://toil.kitemaker.co/developers/rest/v1/workitem
    title: Curl
    language: bash
---
