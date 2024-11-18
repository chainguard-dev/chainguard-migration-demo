# Create an Assumed Identity

This allows chainctl to authenticate using the Ambient OIDC credentials of a specific repository. Just for demo purposes this example command will work all GitHub Workflows with "-demo" in the name under the chainguard-dev organization:

## Usage

```bash
chainctl iam identities create github-identity-demo \
    --identity-issuer="https://token.actions.githubusercontent.com" \
    --subject-pattern="repo:chainguard-dev/.*-demo.*:(ref:refs/heads/main|pull_request)" \
    --role=registry.pull \
    --parent=cgr-demo.com
```
