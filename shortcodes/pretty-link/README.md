# PrettyLink Shortcode

## Install Module

Add the following code to your module list in the `config/_default/module.toml` file.

```toml
[[imports]]
path = "github.com/mariox77/hugo-modules/shortcodes/pretty-link"
```

## Shortcode Implementation

Available parameters:

- href: Hugo internal post or external URL

## Customize look and feel

The two files are card layouts for links:

- `layouts/partials/pretty-link/simple-link.html`: A simple link view with Favicon, Title, and Description.
- `layouts/partials/pretty-link/thumbnail-link.html`: A card view with Thumbnail, Title, and Description.

```html
Example1

{{< pretty-link href="https://github.com/blampe/goat" >}}

Example2

{{< pretty-link href="https://tailwindcss.com/docs/object-fit" >}}

Example3

{{< pretty-link href="https://docs.aws.amazon.com/ko_kr/pricing-calculator/latest/userguide/what-is-pricing-calculator.html" >}}

Example4

{{< pretty-link href="/blog/post-2" >}}

Example5

{{< pretty-link href="/blog/post" >}}

Example6

{{< pretty-link href="https://golang-jwt.github.io/jwt/usage/signing_methods/#signing-methods-and-key-types" >}}

Example7

{{< pretty-link href="https://medium.com/@arnaudrinquin/build-modular-application-with-npm-local-modules-dfc5ff047bcc" >}}

Example8

{{< pretty-link href="https://h2s1880.medium.com/ios-android-declarative-ui-programming-%EB%B0%A9%EC%8B%9D%EC%9D%B4-%EA%B0%80%EC%A0%B8%EC%98%A8-%EB%B3%80%ED%99%94%EB%93%A4-f61896275110" >}}

Example9

{{< pretty-link href="https://gohugo.io/functions/transform/htmlunescape/" >}}

Example10

{{< pretty-link href="https://regex101.com/">}}

Example11

{{< pretty-link href="https://firebase.google.com/pricing?hl=ko">}}

Example12

{{< pretty-link href="https://go.dev/" >}}

Example13

{{< pretty-link href="https://ko.wix.com/blog/post/what-is-favicon-how-to-make" >}}
```
