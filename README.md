# hovercard.js

A script to load cards when you hover over a link in an article.

## Example

![Text in an article with an active hovercard that contains an image, a title, and a description](screenshot.png)

## Getting Started

The `hovercard.js` script searches for all `<a>` tags enclosed within an `<article>` tag on a web page. Mouse hover and focus listeners are added to each link. When the mouse hovers over a link, `hovercard.js` looks for the `href` value of the link in a JSON object called `hovercards`. If the link is found in the JSON object, a hovercard is added directly below the link on the page.

When a user hovers off the link or moves focus onto another element (i.e. by using the keyboard to navigate links on the page), the hovercard will disappear.

## Usage

To use the hovercard script, first download a copy and upload it to your site. Then, add this code above the closing `</body>` tag on your web page:

```html
<script src="./path/to/hovercard.js"></script>
```

Substitute the path of the script in the example above with the location of the script on your site.

You should add a JSON object to every page that contains a hovercard. This JSON object should use the following structure:

```json
{
    "https://example.com": {
        "title": "Example Domain",
        "description": "This domain is used for examples."
        "photo": "https://example.com/example.png"
    }
}
```

Keys in the JSON object represent links on the page to look up. The only required key value is `title`. If a description and/or photo are provided, these will be included in the hovercard.

## License

This code for this project is placed in the public domain.

## Contributors

- capjamesg
