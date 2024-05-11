### Port Forwarding
Applied with [Ngrok](https://ngrok.com/).

1. Signup \ Login to the Ngrok site and fetch the auth token and static domain

2. Run this docker run command with the information from Ngrok site:
```
docker run -d -it -e NGROK_AUTHTOKEN=<auth-token> --network host --restart always --name ngrok_port_forward ngrok/ngrok:latest http --domain=<static-domain> 8000
```