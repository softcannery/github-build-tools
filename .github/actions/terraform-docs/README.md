## Description

A Github action for generating Terraform module documentation using terraform-docs and gomplate.

## Inputs

| parameter | description | required | default |
| --- | --- | --- | --- |
| config-file | Name of terraform-docs config file. To enable, provide the file name (e.g. `.terraform-docs.yml`) | `false` | disabled |
| working-dir | Comma separated list of directories to generate docs for (ignored if `atlantis-file` or `find-dir` is set) | `false` | . |
| atlantis-file | Name of Atlantis file to extract list of directories by parsing it. To enable, provide the file name (e.g. `atlantis.yaml`) | `false` | disabled |
| find-dir | Name of root directory to extract list of directories by running `find ./find_dir -name *.tf` (ignored if `atlantis-file` is set) | `false` | disabled |
| recursive | If true it will update submodules recursively | `false` | false |
| recursive-path | Submodules path to recursively update | `false` | modules |
| output-format | terraform-docs format to generate content (see [all formats](https://github.com/terraform-docs/terraform-docs/blob/master/docs/FORMATS_GUIDE.md)) (ignored if `config-file` is set) | `false` | markdown table |
| output-method | Method should be one of `replace`, `inject`, or `print` | `false` | inject |
| output-file | File in module directory where the docs should be placed | `false` | README.md |
| template | When provided will be used as the template if/when the `output-file` does not exist | `false` | <!-- BEGIN_TF_DOCS --> {{ .Content }} <!-- END_TF_DOCS --> |
| args | Additional arguments to pass to the command (see [full documentation](https://github.com/terraform-docs/terraform-docs/tree/master/docs)) | `false` |  |
| indention | Indention level of Markdown sections [1, 2, 3, 4, 5] | `false` | 2 |
| git-push | If true it will commit and push the changes | `false` | false |
| git-push-user-name | If empty the name of the GitHub Actions bot will be used (i.e. `github-actions[bot]`) | `false` |  |
| git-push-user-email | If empty the no-reply email of the GitHub Actions bot will be used (i.e. `github-actions[bot]@users.noreply.github.com`) | `false` |  |
| git-commit-message | Commit message | `false` | terraform-docs: automated action |
| git-push-sign-off | If true it will sign-off commit | `false` | false |
| fail-on-diff | Fail the job if there is any diff found between the generated output and existing file (ignored if `git-push` is set) | `false` | false |


## Outputs

| parameter | description |
| --- | --- |
| num_changed | Number of files changed |


## Runs

This action is a `docker` action.


