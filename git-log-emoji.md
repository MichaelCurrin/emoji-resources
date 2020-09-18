# Git log emoji
> Prettify a semantic commit git log with emojis

When viewing git log in the command-line, this will read any semantic commit "leaders" (prefixes) and prepend an emoji.
Even if you didn't use emojis originally, you get them how and you don't actually edit any commits by running this. 


## Commit message style

You must use the semvar convention for this to work.

e.g.

```sh
git commit -m 'docs: Update README.md'
git commit -m 'fix: Move variable'
```

## Command

Here is one long multi-line command you can run. It is not complete for all cases but you get the idea.

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


## Alias

Add to git config under alias.

```toml
  lol = "log --graph --decorate --oneline"
```

Add the emoji command.

```toml
  emoji = "! git lol | sed 's/docs:/📝 docs:/g ; s/feat:/✨ feat:/g ; s/chore:/🔧 chore:/g ; s/tag:/🔖 tag:/g ; s/fix:/🐛 fix:/g ; s/Initial commit$/🎉 Initial commit/g'"
```

Now use it.

```sh
git emoji
# Emoji log output appears...
```
