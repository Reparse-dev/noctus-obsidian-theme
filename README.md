## About the Noctus Theme

> This is a HUGE work in progress!

The Noctus Theme for Obsidian is a theme made with the intent to be as modular **as possible**, which is why it was initially known as the "Modulo Theme". It uses Oklch instead of RGB as a color space, which allows for more modular treatment of colors and better gradients **BUT also leads to many snippets becoming incompatible with this theme. *Yet we intend to make snippets of our own to both extend the functions of this theme but also offer beloved snippets compatible with our theme.***

Initially, this theme was just a modified version of the [Obsidian Encore Theme](https://github.com/carbonateb/obsidian-encore-theme) by Carbonateb but overtime I, Shayde, looked at other themes, like the [Minimal Theme](https://github.com/kepano/obsidian-minimal) by kepano, and started making it a theme of its own.

Around that time I also started working on an obsidian snippet that would change the colors, functions, and similar of callout when putting in different callout (meta-) data, which has become a major function in this theme and has long surpassed the snippet since. I have added formats, like a timeline callout based on harr's [Timeline CSS](https://forum.obsidian.md/t/css-snippet-timeline-as-callout/93652) and more.

### Features

1. Usage of Oklch instead of RGB: Allows more precise gradients and more modular coloring.
2. New Callout Formats: Timeline callouts and a reverse callout (places title below content).
3. New Callout Presets: Highlight, Result, and Solution.
4. Modular Callouts: Allows changing colors and icons of all Presets and Formats, even down to precise color value changes and more!

#### Plugin Integrations

We integrate CSS for plugins we personally use into the base theme, given the CSS for it is not exessive as to warrant a CSS Snippet of its own. All of these plugins are worth checking out!

**List of currently integrated Plugins**
- [Calendar Plugin by Liam Cain](https://github.com/liamcain/obsidian-calendar-plugin)
- [Dataview Plugin by Michael Brenan](https://github.com/blacksmithgu/obsidian-dataview) (Might add support for the experimental [Datacore Plugin](https://github.com/blacksmithgu/datacore) as well)
- [Chat View by Aditya Majethia](https://github.com/adifyr/obsidian-chat-view) (WIP)
- [Excalidraw Plugin](https://github.com/zsviczian/obsidian-excalidraw-plugin) (Currently only removes the Excalidraw welcome)

### How to make Theme Snippets

Every color in this theme is split into multiple variables:

`--colorname-lightness`, `--colorname-chroma`, `--colorname-hue`

`--colorname-color: var(--colorname-lightness) var(colorname-chroma) var(colorname-hue)`
For some, like blockquote color: `--colorname-opacity`

And then, for each element, it is implemented akin to this:
```css
element {
  color: var(--colorname-color / --colorname-opacity)
}
```
