# COMMAND EXAMPLES

## GET 

```
curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com
```

List repos available for the user
```
curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/user/repos
```

curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/users/propalparolnapervom/repos
```

List files changed in the PR
```
curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/repos/propalparolnapervom/test_dir/pulls/59/files
```

List lables on PR
```
curl -H "Authorization: token <your_token_to_the_repo>" https://api.github.com/repos/propalparolnapervom/test_dir/issues/92/labels
```



## POST 

Add label to the PR
```
curl -X POST -H "Authorization: token <your_token_to_the_repo>" -d '{"labels": ["works"]}' https://api.github.com/repos/propalparolnapervom/test_dir/issues/92/labels
```

