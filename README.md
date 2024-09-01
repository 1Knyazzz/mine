# Minecraft Server Using Docker Compose

📙 The complete installation guide is available on my [website](https://www.heyvaldemar.com/install-minecraft-server-using-docker-compose/).

💡 For details on deploying the Minecraft Proxy, check out this link: [Minecraft Proxy Using Docker Compose](https://github.com/heyvaldemar/minecraft-server-proxy-docker-compose/).

❗ Change variables in the `.env` to meet your requirements.

💡 Note that the `.env` file and `plugins` folder should be in the same directory as `minecraft-server-docker-compose.yml`.

Create a network for your services before deploying the configuration using the command:

`docker network create minecraft-server-network`

Deploy Minecraft Server using Docker Compose:

`docker compose -f minecraft-server-docker-compose.yml -p minecraft-server up -d`

You can check the Minecraft Server status using the commands:

```
MINECRAFT_SERVER_CONTAINER=$(docker ps -aqf "name=minecraft-server-minecraft-server") \
&& docker exec -it $MINECRAFT_SERVER_CONTAINER mc-monitor status
```

# Minecraft Servers Logs

You can check logs using the commands:

```
MINECRAFT_SERVER_CONTAINER=$(docker ps -aqf "name=minecraft-server-minecraft-server") \
&& docker logs $MINECRAFT_SERVER_CONTAINER
```

# Minecraft Server Management

Apply new configuration after a change in the `minecraft-server-docker-compose.yml` or `.env` using the command:

`docker compose -f minecraft-server-docker-compose.yml -p minecraft up -d`

Connect to the Minecraft server command-line interface using the command:

```
MINECRAFT_SERVER_CONTAINER=$(docker ps -aqf "name=minecraft-server-minecraft-server") \
&& docker exec -i $MINECRAFT_SERVER_CONTAINER rcon-cli
```

# Backups

The `minecraft-server-data-backups` folder, holding all server backups, will be automatically created in the same directory as `minecraft-server-docker-compose.yml` upon the server's initial startup.

# Author

I’m Vladimir Mikhalev, the [Docker Captain](https://www.docker.com/captains/vladimir-mikhalev/), but my friends can call me Valdemar.

🌐 My [website](https://www.heyvaldemar.com/) with detailed IT guides\
🎬 Follow me on [YouTube](https://www.youtube.com/channel/UCf85kQ0u1sYTTTyKVpxrlyQ?sub_confirmation=1)\
🐦 Follow me on [Twitter](https://twitter.com/heyValdemar)\
🎨 Follow me on [Instagram](https://www.instagram.com/heyvaldemar/)\
🧵 Follow me on [Threads](https://www.threads.net/@heyvaldemar)\
🐘 Follow me on [Mastodon](https://mastodon.social/@heyvaldemar)\
🧊 Follow me on [Bluesky](https://bsky.app/profile/heyvaldemar.bsky.social)\
🎸 Follow me on [Facebook](https://www.facebook.com/heyValdemarFB/)\
🎥 Follow me on [TikTok](https://www.tiktok.com/@heyvaldemar)\
💻 Follow me on [LinkedIn](https://www.linkedin.com/in/heyvaldemar/)\
🐈 Follow me on [GitHub](https://github.com/heyvaldemar)

# Communication

👾 Chat with IT pros on [Discord](https://discord.gg/AJQGCCBcqf)\
📧 Reach me at ask@sre.gg

# Give Thanks

💎 Support on [GitHub](https://github.com/sponsors/heyValdemar)\
🏆 Support on [Patreon](https://www.patreon.com/heyValdemar)\
🥤 Support on [BuyMeaCoffee](https://www.buymeacoffee.com/heyValdemar)\
🍪 Support on [Ko-fi](https://ko-fi.com/heyValdemar)\
💖 Support on [PayPal](https://www.paypal.com/paypalme/heyValdemarCOM)
