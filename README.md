# Auto merge SmartLing's pull requests

A GitHub Action to automatically merge pull requests from our TMS SmartLing:

*   SmartLing opens a PR
*   The test suite is passing
*   I haven't marked the PR as a WIP

## Usage
Reference the Action in your `.workflow` file:

```hcl
workflow "merge_smartling_pr_cleanup" {
  on = "pull_request"
  resolves = ["Merge SmartLing PR and Cleanup"]
}

action "Merge SmartLing PR and Cleanup" {
  uses = "JamesMarkWilton/auto_merge_my_pull_requests@development"
  secrets = ["GITHUB_TOKEN"]
}
```
## License

MIT.
