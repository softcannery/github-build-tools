                                                                                    
## Description

Build Docker image and push to Github registry

## Inputs

| parameter | description | required | default |
| --- | --- | --- | --- |
| image-name | Docker image name | `true` |  |
| chart-path | set custom chart path | `false` | ./ |
| git-token | the git token used to operate on the git repository. If not specified it's loaded from the git credentials file | `true` |  |
| version | set version | `false` | snapshot |
| git-username | the git username used to operate on the git repository. If not specified it's loaded from the git credentials file | `false` | Actions Bot |
| git-author-name | the user name to git commit | `false` |  |
| git-author-email | the user email to git commit | `false` | no-reply@no-reply.users.github.com |


## Runs

This action is a `composite` action.


