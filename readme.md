# dump workflow inputs

This action dumps the branch/tag, commit hash and workflow inputs to the log.

# Usage

```yaml
- uses: freenet-actions/dump-workflow-inputs@HEAD
  with:
    inputs: ${{ toJSON(github.event.inputs) }}
    write-summary: 'true'
```

## Inputs
### inputs
The json representation of the workflow inputs. There is no other way to access this information from within an action, so you need to pass it.
### write-summary
Also write the inputs to the job summary (see https://github.blog/2022-05-09-supercharging-github-actions-with-job-summaries/).

## Development

For GitHub actions, all dependencies need to be included in the repository. Therefore, node_modules is not .gitignored.
