# gbp-pre-commit-hooks or gbp-pre-push-hooks

Initially, the `pre-commit` hook was used, but later, in order not to interfere with the developer, the checks were moved to the `pre-push` hook.

## install deps

```
apt install pre-commit*

cd ~/git/<repo>
```

## copy-paste into terminal


```
git clone https://github.com/skosachiov/gbp-pre-commit-hooks ~/.cache/pre-commit/gbp-pre-commit-hooks

grep -qxF ".pre-commit-config.yaml" .git/info/exclude || echo ".pre-commit-config.yaml" >> .git/info/exclude

ln -s ~/.cache/pre-commit/gbp-pre-commit-hooks/.pre-commit-config.yaml debian/.pre-commit-config.yaml

cp ~/.cache/pre-commit/gbp-pre-commit-hooks/assets/pre-push .git/hooks/

chmod 775 .git/hooks/pre-push

```


```
git clone -c http.extraHeader="Authorization: Bearer ..." https://github.com/skosachiov/gbp-pre-commit-hooks ~/.cache/pre-commit/gbp-pre-commit-hooks
```

## run

git push

## skip

git push --no-verify

## update

```
cd ~/.cache/pre-commit/gbp-pre-commit-hooks
git pull
cd -
```

## clean

debian/source/options (local-options)

`extend-diff-ignore = ^.pre-commit-config.yaml`
