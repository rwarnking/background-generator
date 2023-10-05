# Background Generator

## How To

### HTML to transparent PDF

Unfortunately it seems to be very difficult to transform HTML into a PDF that retains a
transparent background.

The usual options for exporting a HTML document to PDF are

- use a PDF reader and either use `print` or `save as PDF`
- use an online tool
- use a special software

But all these option either do not evaluate the JavaScript or fill the background with white
instead of keeping it transparent.

#### The solution

Using [this website](https://cloudconvert.com/svg-to-pdf) the following steps should work:

1. Convert the HTML to a PDF by opening it in the browser and using `print`
2. Use the website to convert the PDF to SVG
3. Edit the SVG, the following line needs to be removed
  - `<path d="M 0 0 L 1920 0 L 1920 1084 L 0 1084 Z " fill="#ffffff"/>`
4. Convert the modified SVG back to PDF

The background should now be transparent.
If you are not sure wether the background is transparent you can
adjust the settings of your PDF viewer to show a transparency grid instead of default white.

## Todos

Expand the project, such that the user can alter the settings in the HTML-page and directly
export the result to a PDF or SVG.
