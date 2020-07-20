## Media Queries

CSS uses media queries to adapt a website’s content to different screen sizes. 

With media queries, CSS can detect the size of the current screen and apply different CSS styles depending on the width of the screen.

Example 1

```css

@media only screen and (max-width: 480px) {
  body {
    font-size: 12px;
  }
}

```

The example above demonstrates how a media query is applied. 

The media query defines a rule for screens smaller than 480 pixels (approximately the width of many smartphones in landscape orientation).

Let’s break this example down into its parts:

1. `<@media>` — This keyword begins a media query rule and instructs the CSS compiler on how to parse the rest of the rule.

2. `<only screen>` — Indicates what types of devices should use this rule. In early attempts to target different devices, CSS incorporated different media types (screen, print, handheld). The rationale was that by knowing the media type, the proper CSS rules could be applied. However, “handheld” and “screen” devices began to occupy a much wider range of sizes and having only one CSS rule per media device was not sufficient. `<screen>` is the media type always used for displaying content, no matter the type of device. The `<only>` keyword is added to indicate that this rule only applies to one media type (screen).

3. `<and (max-width : 480px)>` — This part of the rule is called a media feature, and instructs the CSS compiler to apply the CSS styles to devices with a width of 480 pixels or smaller. Media features are the conditions that must be met in order to render the CSS within a media query.

4. CSS rules are nested inside of the media query’s curly braces. The rules will be applied when the media query is met. In the example above, the text in the body element is set to a `<font-size>` of 12px when the user’s screen is less than 480px.
}

Example 2

```css

@media only screen and (min-width: 320px) and (max-width: 480px) {
    /* ruleset for 320px - 480px */
}

```

The example above would apply its CSS rules only when the screen size is between 320 pixels and 480 pixels. Notice the use of a second and keyword after the min-width media feature. This allows us to chain two requirements together.

The example above can be written using two separate rules as well:

```css

@media only screen and (min-width: 320px) { 
    /* ruleset for >= 320px */
}


@media only screen and (min-width: 480px) { 
    /* ruleset for >= 480px */
}

````

The first media query in the example above will apply CSS rules when the size of the screen meets or exceeds 320 pixels. The second media query will then apply CSS rules when the size of the screen meets or exceeds 480 pixels, meaning that it can override CSS rules present in the first media query or apply additional CSS rules that are not already present in the first.

Both examples above are valid, and it is likely that you will see both patterns used when reading another developer’s code.

Example 3

If only one of multiple media features in a media query must be met, media features can be separated in a comma separated list.

For example, if we needed to apply a style when only one of the below is true:

* The screen is more than 480 pixels wide

* The screen is in landscape mode

We could write:

```css

@media only screen and (min-width: 480px), (orientation: landscape) {
    /* CSS ruleset */
}

```

In the example above, we used a comma (,) to separate multiple rules. The example above requires only one of the media features to be true for its CSS to apply.

Note that the second media feature is orientation. The orientation media feature detects if the page has more width than height. If a page is wider, it’s considered landscape, and if a page is taller, it’s considered portrait.
