## Description

Generate Helm docs

## Inputs

| parameter | description | required | default |
| --- | --- | --- | --- |
| path | set custom chart path | `false` | ./ |
| git-token | the git token used to operate on the git repository. If not specified it's loaded from the git credentials file | `true` |  |
| version | set version | `false` |  |
| git-username | the git username used to operate on the git repository. If not specified it's loaded from the git credentials file | `false` | Actions Bot |
| git-author-name | the user name to git commit | `false` |  |
| git-author-email | the user email to git commit | `false` | no-reply@no-reply.users.github.com |


## Runs

This action is a `composite` action.


