# Git log emoji

When viewing git log in the command-line, read any semantic commit "leaders" (prefixes) and prepend an emoji. 


## Command

```sh
git lol | sed 's/docs:/📝 docs:/g
s/feat:/✨ feat:/g
s/chore:/🔧 chore:/g
s/tag:/🔖 tag:/g
s/fix:/🐛 fix:/g
s/Initial commit$/🎉 Initial commit/g'
```

You must use the convention for this to work.

e.g.

```sh
git commit -m 'docs: Update README.md'
```

This does not change how commits are stored.


## Aliases

```
lol = log --graph --decorate --oneline
```

```sh
git emoji = ! git lol | sed 's/docs:/📝 docs:/g'
```
