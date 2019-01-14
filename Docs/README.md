![Use GIF](https://github.com/EasyPrograms/Issue-Comment-From-Slack/raw/master/use.gif)

## Getting Started

### Prerequisite

> #### Slack

* [Creating a slack command](https://api.slack.com/tutorials/your-first-slash-command)
* [Generating Slack API Access tokens](https://get.slack.help/hc/en-us/articles/215770388-Create-and-regenerate-API-tokens)

> #### Github

* [Generating Github API Access Token](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/)

* Creating a Monitor WebHook

### Setting Up Environment Variables

* `slack-bot-token` - Your slack bot's access token
* `github-account` - Your organization/personal account name on github
* `github-account-type` - `org`/`user`
* `github-token` - Your github personal/App access token


### Setting up Webhook for the collection

[Postman Webhooks](https://learning.getpostman.com/docs/postman/monitors/integrations_for_alerts/)

* make a `POST` Request to `https://api.getpostman.com/webhooks?apikey={{API-key}}`
* Set Body to
```
{
	"webhook": {
		"name": "{{webhook-name}}",
		"collection": "{{collId}}"
	}
}
```

* Set Header `Content-Type` to `application/json`

This gives a JSON response with webhook's (that we created) information. 

Save the webhook url for later.

> ## NOTE
* Replace {{API-key}} with the postman api access key
* Replace {{webhook-name}} with the name you wan't to give to the webhook
* Replace {{collId}} with the collection's Id that needs to be executed with this webhook.
* Collection's Id can be found here
![Collection Id](https://github.com/EasyPrograms/Issue-Comment-From-Slack/raw/master/use.gif)
