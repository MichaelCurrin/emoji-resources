# Git log emoji
> Prettify a conventional commit git log with emojis

When viewing your git log in the command-line, this tool will read any conventional commit "leader" (prefix) keywords and prepend an emoji.

This only affects your viewing output and doesn't change the commits.

This works on any git project where you used conventional commit leaders in some or all of the commits.


## Commit message style

You must use the semvar convention for this to work.

e.g.

```sh
git commit -m 'docs: Update README.md'
git commit -m 'fix: Move variable'
```


## Run a command

For Bash or Linux, using `sed` to find and replace.

Here is a long multi-line command you can run. It is not complete for all cases but you get the idea.

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


## Setup an alias

To make is easier to use the command above any time, you can add it to your git aliases in `~/.gitconfig`.

Add to your git config under `[alias]` section.

This shows a commit message in a single line and adds a tree flow for use with branches. No emojis yet.
```toml
  lol = "log --graph --decorate --oneline"
```

Now the emoji command as an alias too. This will use `lol` as defined above.

```toml
  emoji = "! git lol | sed 's/docs:/📝 docs:/g ; s/feat:/✨ feat:/g ; s/chore:/🔧 chore:/g ; s/tag:/🔖 tag:/g ; s/fix:/🐛 fix:/g ; s/Initial commit$/🎉 Initial commit/g'"
```

Save the config.

Now you can use it anywhere in a git repo. You don't need to restart your terminal.

```sh
git emoji
```
```
* a15457b Update development.md
* 00e49b0 Create development.md
...
```
