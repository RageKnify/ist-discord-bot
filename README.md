# IST Discord Bot

Discord bot to manage the IST Hub server -- join [here](https://discord.leic.pt).

### Running

1. Create a `docker-compose.yml` file as below:

```yaml
version: "3.8"

services:
    ist-discord-bot:
        image: ist-bot-team/ist-discord-bot:v2.0.0
        volumes:
            - type: bind
              source: ./data
              target: /app/data
        environment:
            DISCORD_TOKEN: PLACE_BOT_TOKEN_HERE
        restart: unless-stopped
```

2. Run `docker-compose up -d --build`
3. That's it!

_You can also use `docker-compose down`, `docker-compose up`, `docker-compose restart` and `docker-compose logs`._

### Adding to a Server

Replacing `CLIENT_ID` with the application's public ID, access the following link:

```
https://discord.com/oauth2/authorize?client_id=CLIENT_ID&scope=bot+applications.commands&permissions=8
```
