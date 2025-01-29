# Deno API Proxy

# [中文版本](README.MD)

### Author: Tech PaPaXia
Find me on Bilibili, YouTube, TikTok, and WeChat Official Account under the same name. Please credit the author when sharing.

## Project Overview
Use Deno to proxy Open AI, Claude, Groq and other APIs to mainland China, breaking geographical restrictions.

## Deno Deployment (Recommended)

1. Login/Register at [https://dash.deno.com/account/projects](https://dash.deno.com/account/projects)
2. Click "New Playground" in the top right corner
3. Copy all code from main.ts into the playground
4. Click "Save & Deploy"
5. Check the deployed service domain name (looks like: xxx.deno.dev)
6. Fill in your domain name, service name to proxy, and API Key in the commands below

<b>Proxy OpenAI</b>
```
curl --location 'https://YOUR-DOMAIN/api.openai.com/v1/chat/completions' \
--header 'Authorization: Bearer YOUR-API-KEY' \
--header 'Content-Type: application/json' \

--data '{
    "messages": [
        {
            "role": "system",
            "content": "You are a test assistant."
        },
        {
            "role": "user",
            "content": "Testing. Just say hi and nothing else."
        }
    ],
    "model": "gemini-2.0-flash-exp"
}'
```

<b>Proxy Groq</b>
```
curl --location 'https://YOUR-DOMAIN/api.groq.com/v1/chat/completions' \
--header 'Authorization: Bearer YOUR-API-KEY' \
--header 'Content-Type: application/json' \

--data '{
    "messages": [
        {
            "role": "system",
            "content": "You are a test assistant."
        },
        {
            "role": "user",
            "content": "Testing. Just say hi and nothing else."
        }
    ],
    "model": "gemini-2.0-flash-exp"
}'
``` 