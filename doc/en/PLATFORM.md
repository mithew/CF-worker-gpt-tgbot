# Supported platforms

### 1. [Cloudflare Workers](https://workers.cloudflare.com/)

The easiest way, the deployment method supported by this project by default, see [Deployment Process](DEPLOY.md) for details. Free, no domain, no server, no need to configure local development environment. kv storage, no database, but there are some storage limitations.

> KV write limit is 1000 times per day, but it should be enough for chatbot. (Debug mode `DEBUG_MODE` will save the latest message to KV, token stats will update the stats every time the conversation is successful, so there will be a certain number of writes. If you regularly use it more than 1000 times, consider turning off debug mode and token usage statistics)

### 2. [Vercel](https://vercel.com/)

See details at [Vercel](../../adapter/vercel). It is free, does not require a domain name or server. Deployment requires configuring the local development environment and cannot be done by copying and pasting. There is no storage service, so you need to configure your own database. You can use the free Redis from [Redis Cloud](https://redis.com). It can connect to GitHub for automatic deployment, but you need to understand Vercel's configuration.


### 3. [Render](https://render.com/)

See [Render](../../adapter/render) for details.. Free, no domain name, no server required. Some development skills are required.

### 4. Local

See [Local](../../adapter/local) for details. For local deployment method, you need to configure local development environment.