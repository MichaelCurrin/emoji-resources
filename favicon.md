# Favicon

Using an emoji as favicon.


## SVG for link tag

Now that all modern browsers support SVG favicons, here's how to turn any emoji into a favicon.svg:

From [Emojis as Favicons](https://css-tricks.com/emojis-as-favicons/) tutorial.

```html
<link rel="icon" 
  href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>
  🎯</text></svg>">
```

I tested this out and it works great setting the favicon.


## Generate icon

See [Emoji favicons on Favicon Generator](https://favicon.io/emoji-favicons/) website.

Browse favicons which get converted to files you can download and use.

Then use as:

```html
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
<link rel="manifest" href="/site.webmanifest">
```
