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

List releases for the repo:
```
curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/repos/propalparolnapervom/test_dir/releases
```


## POST 

Add label to the PR
```
curl -X POST -H "Authorization: token <your_token_to_the_repo>" -d '{"labels": ["works"]}' https://api.github.com/repos/propalparolnapervom/test_dir/issues/92/labels
```

## DELETE

Delete `br4` branch
```
    # Overall reference:
    #   DELETE /repos/:owner/:repo/git/refs/:ref
    # Branch - specific version of references
    
curl -X DELETE -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/repos/propalparolnapervom/test_dir/git/refs/heads/br4
```
