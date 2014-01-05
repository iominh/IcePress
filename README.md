# A simple responsive Octopress theme

IcePress is a responsive Octopress theme that was forked from PageTurner,
a theme created by Elise Hein and Karl Sutt, which unfortunately is not under active development.
This team builds on PageTurner to improve upon its syntax highlighter, excerpt support, and
fixes various issues.

It is currently under active development. See the live demo for more information.

## Demo

See http://icepress.minh.io

## Install

From your Octopress root directory:

	# git clone https://github.com/minhongrails/IcePress.git .themes/IcePress
	# rake install['IcePress']
	# rake generate

## About

`sass/_variables.scss` allows for a lot of customization.

### Fonts

I experimented with a lot of fonts and didn't bother removing the ones I
didn't like so there's a lot to choose from. See `sass/_typography.scss`
for a full list of fonts that come with this theme.

### Code blocks and syntax highlighting

The theme comes with Prettify.js for syntax highlighting. My color scheme of
choice for Prettify was Hemisu from
http://jmblog.github.com/color-themes-for-google-code-prettify/. To use a
different color scheme, add the css file to `sass/.` change the stylesheet name in the
`<head>` section of `source/_layouts/default.html` (this is the base layout
that all other pages use). You will need to save the css file as .scss,
otherwise `rake generate` won't pick it up.

Using Prettify does not require any special markdown syntax. You simply
begin a code block with the usual indentation or grave characters. 

Of course, the the standard of using Pygments and `{% codeblock %}` should
work as well, but this theme does not include styling for any `{% codeblock
%}` elements.


## Issues

- zclip.js error `PPB_Graphics2D.PaintImageData: Rectangle is outside
	bounds.`
- `_responsive.scss` mixins are causing syntax errors. This is probably
	caused by the way rake compiles sass files. Using regular `@media`
	queries instead until fixed.
- No styling for Octopress codeblock and gist plugins yet
- If you've enabled like buttons or disqus comments in your _config.yml, you will need to add relevant tags and styling
