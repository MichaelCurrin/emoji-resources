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

Example output:

```
* a15457b Update development.md
* 00e49b0 Create development.md
* a400c64 ✨ feat: Update link layout
* bb96ef5 (🔖 tag: v0.2.0) ✨ feat: Add to homepage
* 715c4bd 📝 docs: Add to README.md
* 3670bfb ✨ feat: Change theme to dark
* 9720c96 🎉 Initial commit
```


## Aliases

Add to git config under aliases.

```
lol = log --graph --decorate --oneline
```

```sh
emoji = ! git lol | sed 's/docs:/📝 docs:/g
...'
```


## Commit message style


You must use the convention for this to work.

e.g.

```sh
git commit -m 'docs: Update README.md'
```

This does not change how commits are stored.
