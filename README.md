# docbot
[![FOSSBilling Discord](https://img.shields.io/badge/FOSSBilling-Discord-blue)](https://fossbilling.org/discord)
![GitHub go.mod Go version](https://img.shields.io/github/go-mod/go-version/evrifaessa/docbot)
![GitHub](https://img.shields.io/github/license/evrifaessa/docbot)

![Screenshot](https://user-images.githubusercontent.com/35808275/196697286-dc3a3b5b-024b-42ec-96e8-47f1490fba65.png)

A simple Discord bot that replies with the related documentation page when you call it.
It will likely mainly be used in the [FOSSBilling](https://fossbilling.org/discord) Discord server, but I'm planning to make it more extensible and customizable in the future.

Heavily inspired by the bot in Laravel's Discord server with the same name.

## How it works
* The bot is invited with minimal permissions, the permissions to read and send messages should be fine.
* The bot will then listen for messages in the channels it has access to. If a message starts with `docs`, it will reply with the full documentation URL.

## How to use
You can invite the bot using [this invite link](https://discord.com/oauth2/authorize?client_id=1032269333973442600&scope=bot&permissions=2048) (the link only has "Send messages" permissions) or build and deploy it yourself.

## How to deploy
The bot is written in [Go](https://go.dev) and uses [DiscordGo](https://github.com/bwmarrin/discordgo) to interact with the Discord API. You can build it using `go build` and run it with `./docbot`.

The bot uses the following environment variables:
* `DISCORD_TOKEN` - The bot token. You can get one from the [Discord Developer Portal](https://discord.com/developers/applications). Make sure to enable the "Message Content Intent" under the "Privileged Gateway Intents" section. You can also use the `-t` flag to pass the token instead.

## Licensing
Copyright (c) 2022, [evrifaessa](https://github.com/evrifaessa).

This project is licensed under Apache License 2.0. See the [LICENSE](LICENSE) file for more information.