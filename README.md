# Typora Theme Toolkit

This toolkit contains a simple theme template, and some HTML files for designers/developers to preview/debug css theme right inside their browser.

## Usage

Install the necessary dependencies using NPM.

```bash
npm install
```

Configure your theme in `theme/custom/theme.css` and put all of its related related resources, like images or fonts or imported css used by your css file inside `theme/custom` folder.

To preview your theme, run the following command:

```bash
npm run preview
```

Your theme is now available inside the `dist` folder.

### Supported Previews

- `lorem.html`  Preview the basic typesetting.
- `outline-open-and-focus-mode.html` Preview pinned outline panel on Typora for macOS, and focus mode.
- `source-mode.html` Preview source code mode syntax highlighting style.
- `ui-controls.html` Preview some control UIs on macOS, Windows, and Linux and window frame for "unibody"  style on Windows.
- `ui-controls2.html` Preview tips/notifications in Typora and the side panel style on Windows/Linux.
- `unibody.html` Preview the menu style for "unibody"  style on Windows.


So you may find components you never seen in Typora because they may only be available for specific OS platform. If you want to submit your Typora theme to [Typora Theme Gallery](http://theme.typora.io), and share with other users, we strongly recommend you to go through all those HTML files to make your theme looks great in all platforms.

### Publishing Your Theme

Set the name of your theme inside the `theme/config.js`.

```js
module.exports = {
  name: 'your-theme-name'
}
```

Then run build script.

```bash
npm run build
```

## Notice

- This toolkit is created for Typora >= 0.9.9.7.8 (macOS) or Typora >= 0.9.19 (Windows/Linux). Update your Typora to latest version, and update this toolkit to latest version by `git pull` or other commands.
- **Do not edit/format HTML files**, even though they are ugly and unreadable, currently the final rendered output is whitespace sensitive.
- Better to use Chrome or Safari. (in macOS, typora use Safari as web engine, in Windows/Linux typora use Chrome, but their rendering results are almost same).
- If you meet error like `[Not allowed to load local resource: file://XXXX]` in browser's console, the quickest solution for me is to use tools like [httpster](https://github.com/SimbCo/httpster) or [CodeKit](https://incident57.com/codekit/) to host the web content into localhost.

## Documentations

- [How to write a Typora theme](http://theme.typora.io/doc/Write-Custom-Theme/)
- [Typora Theme Gallery](http://theme.typora.io)
- [Some Tips on Typora Styling](http://support.typora.io/style)

## Issues && Contact

If you find bugs, or issues, or require some `class` for rendered HTML Dom in typora, please:

- Put it into <https://github.com/typora/typora-issues/issues>
- Contact us via <hi@typora.io>



