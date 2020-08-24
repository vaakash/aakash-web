---
title: Getting started
menu_order: 1
taxonomy:
    doc_category: wordpress-plugins
---

Using "Git it write" WordPress plugin, you can publish markdown present in a Github repository.

## The Github repository

Since posts are published from a Github repository, you should have a public Github repository. Please check [github docs](https://docs.github.com/en/github/getting-started-with-github/create-a-repo) on how to create a Github repository if you are new to it.

## Adding the repository to the plugin

Once you have a Github repository (or if you wish to pull from another public repository) you can configure Git it write plugin on the same. Your repository will have an owner and the name of the repository itself. This information is used to configure in the plugin settings page.

It does not matter if your repository is new, empty, old with files already. Below configuration can be done anytime.

1. Install and activate the plugin from WordPress -> Add new
1. Go to Settings -> Git it write
1. Click "Add a new repository to publish posts from"
1. In the add repository page, enter the repository owner and the name.
1. Enter the path of the folder in the repository you would like to publish in your website.
1. Select a post type to which posts have to be published. A hierarchial post type is preferred as it allows parent, child posts in a tree like structure provided custom permalinks are configured in your site. Read [FAQ](./faq.md) for more information on this.
1. Save the settings.

## The webhook

Github Webhook allows to notify the plugin whenever the files in the repository are modified. This allows the plugin to fetch the latest changes automatically and publish/update the posts automatically without any manual need to pull posts.

If you do not own the repository then you cannot configure webhooks. Also if you do not wish to automatically update posts, then you can skip configuring the webhook.

1. Go to Settings -> Git it write settings page.
1. Under "General settings" enter a secret key which will be used by all the Github repositories you configure.
1. Go to Github repository settings -> Webhook and add a webhook for the payload URL as mentioned in the settings page.
1. Enter the same secret key in Github webhook settings page.
1. Set the remaining webhook settings accordingly as mentioned.
1. Save the settings.

Webhook is now configured. So whenever repository changes, the payload URL will be notified and the plugin will take care of adding/updating the posts.

## Writing in markdown

Markdown is a simple markup language which allows to easily write formatted text. Please refer [markdown guide](https://www.markdownguide.org/getting-started/) for more information on the syntax. Markdown files end with `.md` file extension.

You can now organize the files in folders as you need and write your posts using markdown format.

See [writing posts](./writing-posts.md) page for more information on this.

## Publishing the posts

### When webhook is configured

Whenever you commit and push the changes or pull changes to the repository the Github will notify the plugin and the plugin will automatically publish the posts by reading the markdown files from the repository as HTML post content.

### When webhook is not configured or manually publishing

In Git it write settings page every repository has option to manually pull the posts to publish. The "Pull posts" link can be seen under the repository name in the table when the row is hovered over.

There are two types of pull:

1. Pull only changes - This will pull only the changes made to the repository.
2. Pull all the files - This will pull all the files and overwrite all the posts. This is needed if you have changed the "content template" in the repository settings.

## Viewing logs

When posts are published by the plugin, all the file-by-file activities are logged. The logs can be seen using the "Logs" link in the settings page. This is helpful to debug and get to know when posts are published.