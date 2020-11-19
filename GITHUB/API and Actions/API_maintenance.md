# COMMAND EXAMPLES

## GET 

```
curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com
```

List repos available for the user
```
curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/user/repos


curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/users/propalparolnapervom/repos
```

List files changed in the PR
```
curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/repos/propalparolnapervom/test_dir/pulls/59/files
```

List labeles on PR
```
curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/repos/propalparolnapervom/test_dir/issues/92/labels
```

List releases (only published ones are shown **!!!** ) for the repo:
```
curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/repos/propalparolnapervom/test_dir/releases
```

List API calls rate limit:
```
# https://docs.github.com/en/free-pro-team@latest/rest/reference/rate-limit
curl -H "Authorization: token <your_token>" https://api.github.com/rate_limit
```

## POST 

Add label to the PR
```
curl -X POST -H "Authorization: token <your_token_to_the_repo>" -d '{"labels": ["works"]}' https://api.github.com/repos/propalparolnapervom/test_dir/issues/92/labels
```

Add Check with `success` status to the PR
```
curl -X POST -H "Authorization: token <your_token_to_the_repo>" -d '{"context": "checkname", "state": "success", "description": "Manually added status check"}' https://api.github.com/repos/propalparolnapervom/test_dir/statuses/<sha of commit>
```

## DELETE

Delete `br4` branch
```
    # Overall reference:
    #   DELETE /repos/:owner/:repo/git/refs/:ref
    # Branch - specific version of references
    
curl -X DELETE -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/repos/propalparolnapervom/test_dir/git/refs/heads/br4
```
