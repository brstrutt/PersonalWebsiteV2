# Description

This is a total rewrite of my personal website to use a static site generator instead of PHP + and a MySQL Database. Hopefully this should make the website much more lightweight as it never really needed any dynamic elements anyway.

Currently trying out Hugo.

## Development

To develop:

1. Clone the repo
2. Open the devcontainer
3. To see the site run `hugo server`. Use `hugo server -D` to see draft posts. This server should auto rebuild whenever you update the content.
4. To build the release html/css run `hugo`. The site will be built to the *./public* directory
