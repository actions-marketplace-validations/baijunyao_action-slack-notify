## Preview
![](./docs/success.png)  
![](./docs/failed.png)  

## Usage
```yaml
- name: Notify slack
  uses: baijunyao/action-slack-notify@v3.0.1
  if: always()
  with:
    slack_channel_id: your_channel_id
    slack_bot_token: ${{ secrets.SLACK_BOT_TOKEN }}
    github_context: ${{ toJson(github) }}
```

## Setup
1. [Creating a Slack App](https://api.slack.com/apps)  
![](./docs/create-slack-app.png)  
2. Add a Bot user  
![](./docs/bot-user.png) 
3. Set an icon for your bot  [Download icon](https://github.com/baijunyao/action-slack-notify/raw/master/docs/app-icons/github-action-icon.png)
![](./docs/set-an-icon.png)  
4. Install your app to your workspace
![](./docs/install-app-to-workspace.png)
5. Copy the "Bot User OAuth Access Token"  
![](./docs/bot-user-oauth-access-token.png)
6. Add the "Bot User OAuth Access Token" to GitHub secret
![](./docs/add-token-to-secret.png)
7. Get channel ID
![](./docs/get-channel-id.png)

## Example
- [laravel-bjyblog](https://github.com/baijunyao/laravel-bjyblog/blob/fba111e2fb497a4eb7a02bd9409a9c21f09b1adb/.github/workflows/CI.yml#L411)

## Thanks
- [pullreminders/slack-action](https://github.com/pullreminders/slack-action)
