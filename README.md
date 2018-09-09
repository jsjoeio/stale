# camper-probot

> A GitHub App built with [Probot Stale](https://github.com/probot/stale) that closes abandoned Issues and Pull Requests after a period of inactivity in freeCodeCamp&#x27;s GitHub repositories.

Please visit [Probot Stale](https://github.com/probot/stale) to see the original project and documentation.

## Setup

```sh
# Install dependencies
npm install

# Run the bot
npm start
```

## Usage

1. **[Configure the GitHub App](https://github.com/apps/stale)**
2. Create `.github/stale.yml` based on the following template.
3. It will start scanning for stale issues and/or pull requests within an hour.

A `.github/stale.yml` file is required to enable the plugin. The file can be empty, or it can override any of these default settings:

```yml
# Configuration for probot-stale - https://github.com/probot/stale

# Number of days of inactivity before an Issue or Pull Request becomes stale
daysUntilStale: 60

# Number of days of inactivity before an Issue or Pull Request with the stale label is closed.
# Set to false to disable. If disabled, issues still need to be closed manually, but will remain marked as stale.
daysUntilClose: 7

# Issues or Pull Requests with these labels will never be considered stale. Set to `[]` to disable
exemptLabels:
  - pinned
  - security
  - "[Status] Maybe Later"

# Set to true to ignore issues in a project (defaults to false)
exemptProjects: false

# Set to true to ignore issues in a milestone (defaults to false)
exemptMilestones: false

# Label to use when marking as stale
staleLabel: wontfix

# Comment to post when marking as stale. Set to `false` to disable
markComment: >
  This issue has been automatically marked as stale because it has not had
  recent activity. It will be closed if no further activity occurs. Thank you
  for your contributions.

# Comment to post when removing the stale label.
# unmarkComment: >
#   Your comment here.

# Comment to post when closing a stale Issue or Pull Request.
# closeComment: >
#   Your comment here.

# Limit the number of actions per hour, from 1-30. Default is 30
limitPerRun: 30

# Limit to only `issues` or `pulls`
# only: issues

# Optionally, specify configuration settings that are specific to just 'issues' or 'pulls':
# pulls:
#   daysUntilStale: 30
#   markComment: >
#     This pull request has been automatically marked as stale because it has not had
#     recent activity. It will be closed if no further activity occurs. Thank you
#     for your contributions.

# issues:
#   exemptLabels:
#     - confirmed
```


## Deployment

See [docs/deploy.md](docs/deploy.md) if you would like to run your own instance of this plugin.

## Contribute

If you have suggestions for how camper-probot could be improved, or want to report a bug, open an issue! We'd love all and any contributions.

For more, check out the [Contributing Guide](CONTRIBUTING.md).

## License

[ISC](LICENSE) © 2018 freeCodeCamp.org <team@freecodecamp.org> (https://github.com/freeCodeCamp/camper-probot)

