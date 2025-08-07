# gbp-pre-commit-hooks

```
apt install pre-commit*

cd ~/git/<repo>
```

copy-paste into terminal:

```
git clone -c http.extraHeader="Authorization: Bearer ..." https://github.com/skosachiov/gbp-pre-commit-hooks ~/.cache/pre-commit/gbp-pre-commit-hooks

grep -qxF ".pre-commit-config.yaml" .git/info/exclude || echo ".pre-commit-config.yaml" >> .git/info/exclude

ln -s ~/.cache/pre-commit/gbp-pre-commit-hooks/.pre-commit-config.yaml .pre-commit-config.yaml

pre-commit install

```

## run

git commit -am "msg"

## skip

git commit -am "msg" --no-verify

## update

```
cd ~/.cache/pre-commit/gbp-pre-commit-hooks
git pull
cd -
```

## clean

debian/source/options (local-options)

`extend-diff-ignore = ^.pre-commit-config.yaml`
