# Git log emoji
> Prettify a conventional commit git log with emojis

## Features

- Run this tool as an alternative to `git log`, whenever you need to.
- You'll get an emoji inserted before any conventional commit leader (prefixes).
- Works on any git repo with at least one conventional commit message.
- Safe and non-destructive. This only affects your viewing output and doesn't change the commits.
- Simply copy and paste code to your git config. Easy to change later. No need to install a tool or set up a shell script.


## Resources

- [Conventional Commits](https://www.conventionalcommits.org/) homepage - to learn more on writing Conventional Commits messages. The _Summary_ section covers the prefixes used here.
- [Type](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#type) on Angular repo. This is linked from the Conventional Commits website as "Angular Convention" and explains what `build` etc. means.
- [Gitmoji](https://gitmoji.dev/) site - for a standard of using emojis in commits. That page is _very_ detailed and the emojis don't all map to Conventional Commit standard, so I won't try and cover them all here.


## Commit message style

### Write conventianl commits

This guide expects you to write commit messages like these.

```sh
docs: Update README.md
fix: Rename variable
```

### Add emojis

Then we'll use a command to turn the above into this:

```sh
📝 docs: Update README.md
🐛 fix: Rename variable
```


## The command to run

For Bash or Linux, using `sed` to find and replace.

Here is a long multi-line command you can copy and paste. Prevent going through the _entire_ git log, I've limited to the most recent 20 commits.

```sh
git lol -20 | sed 's/feat:/✨ feat:/g
s/fix:/🐛 fix:/g
s/build:/👷‍♂️ build:/g
s/chore:/🔧 chore:/g
s/ci:/🔧 ci:/g
s/docs:/📝 docs:/g
s/refactor:/♻️ refactor:/g
s/perf:/⚡️ perf:/g
s/style:/🎨 style:/g
s/test:/✅ test:/g
s/tag:/🔖 tag:/g
s/Initial commit$/🎉 Initial commit/g'
```

Example output with emojis inserted:

```
* a15457b Update development.md
* 00e49b0 Create development.md
* a400c64 ✨ feat: Update link layout
* bb96ef5 (🔖 tag: v0.2.0) ✨ feat: Add to homepage
* 715c4bd 📝 docs: Add to README.md
* 3670bfb ✨ feat: Change theme to dark
* 9720c96 🎉 Initial commit
```

Notes:

- See use of one `sed` call that uses newlines to separate rules. Or you can do it in one line using semicolons.
- Use of colons in the rule like `ci:` means if `ci` appears not as a prefix but in the middle of your message, it won't get affectd.
- For prefixes.
    - I've followed the Convetional Commit website's _Summary_ section.
    - Then added some non-standard ones that make sense to me.
    - The `chore` prefix is not actually in the Angular Convention. 
    - You might consider dependency changes as part of your "build system" and so use `build:` as a prefix like I do.
- Character encoding.
    - Don't worry if the text looks weird in your console or editor e.g. `👷<200d>` for build and `⚡<fe0f>` for perf. The command output still looks correct.
- For emojis, here isn't a clean mapping for some prefixes.
    - There are multiple `ci` emojis.
    - For `chore`, as it depends on the context. With a smarter system looking at the rest of the message, one of these could be used.
        - `🔥` for `Remove code or files.` 
        -  `🔧` for `Add or update configuration files.`.
        -  `🚚` for `Move or rename resources (e.g.: files, paths, routes).`
    - There also multiple dependency-related emojis, so it was easiest to just use construction emoji.

<!-- TODO turn this into a non-code mapping cheatsheet -->

<!-- TODO add support for one-word commits like "style" or "docs" -->

<!-- TODO add support for Update x -->

<!-- TODO add support for recognized extension - need grouping to add it back and that gets messy or not possible in sed . e.g. Update ...yml - or use Auto Commit -->

<!-- TODO :emoji: sub for emoji -->

If you want to test that without `git`:

```sh
echo 'perf: abc' | sed 's/feat:/✨ feat:/g
s/perf:/⚡<fe0f> perf:/g
```
```
⚡️ perf: abc
```


## Set up an alias

To make is easier to use the command above any time, you can add it to your git aliases in `~/.gitconfig`.

Add to your git config under `[alias]` section.

This shows a commit message in a single line and adds a tree flow for use with branches. No emojis yet.

```toml
  lol = "log --graph --decorate --oneline"
```

Now set the emoji command as an alias too. This will use call `lol` as defined above and then do the replacement.

```toml
  emoji = "! git lol | sed 's/docs:/📝 docs:/g ; s/feat:/✨ feat:/g ; s/chore:/🔧 chore:/g ; s/tag:/🔖 tag:/g ; s/fix:/🐛 fix:/g ; s/Initial commit$/🎉 Initial commit/g'"
```

Note - this alias is note complete yet as misses some items until I update it.

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
