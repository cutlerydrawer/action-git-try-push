# Git try push GitHub Action

An action that tries to make a `git push`. If it does not succeed, then wait some time, perform `git pull --rebase` and try again.
The number of maximum tries is controllable via `tries` input.

## Usage

```yaml
- name: Try pushing
  uses: cutlerydrawer/action-git-try-push@v2
  with:
    # Optional, used for pushing
    token: ${{github.token}}
    # Optional, defaults to current directory
    directory: path/to/repo
    # Optional, defaults to:
    remote: origin
    # Optional, defaults to:
    branch: master
    # Optional, defaults to:
    tries: 20
```
