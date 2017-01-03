---
layout: default
---
Back in my days of working as a freelance photographer, I bought the domain name
[mollyrachelbrown.com](http://mollyrachelbrown.com) to showcase my photography
portfolio. I slapped a nice masonry Wordpress theme on top, uploaded some photos,
and called it done. It did the job, but I could never quite escape the feeling that Wordpress
was rather heavy-handed for what I was trying to do. As my focus shifted away from
photography and towards software development, the purpose of my personal site became
confused yet I was unwilling to give up my domain. I procrastinated on what to do with it
for an embarrasingly long time.

Not anymore! Armed with my newly-acquired skills in Ruby and the ability to piece
together a respectable front-end, I've decided to use [Jekyll](https://jekyllrb.com/)
(a static site generator), [Github Pages](https://pages.github.com/), [Skeleton](http://getskeleton.com/)
(a lightweight responsive CSS grid system), and some domain name tweaking to ditch
Wordpress and create my own site pointing to my old custom domain.

Most tutorials on getting up and running with Jekyll assume you are creating a GitHub Pages,
however I had already started a site a few weeks ago. Therefore, my Jekyll install was
as easy as:

{% highlight ruby %}
$ cd path/to/project/
$ gem install jekyll
$ jekyll serve
{% endhighlight %}

That's it! Well, at least in terms of things that has to be installed through the command line.
Once installed, the real work was in re-organizing my existing files to fit the required
Jekyll site structure, which in my case (as of writing this post) looks like this:

{% highlight ruby %}
├── _config.yml
├── _layouts
|   ├── default.html
|   └── post.html
├── _posts
|   ├── 2016-11-13-ruby-classes.md
|   └── 2017-01-02-goodbye-wordpress-hello-jekyll.md
├── _site
├── css
|   ├── normalize.css
|   ├── skeleton.css
|   └── styles.css
├── assets
├── CNAME
└── index.html_
{% endhighlight %}

Once I got the hang of the organizational structure and made the mental connection
that the files in the layouts folder worked very similarly to an .erb partial, the
rest was pretty smooth sailing. It helps that Jekyll has been around for a while and
has great documentation as well in case you get stuck. However, the one major hurdle
I faced came from when accidentally capitalized "layout" in the front matter block
and subsequently spent 30min wondering how I had inexplicably broken things.

{% highlight ruby %}
---
Layout: default #BAD!
layout: default #GOOD!
---
{% endhighlight %}

NEVER AGAIN.

Anyways, once I felt comfortable with things, the last thing for me to do was push my
changes to GitHub Pages and check out my new site. I did it, and this page is proof it
worked! I'm exited to continue refining the look and functionality of the site, and
and equally excited for how easy it is to make changes going forward.
