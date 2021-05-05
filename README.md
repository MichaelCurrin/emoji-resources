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

See my [Python Strings](https://michaelcurrin.github.io/dev-cheatsheets/cheatsheets/python/strings/) cheatsheet for more info.


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
