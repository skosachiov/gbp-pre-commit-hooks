# gbp-pre-commit-hooks

```
apt install pre-commit*

cd ~/git/<repo>

git clone -c http.extraHeader="Authorization: Bearer ..." https://github.com/skosachiov/gbp-pre-commit-hooks ~/.cache/pre-commit/gbp-pre-commit-hooks

echo ".pre-commit-config.yaml" >> .git/info/exclude

ln -s ~/.cache/pre-commit/gbp-pre-commit-hooks/.pre-commit-config.yaml .pre-commit-config.yaml

pre-commit install

```

## update

```
cd ~/.cache/pre-commit/gbp-pre-commit-hooks
git pull
cd -
```


## clean

debian/source/options (local-options)

`extend-diff-ignore = ^.pre-commit-config.yaml`