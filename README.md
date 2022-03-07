## Update (2017-10-18)

The fix to continue support for custom devtools themes landed in m62. The new method injects the custom stylesheet into every shadow root that gets rendered. This caused devtools to be super sluggish especially with the shadow piercing combinators. I haven't finished refactoring the styles, but I decided to release it early to address some of the performance and style issues.

## How You Can Help

Please [file issues](https://github.com/mauricecruz/zero-base-themes/issues) for anything that seems broken/unstyled.

I'm trying to prune as much css as possible to improve performance. Haven't figured out a good way of verifying if a selector was removed/deprecated by the Chrome Team other than searching the code base. And that's a slow and painful process.

If you want to pitch in with the cleanup, feel free to create pull requests.

## Only Supporting Stable Channel (Temporarily)

The css combinators used to override the devtools CSS is deprecated and support will be removed from Chrome in m63 (~ December 2017). The [Chrome Team will continue to support custom themes](https://bugs.chromium.org/p/chromium/issues/detail?id=709732&can=2&q=709732) by changing the implementation.

The implementation change requires a rewrite of this theme. During this time, only stable channel will be supported.

## Zero Base Themes

An assortment of Chrome Devtools themes that use the Zero Base Template.

## Contributing

Zero Base Themes is built on LESS. Grunt is used to listen for changes to LESS files and generates CSS. This means [Node](http://nodejs.org/) is required.

## Getting Started

1. Clone this repo: `git clone https://github.com/mauricecruz/zero-base-themes.git`.

2. Install dependencies: `npm install`.

3. To use an existing theme: `grunt`. (If you're going to work on your own theme: `grunt watch` to listen for changes).

4. `Chrome > Preferences... > Extensions > DevTools Theme: Zero Dark Matrix = Enabled`

5. chrome://flags (make sure `Enable Developer Tools experiments` is enabled).

6. In Chrome Dev Tools > Settings (cog icon or `Shift+?`) > Experiments > Allow custom UI themes.

7. Close and reopen the dev tools.

## Contributing to Template Source

All template files are located in the `/less` directory. Files beginning with an `_` indicate template partials. Any addition/removal of template partials should be reflected in the build file.

## Changing Themes

Copy `/themes/_theme-template.less` and modify color values accordingly. Rename the file and save in the `/themes` directory. Specify the theme of your choice in `config.less`.

## Alternatives

Chrome now has an option to let you select different themes via Settings > Appearance > Theme: Light/Dark.

## Additional Resources

Blog post and screencast showing how to get up and running and create your own theme as well http://s10wen.com/blog/2014/03/12/chrome-dev-tools-theming-with-zero-base-themes/

## Community

- [Twitter](https://twitter.com/draculatheme) - Best for getting updates about themes and new stuff.
- [GitHub](https://github.com/dracula/dracula-theme/discussions) - Best for asking questions and discussing issues.
- [Discord](https://draculatheme.com/discord-invite) - Best for hanging out with the community.
