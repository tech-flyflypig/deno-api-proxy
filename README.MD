# Deno API代理
# Deno API Proxy

# [English Version](README_EN.MD)

### 作者：技术爬爬虾
B站，YouTube，抖音，公众号 全网同名。转载请注明作者。

## 项目简介
使用Deno将Open AI, Claude, Groq等 API代理到国内，打破地域限制。

## Deno部署（推荐）

1. 登录/注册 [https://dash.deno.com/](https://dash.deno.com/account/projects)
2. 点击右上角的New Playground
3. 把main.ts里面所有代码复制进去
4. 点击 Save & Deploy 
5. 查看部署后的服务的域名（长这样：xxx.deno.dev）
6. 将域名，需要代理的服务名字，API Key填入下方命令中

```代理 OepnAI
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


```代理Groq
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