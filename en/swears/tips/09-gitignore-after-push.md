---
tags: tip
title: Oh shit, I committed files that I meant to add to my .gitignore!
id: gitignore-after-push
order: 9
---

```git
# make sure everything is committed
git commit -a
# update your .gitignore 
# check git status to find the files/directories you need to add
vi .gitignore
# remove everything from source control
# do NOT forget the --cached flag
# you can do --dry-run first to test things out
git rm -r --cached .
# re-add everything to git, then commit
git add .
git commit -m ".gitignore fix"
# push if you also messed up remote
git push origin BRANCH
```

I'll be honest, I have no idea why IDEs seem to add files at random. But it hasn't stopped me from doing `git commit -a` on the regular and committing a bunch of cache files nobody needs to see! 