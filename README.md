# Base.scss

Base.scss is currently based entirely on [Set.scss](https://github.com/robwierzbowski/set.scss) by [Rob Wierzbowski](https://twitter.com/robwierzbowski).

Set.scss is a [Sass](http://sass-lang.com/) normalize and base stylesheet that emphasizes setting your own values instead of linking to an unedited third-party stylesheet. As [Eric Meyer](http://meyerweb.com/eric/tools/css/reset/) says, CSS resets are "a starting point, not a self-contained black box of no-touchiness."

## Using Base.scss

Set.scss doesn't make assumptions on how baseline elements should be styled. It provides scaffolding to fill with element styles specific to your project, prepopulated with normalization rules from [Nicolas Gallagher's](https://twitter.com/necolas) [Normalize.css](https://github.com/necolas/normalize.css) and sensible defaults from [HTML5 Boilerplate](https://github.com/h5bp/html5-boilerplate).

Base.scss improves upon Set.scss is trying to leverage the modularity of Sass by breaking out the differnt sections of Set.scss for two reasons.

1. It allows you to easily eliminate sections that you are not using in a particular project
2. It breaks up the style sheet into more managable chunks. As the idea behind Set.scss and Base.scss is to build onto them it makes sense to abstact each section you may be building on.

Comments above selectors let you know which rules must be set, and the project where the rule originated:

```scss
// Set margin (Normalize)
body {
  margin: 0;
}
```

If a rule must be set to a certain value, the value is given in the comment as well:

```scss
// Set font-size, font-family (Normalize)
// Set white-space: pre-wrap (Normalize)
pre {
  font-size: 1em;
  font-family: $type-stack-monospace;
  white-space: pre-wrap;
}
```
## Testing

Base.scss currently provides a barebones grunt task to build your base.css file to use for testing against the test.html provided

If you have never used [Grunt](http://gruntjs.com/) check out their site.

### Technical notes

This project currently tracks:

- [Set.scss](https://github.com/robwierzbowski/set.scss) v0.1.1
- [Normalize.css](https://github.com/necolas/normalize.css) v2.1.2.
- [HTML5 Boilerplate](https://github.com/h5bp/html5-boilerplate) v4.2.0

Since this is primarily a re-interpretation of Normalize.css 2.x, browser support is identical: Modern browsers and IE8+.

`html [element]` is a hack to target android 4.x fixes, in case you're wondering (I was).
