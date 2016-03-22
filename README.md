# hubot-winslack

This is a fork of hobot-slack. Most likely a very short fork. Will only be maintained until hubot-slack supports slack client >= 2.0
I ran into problems building hubot-slack because of slack-clients dependency on ws 0.4.31. slack-client 1.5.1 does not cause
this problems for me.


This is a [Hubot](http://hubot.github.com/) adapter to use with [Slack](https://slack.com).


## Getting Started

#### Creating a new bot

- `npm install -g hubot coffee-script yo generator-hubot`
- `mkdir -p /path/to/hubot`
- `cd /path/to/hubot`
- `yo hubot`
- `npm install hubot-winslack --save`
- Initialize git and make your initial commit
- Check out the [hubot docs](https://github.com/github/hubot/tree/master/docs) for further guidance on how to build your bot

#### Testing your bot locally

- `HUBOT_SLACK_TOKEN=xoxb-1234-5678-91011-00e4dd ./bin/hubot --adapter winslack`


## Configuration

This adapter uses the following environment variables:

 - `HUBOT_SLACK_TOKEN` - this is the API token for the Slack user you would like to run Hubot under.

To add or remove your bot from specific channels or private groups, you can use the /kick and /invite slash commands that are built into Slack.

If you have scripts that send notifications to specific channels, use the channel name ie. `HUBOT_TWITTER_MENTION_ROOM="#general"` Keep in mind that your bot needs to be joined to your specific channels by the /invite slash command.

If you're using the [hubot-auth](https://github.com/hubot-scripts/hubot-auth/) script, you can get the user IDs required for the `HUBOT_AUTH_ADMIN` setting by calling the [users.list API method](https://api.slack.com/methods/users.list/test).

## Copyright

Copyright &copy; Slack Technologies, Inc. MIT License; see LICENSE for further details.
