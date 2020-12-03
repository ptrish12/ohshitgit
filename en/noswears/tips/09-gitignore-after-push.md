---
tags: tip
title: Oh shit, I pushed files to remote that I meant to add to my .gitignore!
id: gitignore-after-push
order: 9
---

```git
# don't do this to the wrong branch by accident
git checkout BRANCH
# commit everything
git commit -a
# make sure your .gitignore is up-to-date with all those pesky .idea files and __pycache__ directories
vi .gitignore
# remove everything from source control. 
# do NOT forget the --cached flag, or you will remove the files themselves.
# you can do --dry-run first to test things out.
git rm -r --cached .
# re-add everything to git, then commit
# it will skip the things you just added to your .gitignore
git add .
git commit -m ".gitignore fix"
# if you also messed up remote
git push origin BRANCH
```

I'll be honest, I have no idea why IDEs seem to add files at random. But it hasn't stopped me from doing `git commit -a` on the regularly and committing a bunch of cache files nobody needs to see! 