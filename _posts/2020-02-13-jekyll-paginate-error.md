---
layout: post
title:  "jekyll-paginate Dependency Error"
categories: web design
description: A quick solution to the jekyll-pageinate Dependency Error
---

Dependency Error: Yikes! It looks like you don't have jekyll-paginate or one of its dependencies installed. In order to use Jekyll as currently configured, you'll need to install this gem. The full error message from Ruby is: 'cannot load such file -- jekyll-paginate' If you run into trouble, you can find helpful resources at https://jekyllrb.com/help/! 

A quick [search](https://duckduckgo.com/?t=ffab&q=you+don%27t+have+jekyll-paginate&ia=web) will lead you to [StackOverflow](https://stackoverflow.com/questions/35401566/dont-have-jekyll-paginate-or-one-of-its-dependencies-installed).

There, you will find various solutions. The one that worked for me was to simply run the following command to install the Jekyll Paginate gem.

```
gem install jekyll-paginate
```

Once I did that, I was able to rebuild my site and push it to Github.