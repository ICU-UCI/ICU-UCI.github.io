---
title: "Text and Typography"
date: 2019-08-08 11:33:00 +0800
categories: [Blogging, Tutorial]
tags: [typography]
comments: false
---

This Jekyll template totally compatible with Markdown syntax. Now, let me show you what typography will looks like.

## Titles

***
# H1

<h2 data-toc-skip>H2</h2>

<h3 data-toc-skip>H3</h3>

#### H4

***

## Paragraph

I wandered lonely as a cloud

That floats on high o'er vales and hills,

When all at once I saw a crowd,

A host, of golden daffodils;

Beside the lake, beneath the trees,

Fluttering and dancing in the breeze.

## Block Quote

> This line to shows the Block Quote.

## Tables

|Company|Contact|Country|
|:---|:--|---:|
|Alfreds Futterkiste | Maria Anders | Germany
|Island Trading | Helen Bennett | UK
|Magazzini Alimentari Riuniti | Giovanni Rovelli | Italy

## Link

[http://127.0.0.1:4000](http://127.0.0.1:4000)


## Footnote

Click the hook will locate the footnote[^footnote].


## Image

![Desktop View]({{site.baseurl}}/assets/img/sample/mockup.jpg)


## Inline code

This is an example of `Inline Code`.


## Code Snippet

Markdown <code class="highlighter-rouge">```</code> can easily create a code block as following examples.

### Ruby

```ruby
def sum_eq_n?(arr, n)
  return true if arr.empty? && n == 0
  arr.product(arr).reject { |a,b| a == b }.any? { |a,b| a + b == n }
end
```

### Shell

```shell
if [ $? -ne 0 ]; then
    echo "The command was not successful.";
    #do the needful / exit
fi;
```

### Liquid

If you want to display the **Liquid** snippet, surround the liquid code with `{% raw %}{%{% endraw %} raw {%raw%}%}{%endraw%}` and `{% raw %}{%{% endraw %} endraw {%raw%}%}{%endraw%}` .

{% highlight liquid %}
{% raw %}
{% if product.title contains 'Pack' %}
  This product's title contains the word Pack.
{% endif %}
{% endraw %}
{% endhighlight %}


### Line Number

The Line number of Code Snippet is not displayed by default. To enable it, you should make your code surrounded with `{% raw %}{%{% endraw %} highlight LANGUAGE linenos {% raw %}%}{% endraw %}` and `{% raw %}{%{% endraw %} endhighlight {% raw %}%}{% endraw %}`

**No Scrolling**

{% capture _code %}
{% highlight html linenos %}
<div class="sidenav">
  <a href="#contact">Contact</a>
  <button class="dropdown-btn">Dropdown
    <i class="fa fa-caret-down"></i>
  </button>
  <div class="dropdown-container">
    <a href="#">Link 1</a>
    <a href="#">Link 2</a>
    <a href="#">Link 3</a>
  </div>
  <a href="#contact">Search</a>
</div>
{% endhighlight %}
{% endcapture %}{% include fixlinenos.html %}{{ _code }}

**Horizontal Scrolling**

{% capture _code %}
{% highlight html linenos %}
<div class="panel-group">
  <div class="panel panel-default">
    <div class="panel-heading" id="{{ category_name }}">
      <i class="far fa-folder"></i>
      <p>This is a very long long long long long long long long long long long long long long long long long long long long long line.</p>
      </a>
    </div>
  </div>
</div>
{% endhighlight %}
{% endcapture %}{% include fixlinenos.html %}{{ _code }}

<br>

***

[^footnote]: The footnote source.


