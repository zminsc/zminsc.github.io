---
title: code highlighting in jekyll
layout: article
---

**TL;DR**: Surround your code snippet in highlight tags ({% raw %}`{% highlight %}` and `{% endhighlight %}`{% endraw %}). Install a stylesheet from [this repository](https://github.com/jwarby/jekyll-pygments-themes) and link it. Voilà, you've got code highlighting. And always remember to read the documentation.

Wanting to include code snippets in my posts, I took to Google and searched "code highlighting jekyll". The first result, a StackOverflow post, proposed I use `highlight` tags like so:

{% highlight markdown %}
{% raw %}
{% highlight python %}

# put my code snippet here

{% endhighlight %}
{% endraw %}
{% endhighlight %}

This did nothing. In fact, methods described in several other StackOverflow posts -- editing my `Gemfile`, `_config.yml`, and so on -- all failed. An hour later and ready to give up, I switched off of StackOverflow and landed on... [Jekyll's official documentation for code highlighting](https://jekyllrb.com/docs/liquid/tags/). In fact, this should have been my first destination. The age-old adage of **READ THE DOCUMENTATION** that I had so often preached, I had completely ignored myself.

Indeed, I was to surround my code snippets with `highlight` tags, as the first StackOverflow post suggested. However, I had missed a crucial detail: "In order for the highlighting to show up, you’ll need to include a highlighting stylesheet." So in addition to the highlight tags, I needed to install or provide a stylesheet and link it appropriately. I downloaded [tango](https://github.com/jwarby/jekyll-pygments-themes/blob/master/tango.css) and `@use`'d it in my `style.css` file. You can find a sample code snippet in Python styled this way in [fibonacci pytest]({% post_url 2024-01-07-fibonacci-pytest %}).
