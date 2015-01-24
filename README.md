rundeck-slack-incoming-webhook-plugin
======================

Sends rundeck notification messages to a slack channel.  This plugin  is based on [rundeck-slack-plugin](https://github.com/bitplaces/rundeck-slack-plugin)(based on run-hipchat-plugin).

Installation Instructions
-------------------------

See the [Included Plugins | Rundeck Documentation](http://rundeck.org/docs/plugins-user-guide/installing.html#included-plugins "Included Plugins") for more information on installing rundeck plugins.

## Download jarfile

1. Download jarfile from [releases](https://github.com/higanworks/rundeck-slack-incoming-webhook-plugin/releases).
2. copy jarfile to `$RDECK_BASE/libext`

## Build

1. build the source by gradle.
2. copy jarfile to `$RDECK_BASE/libext`


## Configuration
This plugin uses Slack incoming-webhooks.
Create a new webhook and webhook_url is set in project.properties file for your project.

```
framework.plugin.Notification.SlackNotification.webhook_url = https://hooks.slack.com/services/T00000000/B00000000/E00000000000000000000000
```

![configuration](config.png)

The only required configuration settings are:

- `WebHook URL`: Slack incoming-webhook URL. (in project.properties)
- `Channel`: Notification #channel (Default: in slack settings)

## Slack message example.

On success.

![on success](on_success.png)

On failure.

![on failure](on_failure.png)

## Contributors
*  Original [hbakkum/rundeck-hipchat-plugin](https://github.com/hbakkum/rundeck-hipchat-plugin) author: Hayden Bakkum @hbakkum
*  Original [bitplaces/rundeck-slack-plugin](https://github.com/bitplaces/rundeck-slack-plugin) authors
    *  @totallyunknown
    *  @notandy
    *  @lusis
*  @sawanoboly