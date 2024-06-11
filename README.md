# Wecom Bot Notify

`wecom-bot-notify` is a simple tool to send notifications to Wecom Bot by web hook.

## Usage

```yaml
name: 'Notify'
on:
  push:
    branches:
      - main

jobs:
  notify:
    runs-on: ubuntu-latest
    steps:
      - uses: amazing-actions/wecom-bot-notify@v1.0.0
        with:
          type: markdown # text, markdown, image, news, template_card
          content: '## Test' # see https://developer.work.weixin.qq.com/document/path/91770
          key: ${{ secrets.WECOM_BOT_KEY }} # Your key of wecom bot hook
```