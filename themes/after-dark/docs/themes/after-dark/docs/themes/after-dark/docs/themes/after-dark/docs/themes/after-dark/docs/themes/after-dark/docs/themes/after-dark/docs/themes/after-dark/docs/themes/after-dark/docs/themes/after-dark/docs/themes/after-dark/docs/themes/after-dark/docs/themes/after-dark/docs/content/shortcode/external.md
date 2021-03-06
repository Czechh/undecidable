+++
title = "External"
description = "Create links with SVG icon and custom behavior."
categories = ["navigation"]
tags = ["links", "security", "privacy"]
html_attributes = ["href", "class", "referrerpolicy", "target", "type", "rel"]
custom_attributes = []
snippets_used = ["external", "button"]
+++

Basic usage:

```html
{{</* external text="After Dark" href="https://after-dark.habd.as" /*/>}}
{{</* external href="https://after-dark.habd.as" /*/>}}
```

{{< external text="After Dark" href="https://after-dark.habd.as" />}}
{{< external href="https://after-dark.habd.as" />}}

```
{{</* external "https://go.habd.as/after-dark" /*/>}}
{{</* external "wss://fs1.habd.as:80" /*/>}}
```

{{< external "https://go.habd.as/after-dark" />}}
{{< external href="wss://fs1.habd.as:80" />}}

With external link styling removed:

```html
{{</* external rel="noopener" href="https://keybase.io/jhabdas" /*/>}}
```

{{< external rel="noopener" href="https://keybase.io/jhabdas" />}}

With internal link opening in a new window:

```html
{{</* external href="/404.html" text="Error Page" /*/>}}
```

{{< external href="/404.html" text="Error Page" />}}

With structured data type:

```html
{{</* external itemtype="significantLink" href="https://habd.as" /*/>}}
```

{{< external itemtype="significantLink" href="https://habd.as" />}}

With site-wide [Referrer Policy](/feature/referrer-policy) overridden:

```html
{{</* external referrerpolicy="unsafe-url" href="http://goo.gl" /*/>}}
```

{{< external referrerpolicy="unsafe-url" href="http://goo.gl" />}}

With markdown image and link styling removed:

```markdown
{{%/* external rel="next" href="https://source.unsplash.com/collection/983219/2160x1440" %}}
  ![Example image](https://source.unsplash.com/collection/983219/1080x720 "View Random Image Enlarged")
{{% /external */%}}
```

{{% external rel="next" href="https://source.unsplash.com/collection/983219/2160x1440" %}}
  ![Example image](https://source.unsplash.com/collection/983219/1080x720 "View Random Image Enlarged")
{{% /external %}}

With interactive [Button](../button) to run a [Fuzzy Search](/feature/fuzzy-search):

```html
{{</* external rel="search" target="_self" href="/search/?s=button" >}}
  {{< hackcss-button type="primary" text="Search" />}}
{{< /external */>}}
```

{{< external rel="search" target="_self" href="/search/?s=button" >}}
  {{< hackcss-button type="primary" text="Search" />}}
{{< /external >}}
