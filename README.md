# Bark
**Bark** is a Bash script that allows you to send push notifications to various platforms such as Telegram, Bark, WeCom, Feishu, and Discord.    
<img width="777" alt="Screenshot 2023-08-11 at 17 48 19" src="https://github.com/likaci/bark/assets/3407980/8077243f-79a0-477d-8b79-68f89e60a4db">


## Usage
### bark
`bark title msg channel(b|t|w|f|d)` send "title msg" to channel.   

- `title` (optional): The title of the notification. The default title is hostname.
- `msg` (optional): The content of the notification. The default content is current dir.
- `channel` (optional): The default channel is Telegram. Others:
  - `b` for Bark
  - `t` for Telegram
  - `w` for WeChat/WeCom
  - `f` for Feishu/Lark
  - `d` for Discord

 ### barkrun
`barkrun xxxx`
run `xxx` command, save out to run.log, notify if command run failed.

## Example
`bark`   
Send Hostname dir to telegram (default channel)

To send a notification with a custom title "hello" and message "test" to multiple channels, you can use the following command:   
`bark hello test btwfd`

To send a notification after a long long time make:   
`make -j9; bark`

## Notification Channel Setup

### Bark
1. Install the Bark app on your iOS device.
2. Replace `BARK_TOKEN` in script.

### Telegram
1. Create a Telegram Bot by the [official guide](https://core.telegram.org/bots#botfather), Obtain the bot `token`.
2. Start chat with your bot, run `curl "https://api.telegram.org/botBOT_TOKEN/getUpdates"` get your `chat_id`.
3. Replace `TG_TOKEN` `TG_CHAT_ID`.

### Discord
* Get Webhook by [official guide](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks)

### WeCom
* Refer [here](http://lyallchan.github.io/2016/03/25/%E5%91%BD%E4%BB%A4%E8%A1%8C%E5%8F%91%E9%80%81%E6%B6%88%E6%81%AF%E5%88%B0%E5%BE%AE%E4%BF%A1%E4%BC%81%E4%B8%9A%E5%8F%B7/)

### Feishu
* See [official guide](https://open.feishu.cn/document/client-docs/bot-v3/add-custom-bot)
