# PrettyLink Shortcode

## Install Module

Add the following code to your module list in the `config/_default/module.toml` file.

```toml
[[imports]]
path = "github.com/mariox77/hugo-modules/shortcodes/pretty-link"
```

Add the following code to the `config/_default/params.toml` file.

```toml
# pretty_link
[pretty_link]
theme = "hugoplate"
```

## Shortcode Implementation

Available parameters:

- href: Hugo internal post or external URL

## Customize look and feel (eg. theme)

Views must be different for each theme in Hugo.

Currently, I have included default support for `Hugoplate`'s Bigfan. (However, since I'm not a CSS expert, the quality might be somewhat lacking.)

There are two files responsible for the view:
- `simple-link.html`: A simple card displaying only the title and summary.
- `thumbnail-link.htm`l: A card layout displaying the thumbnail, title, and summary.

Based on the theme set in `pretty_link.theme`, please create these files accordingly.

Using `hugoplate` as an example, the paths are:
- `layouts/partials/pretty-link/themes/hugoplate/simple-link.html`
- `layouts/partials/pretty-link/themes/hugoplate/thumbnail-link.html`

Create the files in the local directory and find the corresponding file in this repository to copy and paste its contents.

Modify the two files to match the theme you are currently using. If you believe the changes you made to the theme could benefit other users, please submit a Pull Request.
