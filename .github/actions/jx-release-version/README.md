## Description

https://github.com/jenkins-x-plugins/jx-release-version

## Inputs

| parameter | description | required | default |
| --- | --- | --- | --- |
| previous-version | The strategy to detect the previous version: auto, from-tag, from-file or manual | `false` | auto |
| next-version | The strategy to calculate the next version: auto, semantic, from-file, increment or manual | `false` | auto |
| output-format | The output format of the next version | `false` | {{.Major}}.{{.Minor}}.{{.Patch}} |
| tag | If enabled, a new tag will be created | `false` | false |
| tag-prefix | The prefix for the new tag - prefixed before the output | `false` | v |
| push-tag | If enabled, the new tag will be pushed to the `origin` remote | `false` | true |
| github-token | The github token used to push the tag | `false` |  |
| git-user | If you want to override the name of the author/committer of the tag | `false` | Actions Bot |
| git-email | If you want to override the email of the author/committer of the tag | `false` | no-reply@no-reply.users.github.com |


## Outputs

| parameter | description |
| --- | --- |
| version | The next release version |


## Runs

This action is a `docker` action.


