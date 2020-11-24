# Emoji Resources
> Find services, add-ons and actual emojis to help with all your emoji needs

> Emojis are a pictorial language used mainly in electronic messaging to express a variety of emotions, objects or ideas. [source](https://github.com/topics/emoji).

They can be in the form of unicode characters which can be used in text files - including scripts and HTML pages. They can also be used in the GitHub context as `:name:` and then the result rendered in markdown.

Note that the mapping of unicode codes to the symbols appears consistent across devices and browsers, but each platform can choose _how_ to represent the image such as using more or less detail and color choices.


## About emojis

- [Emoji](https://en.wikipedia.org/wiki/Emoji) on Wikipedia.
- [Emojis.wiki](https://emojis.wiki/)
    > Emoji Encyclopedia,
    >
    > a full collection of 📙 Emoji Meanings, 👨‍💻 Data, 🙅‍♀️🍕🍔🍟 Combinations, Emoji Art and more. Easy to Copy and Paste!
- [Emoticons](https://en.wikipedia.org/wiki/List_of_emoticons) `:)` and their corresponding emojis.


For interest, see this blog post - [Emoji skin modifier handshake](https://thenextweb.com/shareables/2020/08/12/emoji-skin-tone-modifier-handshake/). Aside from the skin color emojis discussed, this gives insight into how emoji/unicode standards are defined and implemented. Plus mention of nett new emojis or variations on existing ones, which is a reminder that emojis are not fixed.


## Unicode emojis

Emojis are part of the unicode range of characters. They can be inserted as characters, platform independent. Though different operating systems and applications might have different images for each emoji specification.

e.g.

- 😃


Unicode characters including accented characters and emojis are suppored in Python 3. They can also be converted from unicode strings into bytes.

 ```python
 >>> '😃'
'😃'
>>> print(_)
😃
>>> '😃'.encode('utf-8')
b'\xf0\x9f\x98\x83'
```


## View and search emojis

### List

- [Full emoji list](https://unicode.org/emoji/charts/full-emoji-list.html) on [unicode.org](https://unicode.org) website.
- [Emoji cheat sheet](https://www.webfx.com/tools/emoji-cheat-sheet/) on WebFx.

### By platform

If you are interested to compare emojis across platforms, I recommend going to [emojipedia.org/](https://emojipedia.org/) and see their platforms list at the bottom.

Some links:

- _Emojipedia_
    - [Whatsapp emojis](https://emojipedia.org/whatsapp/)
    - [Twitter emojis](https://emojipedia.org/twitter/)
    - [Slack emojis](https://emojipedia.org/slack/) 
        - Some are animations. Some are contributed by users and so do not follow a fixed standard.
        - See also [Slackmojis](https://slackmojis.com/)

### Emoji search services

Want to lookup emojis by category or search for emojis based on text? Use one of these.

This list is not curated, so I cannot guarantee the quality of these.

- [EmojiKeyboard.io](https://emojikeyboard.io/)
- [EmojiPedia](https://emojipedia.org/)
- [GetEmoji](https://getemoji.com/)
- [EmojiSearch](https://emojisearch.com/)
- [EmojiFinder](https://emojifinder.com/)
- [Emoji cheat sheet](https://www.webfx.com/tools/emoji-cheat-sheet/)

As far as I can tell, those all produce unicode emojis which you can copy and paste across platforms.


### GitHub

See projects on GH relating to [#Emoji](https://github.com/topics/emoji).

See [/emojis](https://api.github.com/emojis) endpoint on the REST API. Lists all emojis as PNGs e.g. [1f4af.png?v8](https://github.githubassets.com/images/icons/emoji/unicode/1f4af.png?v8)


## Git emoji

### Use git emojis in GitHub markdown

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

### Git emoji plugins for your website

While the Git emojis with format `:name:` and covered above render fine on plain GitHub markdown, some tools need a plugin to render emojis. 

Docsify plugins

- [Emoji](https://docsify.now.sh/en/plugins?id=emoji)

Jekyll plugins 

- [jekyll/jemoji](https://github.com/jekyll/jemoji)
    - Available on [rubygems](https://rubygems.org/gems/jemoji/).
    - Supported on GitHub Pages.
- [emoji-for-jekyll](https://rubygems.org/gems/emoji_for_jekyll)
    - Not on Github Pages supported list.
    - May not be kept up to date. The URL gets broken from a CDN. e.g. `https://github.global.ssl.fastly.net/images/icons/emoji/anchor.png`.
    - See emojis listed in [emoji.json](https://github.com/yihangho/emoji-for-jekyll/blob/master/lib/emoji.json).

### Commit message emojis

Emoji guides for commit messages.

- [gist](https://gist.github.com/parmentf/035de27d6ed1dce0b36a) by parmentf.
- [Commit Message Emoji](https://github.com/dannyfritz/commit-message-emoji) repo by dannyfritz.
- [gitmoji.carloscuesta.me](https://gitmoji.carloscuesta.me)


## Other

- [Emoji Screen](https://emojiscreen.com/) website. 
    > A listing of movies, TV shows and musicals depicted through emojis. Click on the emojis to reveal the show or movie name!


## IDE support

Extensions

- VS Code
    - [Emoji git](https://github.com/benjaminadk/emojigit)
         - Add emojis to your commit messages
         - Emoji cheatsheet
         - Based on gitmoji - using emojis for semantic commits like bug fixes
         - See mapping in [index.js](https://github.com/benjaminadk/emojigit/blob/master/src/gitmojis/index.js)
    - [Emoji log](https://marketplace.visualstudio.com/items?itemName=ahmadawais.emoji-log-vscode)
        - Add emojis to your commit messages
    - [Markdown emoji](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-emoji)
        - There are a lot of similar extensions to this and this is just one I picked for a high rating.
