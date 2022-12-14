## Description

Create a Pull Request on each downstream repository
See: https://github.com/jenkins-x-plugins/jx-updatebot


## Inputs

| parameter | description | required | default |
| --- | --- | --- | --- |
| auto-merge | should we automatically merge if the PR pipeline is green (default true) | `false` | true |
| version | the version number to promote. If not specified uses $VERSION or the version file | `false` |  |
| version-file | the file to load the version from if not specified directly or via a $VERSION environment variable. Defaults to VERSION in the current dir | `false` | VERSION |
| dir | the directory look for the VERSION file (default ".") | `false` | . |
| pull-request-title | the PR title | `false` |  |
| commit-title | the commit title | `false` |  |
| commit-message | the commit message | `false` |  |
| pull-request-body | the PR body | `false` |  |
| labels | a list of labels to apply to the PR separated by comma, i.e l1,l2,l3 | `false` |  |
| base-branch-name | the base branch name to use for new pull requests. Defaults to default main branch if not specified. | `false` |  |
| flags | Command options, i.e. --git-credentials | `false` |  |
| config-file | the updatebot config file. If none specified defaults to .jx/updatebot.yaml | `false` |  |
| git-token | the git token used to operate on the git repository. If not specified it's loaded from the git credentials file | `false` |  |
| git-username | the git username used to operate on the git repository. If not specified it's loaded from the git credentials file | `false` | Actions Bot |
| git-author-name | the user name to git commit | `false` | Actions Bot |
| git-author-email | the user email to git commit | `false` | no-reply@no-reply.users.github.com |
| jx-updatebot-release | the version of jx-updatebot release | `false` | 0.3.13 |


## Runs

This action is a `composite` action.


