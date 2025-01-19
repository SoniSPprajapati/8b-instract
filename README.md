1. Install bun from the official website
2. Install hono: `bun create hono@latest .`
3. Now start our api using `bun run dev`
4. Change the port 8787 to public (for codespaces)
5. Install echo-api to test our api (alternative to Postman)
6. Test our api using echo-api
7. Convert to post request
8. Read from post request using `await c.req.json()`
9. Generate a new token from Cloudflare and set it using `export CLOUDFLARE_API_TOKEN=token`
10. Deploy our api to Cloudflare
11. To enable AI, uncomment the following line in `wrangler.toml`:
    ```toml`
    [ai]
    binding = "AI"

````
12. Now integrate the AI into our api
```ts
c.env.AI.run("model", { settings })
````

13. Deploy and test the api

Invoke-WebRequest -Uri 'https://8b-instruct.soniprajapati.workers.dev' -Method Post -Body '{ "prompt": "what is your name" }' -ContentType 'application/json'
