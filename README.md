# git-note
Just noted some approaches.

### Reset author information for all commits

for all branch

```command
git filter-branch -f --env-filter '
    GIT_AUTHOR_NAME='ShihTingJustin'
    GIT_AUTHOR_EMAIL='justinhuang777@gmail.com'
    GIT_COMMITTER_NAME='ShihTingJustin'
    GIT_COMMITTER_EMAIL='justinhuang777@gmail.com'
' -- --all
```

you could also use `HEAD`
```command
git filter-branch -f --env-filter '
    GIT_AUTHOR_NAME='ShihTingJustin'
    GIT_AUTHOR_EMAIL='justinhuang777@gmail.com'
    GIT_COMMITTER_NAME='ShihTingJustin'
    GIT_COMMITTER_EMAIL='justinhuang777@gmail.com'
' HEAD
```

src: https://git-scm.com/docs/git-filter-branch

