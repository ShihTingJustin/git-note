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
```cmd
git filter-branch -f --env-filter '
    GIT_AUTHOR_NAME='ShihTingJustin'
    GIT_AUTHOR_EMAIL='justinhuang777@gmail.com'
    GIT_COMMITTER_NAME='ShihTingJustin'
    GIT_COMMITTER_EMAIL='justinhuang777@gmail.com'
' HEAD
```
src: https://git-scm.com/docs/git-filter-branch

---

### Why are my contributions not showing up on my profile?

make sure the email setting in git config is as same as GitHub email

```cmd
git config user.email
```

or read [GitHub Doc](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/managing-contribution-graphs-on-your-profile/why-are-my-contributions-not-showing-up-on-my-profile)
