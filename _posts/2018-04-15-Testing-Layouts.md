---
layout: post
title: "Testing layouts"
excerpt: "The next rabbit hole"
tags: [Jekyll, Formatting, Sass]
modified: 2018-04-15 12:11:00
date: 2018-04-15 12:11:00
author: CleverTwain
comments: true
image:
 feature: function_banner_animated.gif
---
{% include _toc.html %}

## Example Code

```JavaScript
# output as HTML div (using inline CSS styles)
CodeRay.scan('puts "Hello, world!"', :ruby).div

# ...with line numbers
CodeRay.scan("5.times do\n  puts 'Hello, world!'\nend", :ruby).div(:line_numbers => :table)

# output as standalone HTML page (using CSS classes)
CodeRay.scan('puts "Hello, world!"', :ruby).page

# keep scanned tokens for later use
tokens = CodeRay.scan('{ "just": "an", "example": 42 }', :json)

# produce a token statistic
tokens.statistic

# count LoC (lines of code)
CodeRay.scan("# comment\nputs 'Hello, world!'", :ruby).loc  # => 1

# produce a HTML div, but with CSS classes
tokens.div(:css => :class)

# highlight a file (to HTML div); guess the file type base on the extension
CodeRay.highlight_file(__FILE__)

# re-using scanner and encoder with Duo
CodeRay::Duo[:ruby, :div].encode('puts "Hello, world!"')
```

``` powershell
function Get-CleverTwain {
    Start-Process -FilePath 'https://clevertwain.github.io'
}

Get-CleverTwain
```