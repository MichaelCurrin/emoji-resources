# Git log emoji
> Prettify a conventional commit git log with emojis

## Features

- Run this tool as an alternative to `git log`, whenever you need to.
- You'll get an emoji inserted before any conventional commit leader (prefixes).
- Works on any git repo with at least one conventional commit message.
- Safe and non-destructive. This only affects your viewing output and doesn't change the commits.
- Simply copy and paste code to your git config. Easy to change later. No need to install a tool or set up a shell script.


## Commit message style

### Write conventianl commits

For example, write commit messages like these.

```sh
docs: Update README.md
fix: Rename variable
```

See [Conventional Commits](https://www.conventionalcommits.org/) homepage to learn more on writing commits.


### Add emojis

We want to automate displaying messages as:

```sh
📝 docs: Update README.md
🐛 fix: Rename variable
```

See [Gitmoji](https://gitmoji.dev/) site for a guide to choosing emojis, so you are following a standard.


## The command to run

For Bash or Linux, using `sed` to find and replace.

Here is a long multi-line command you can run. 

It is not complete for all cases, but you get the idea.

```sh
git lol | sed 's/docs:/📝 docs:/g
s/feat:/✨ feat:/g
s/chore:/🔧 chore:/g
s/tag:/🔖 tag:/g
s/fix:/🐛 fix:/g
s/Initial commit$/🎉 Initial commit/g'
```

Example output from that command, with emojis inserted by the command.

```
* a15457b Update development.md
* 00e49b0 Create development.md
* a400c64 ✨ feat: Update link layout
* bb96ef5 (🔖 tag: v0.2.0) ✨ feat: Add to homepage
* 715c4bd 📝 docs: Add to README.md
* 3670bfb ✨ feat: Change theme to dark
* 9720c96 🎉 Initial commit
```


## Set up an alias

To make is easier to use the command above any time, you can add it to your git aliases in `~/.gitconfig`.

Add to your git config under `[alias]` section.

This shows a commit message in a single line and adds a tree flow for use with branches. No emojis yet.

```toml
  lol = "log --graph --decorate --oneline"
```

Now set the emoji command as an alias too. This will use `lol` as defined above.

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
* a400c64 ✨ feat: Update link layout
* bb96ef5 (🔖 tag: v0.2.0) ✨ feat: Add to homepage
* 715c4bd 📝 docs: Add to README.md
* 3670bfb ✨ feat: Change theme to dark
* 9720c96 🎉 Initial commit
```
