## About the Noctus Theme

> This is a HUGE work in progress! No Light Theme included yet!

The Noctus Theme for Obsidian is a theme made with the intent to be as modular **as possible**, which is why it was initially known as the "Modulo Theme". It uses Oklch instead of RGB as a color space, which allows for more modular treatment of colors and better gradients **BUT also leads to many snippets becoming incompatible with this theme. *Yet we intend to make snippets of our own to both extend the functions of this theme but also offer beloved snippets compatible with our theme.***

Initially, this theme was just a modified version of the [Obsidian Encore Theme](https://github.com/carbonateb/obsidian-encore-theme) by Carbonateb but overtime I, Shayde, looked at other themes, like the [Minimal Theme](https://github.com/kepano/obsidian-minimal) by kepano, and started making it a theme of its own.

Around that time I also started working on an obsidian snippet that would change the colors, functions, and similar of callout when putting in different callout (meta-) data, which has become a major function in this theme and has long surpassed the snippet since. I have added formats, like a timeline callout based on harr's [Timeline CSS](https://forum.obsidian.md/t/css-snippet-timeline-as-callout/93652) and more.

### Installation

As the theme is still a work in progress, it is not yet in the official Obsidian theme store; Thus, if you want it to be kept up to date, using the [BRAT Plugin by TfTHacker](https://github.com/TfTHacker/obsidian42-brat) is recommended.

#### Steps

1. Install the BRAT plugin from the obsidian plugin store
2. Enable it and go into the options
3. Below "Beta themes list", press "Add beta theme" and paste this repository's link into it (`https://github.com/Reparse-dev/noctus-obsidian-theme`)
4. Press "Add theme" and presto- it's done! Enjoy the Noctus Obsidian Theme ^-^

### Features

1. Usage of Oklch instead of RGB: Allows more precise gradients and more modular coloring.
2. New Callout Formats: Timeline callouts and a reverse callout (places title below content).
3. New Callout Presets: Highlight, Result, and Solution.
4. Modular Callouts: Allows changing colors and icons of all Presets and Formats, even down to precise color value changes and more!
5. Style Settings like line-lenght, featuring line lengths made to approximate PDF exports and line lengths for [optimal readability](https://baymard.com/blog/line-length-readability) (WIP, only line length thus far.)

#### Plugin Integrations

We integrate CSS for plugins we personally use into the base theme, given the CSS for it is not exessive as to warrant a CSS Snippet of its own. All of these plugins are worth checking out!

**List of currently integrated Plugins**
- [Calendar Plugin by Liam Cain](https://github.com/liamcain/obsidian-calendar-plugin)
- [Dataview Plugin by Michael Brenan](https://github.com/blacksmithgu/obsidian-dataview)
- [Datacore Plugin by Michael Brenan](https://github.com/blacksmithgu/datacore)
- [Chat View by Aditya Majethia](https://github.com/adifyr/obsidian-chat-view) (WIP)
- [Excalidraw Plugin](https://github.com/zsviczian/obsidian-excalidraw-plugin) (Currently only removes the Excalidraw welcome)

### How to make Theme Snippets

> Not done yet, might be subject to heavy changes and many variables are yet to be set up.

Every color in this theme is split into multiple variables, like this:

`--colorname-lightness`, `--colorname-chroma`, `--colorname-hue`

`--colorname-color: var(--colorname-lightness) var(colorname-chroma) var(colorname-hue)`

For some, like blockquote or callout color we also have opacity variables: `--colorname-opacity`

And then, for each element, the colors are implemented akin to this:
```css
element {
  color: oklch(var(--colorname-color) / var(--colorname-opacity))
}
```

### Contributing

Contributions via documentation, and general improvements (like "bug fixes") are always welcome. For more major feature work, make an issue about the feature idea / reach out to me so we can judge if it is right for us and how best to implement it.

#### Dev Ressources

- https://oklch.com/
- https://lucide.dev/icons/
- https://github.com/chrisgrieser/obsidian-theme-design-utilities
