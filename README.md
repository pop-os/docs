# POP!_OS Documentation

https://pop-os.github.io/docs


## contribute
### clone docs repo

```bash
git clone git@github.com:pop-os/docs.git docs
cd docs
```

### create a branch

```bash
git checkout -b <your-branch>
```
### make changes and push <your-branch>

```bash
git add . && git commit -m "chore: did stuff" && git push --set-upstream origin <your-branch>
in the gh ui, make a PR to master main
```

when a merge to main occurs it will automatically build and deploy to https://pop-os.github.io/docs