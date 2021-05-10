# Git


## Commit messages

Some people like to add emojis to commit messages that are semvar commits messages.

There are some conventions around which emoji to use.

You can also use command line tools help you and even VS Code extensions.

You can also just insert GitHub emojis in your markdown or static site

### Gitmoji

- [Gitmoji site](https://gitmoji.carloscuesta.me/)
- [Gitmoji CLI](https://github.com/carloscuesta/gitmoji-cli)
- [Gitmoji changelog](https://github.com/frinyvonnick/gitmoji-changelog) - Generate changelog from semvar emoji commits.

### Guides

Emoji guides for commit messages.

- [gist](https://gist.github.com/parmentf/035de27d6ed1dce0b36a) by parmentf.
- [Commit Message Emoji](https://github.com/dannyfritz/commit-message-emoji) repo by dannyfritz.
- [gitmoji.carloscuesta.me](https://gitmoji.carloscuesta.me)


## Git emojis in GitHub markdown

Git supports emojis in markdown. These are down with a keyword between colons, similar to Slack. 

e.g.

- Bowtie
    - Rendered: :bowtie:
    - Markdown:
        ```markdown
        :bowtie
        ```

Git emoji cheatsheets:

- [gist](https://gist.github.com/roachhd/1f029bd4b50b8a524f3c) by roachhd.
- [gist](https://gist.github.com/rxaviers/7360908) by rxaviers.
- [ikatyang/emoji-cheat-sheet](https://github.com/ikatyang/emoji-cheat-sheet)
    > This cheat sheet is automatically generated from GitHub Emoji API and Unicode Full Emoji List.


## Git emoji plugins for your website

While the Git emojis with format `:name:` and covered above render fine on plain GitHub markdown, some tools need a plugin to render emojis. 

Docsify plugins:

- [Emoji](https://docsify.now.sh/en/plugins?id=emoji)

Jekyll plugins:

- [jekyll/jemoji](https://github.com/jekyll/jemoji)
    - Available on [rubygems](https://rubygems.org/gems/jemoji/).
    - Supported on GitHub Pages.
- [emoji-for-jekyll](https://rubygems.org/gems/emoji_for_jekyll)
    - Not on Github Pages supported list.
    - May not be kept up to date. The URL gets broken from a CDN. e.g. `https://github.global.ssl.fastly.net/images/icons/emoji/anchor.png`.
    - See emojis listed in [emoji.json](https://github.com/yihangho/emoji-for-jekyll/blob/master/lib/emoji.json).
