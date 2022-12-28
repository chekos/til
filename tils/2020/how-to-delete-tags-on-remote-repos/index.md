---
categories:
- git
date: 2020-06-23
title: How To Delete Tags On Remote Repos
---

## what i learned
you can delete remote tags from your github repository using `git push --delete origin <TAG NAME>` or you can delete locally and then push those changes to your remote repo

```shell
git tag -d 0.0.7
git push origin :refs/tag/0.0.7
```


## how i learned
recently someone became the very first contributor to `pypums` and when i merged their contribution and tried to automatically build and publish the package to PyPI i found myself making an error. at first i tried to create a release on github then i realized i had not changed the versions accordingly in setup.py and the other files. i had already tagged it as 0.0.7, however, so i had to delete the tag, fix the versions, tag it again. 

i had done this before a few times but this time i found this very quick and easy explanatory post: [how to delete local and remote tags on git](https://devconnected.com/how-to-delete-local-and-remote-tags-on-git/)