# gbp-pre-commit-hooks

```
cd ~/git/<repo>

git clone -c http.extraHeader='Authorization: Bearer ..." https://github.com/skosachiov/gbp-pre-commit-hooks ~/.cache/pre-commit/gbp-pre-commit-hooks

echo ".pre-commit-config.yaml" >> .git/info/exclude

ln -s ~/.cache/pre-commit/gbp-pre-commit-hooks/.pre-commit-config.yaml .pre-commit-config.yaml

pre-commit install

```

## clean

debian/source/options (local-options)

`extend-diff-ignore = ^.pre-commit-config.yaml`