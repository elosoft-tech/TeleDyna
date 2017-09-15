# TeleDyna
Dynatrace AppMon Plugin

[![N|Solid](http://www.elosoft.com.br/pt_br/img/elosoft-logo.png)](https://nodesource.com/products/nsolid)

## Introduction

Based on the SlackChat plugin, TeleDyna was created, a plugin to integrate the incidents of Dynatrace AppMon with Telegram. Find further information in the Dynatrace community.

Special Thanks:

> https://github.com/fabianonline/telegram.sh
>
> https://github.com/Dynatrace/Dynatrace-AppMon-Slack-Integration-Plugin 

## Plugin Details

| Plugin | README |
| ------ | ------ |
| Plug-In Files | dynaTrace 7: TeleDyna 0.0.1 |
| Author | Lewandowski Albuquerque (fernando@elosoft.com.br) |
| DynaTrace AppMon Versions | 7.x |
| License | dynaTrace BSD |
| Support | Not Supported |
| Known Problems |  |
| Dropbox | [a relative link](other_file.md) |

## Requirements

- Only bash and curl. Listing known chats with -l requires jq, but you can easily use this tool without this.
```sh
$ sudo apt-get install jq
```
- Grab the latest telegram file from this repository and put it somewhere (https://bitbucket.org/elosoft/teledyna/raw/23514411d6675f6b350012efca3560264964b257/telegram.sh).
- Give execution permission to the shell
```sh
$ chmod +x telegram.sh
```
- Create a bot at telegram:

| bot at telegram |
| ------ |
| Search for the user @botfather at telegram and start a chat with him. |
| Use the /newbot command to create a new bot. BotFather will give you a token. Keep this. |

- Use your telegram client to send a message to your new bot. Any message will do.
- Find your chat id. Run telegram.sh with -l: 
```sh
$ telegram -t <TOKEN> -l
```
If you have jq installed, it will nicely list its known chats. The number at the front is your chat id. If you don't have jq installed, it will print a bit of JSON data and tell you what to look for. These are the available chats that I can find right now. The ID is the number at the front. If there are no chats or the chat you are looking for isn't there, run this command again after sending a message to your bot via telegram.
- You now have your token and your chat id. Send yourself a first message: 
```sh
$ telegram -t <TOKEN> -c <CHAT ID> "Hello there."
```

## Installation

* Download the plugin in https://bitbucket.org/elosoft/teledyna/raw/23514411d6675f6b350012efca3560264964b257/build/br.com.elosoft.teledyna_0.0.1.jar 

Confirm plugin installation



Inform the Token, Chat ID and directory where the telegram.sh shell is located (If in doubt, see Topic 3. Requirements). In this regard, you will not need to report again.



Elect an incident to be triggered with the TeleDyna plugin





Go to the "Actions"









Choose the TeleDyna plugin. If the configuration has not been done in step 4.C, do so now, informing the Token, Chat ID and directory where the telegram.sh shell is located (If in doubt, see Topic 3. Requirements). Click "Add".








Click "OK"








Once an incident is generated and has been previously configured with a TeleDyna action, a message will be sent to the indicated chat, as shown below:

## Todos

 - Write MORE Tests
 - Proxy Support
 - Filter Options



