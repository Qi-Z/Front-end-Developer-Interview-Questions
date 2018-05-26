# General Questions:

* What did you learn yesterday/this week?

Angular Change Detection, ReactJS, GraphQL

* What excites or interests you about coding?

The ability to implement something fun

* What is a recent technical challenge you experienced and how did you solve it?

Reusable components design. Solved by discussing with peers and reading outstanding open source reusable components

* When building a new web site or maintaining one, can you explain some techniques you have used to increase performance?

First page load with server side rendering

CDN

Image compression

Lazy loading (defer loading) of JS, Images

Uglify

Minify

Caching

* Can you describe some SEO best practices or techniques you have used lately?
* Can you explain any common techniques or recent issues solved in regards to front-end security?

XSS: Escape input from users

CSRF: using cookie (Angular HttpClient module)


* What actions have you personally taken on recent projects to increase maintainability of your code?

Auto documatation tool: CompoDoc

Comments

Self explainatory naming

* Talk about your preferred development environment.
Mac

WebStorm

Terminal

POSTman

Chrome

Chrome Dev Tools

Chrome Extensions



* Which version control systems are you familiar with?

Git
```bash
git clone
git pull
git add
git commit
git push

git rebase
git merge

git checkout

git branch -b
git branch
```

* Can you describe your workflow when you create a web page?

Write basic html, link js, link CSS

Start up a server with npm http-server package or any others

If SPA, follow CLI or official tutorial on creating SPA


* If you have 5 different stylesheets, how would you best integrate them into the site?

Multiple CSS files cause longer round-trip time

inline, internal, external

External (Advantage of Caching)

Combine into one

https://varvy.com/pagespeed/optimize-css-delivery.html

`<link>`

Served over CDN

* Can you describe the difference between progressive enhancement and graceful degradation?

Graceful Degradation: downgrade

Progressive enhancement: kinda like mobile first design (responsive)

* How would you optimize a website's assets/resources?

  * Assets
    * Images
      1. Optimize image (resolution)
      2. CSS sprites for icons, reduce network request
    

gzip (although other algorithm accepptable like Brotli)

CDN

Caching

name the assets

* How many resources will a browser download from a given domain at a time?

https://stackoverflow.com/questions/7456325/get-number-of-concurrent-requests-by-browser

https://blog.octo.com/en/http2-arrives-but-sprite-sets-aint-no-dead/

```
There are a lot of things to consider here. In most situations, I would only choose one cookieless domain/subdomain to host your images such as static.mywebsite.com. And ideally static files should be hosted by a CDN, but that's another story.

First of all, IE7 allowed only two concurrent connections per host. But most browsers today allow more than that. IE8 allows 6 concurrent connections, Chrome allows 6, and Firefox allows 8.

So if your web page only has 6 images, for example, then it'd really be pointless to spread your images across multiple subdomains.

So let's say you have 24 images on a page. Well, few things in life are free and there's such a thing as death by parallelization. If you host your images in 4 different subdomains, then that means that every single image could theoretically be downloaded in parallel. However, it also means that there are 3 additional DNS lookups involved. And a DNS lookup could be 100 ms, 150 ms, or sometimes longer. This added delay could easily offset any benefit of parallel downloads. You can see real-world examples of this by testing sites with http://www.webpagetest.org/

Of course the best solution is to use CSS sprites when possible to cut down on the number of requests. I talk about that and the inherent overhead of every request in this article and this one.

UPDATE

There's an interesting article from Steve Souders on the subject of sharding domains...

Most of the U.S. top ten web sites do domain sharding. YouTube uses i1.ytimg.com, i2.ytimg.com, i3.ytimg.com, and i4.ytimg.com. Live Search uses ts1.images.live.com, ts2.images.live.com, ts3.images.live.com, and ts4.images.live.com. Both of these sites are sharding across four domains. What’s the optimal number? Yahoo! released a study that recommends sharding across at least two, but no more than four, domains. Above four, performance actually degrades.

http://www.stevesouders.com/blog/2009/05/12/sharding-dominant-domains/

Note however that this was written in 2009. And in 2011 he posted a comment...

Since newer browsers open more connections per domain, it’s probably better to revise the number downwards. I think 2 is a good compromize, but that’s just a hunch. It’d be great if some production property ran a test to determine the optimal number.

You should also keep in mind that the big reason it's even necessary for the big sites like Yahoo and Amazon to do domain sharding is that their sites are so dynamic. The images are attached to products or stories which are displayed dynamically. So it's not feasible for them to use CSS sprites as aggressively as would be optimal.

A site like StackOverflow, however, is light on these sorts of images and they have cut down on the number of requests so much that they don't need to do sharding. A big step towards making that happen is their usage of this sprites.png image...

http://cdn.sstatic.net/Sites/stackoverflow/img/sprites.png?v=5

UPDATE #2

Steve Souders posted another update on domain sharding. He repeats much of what I've already mentioned. But the thing that stood out was SPDY and how that should affect your decision.

Perhaps the strongest argument against domain sharding is that it’s unnecessary in the world of SPDY (as well as HTTP 2.0). In fact, domain sharding probably hurts performance under SPDY. SPDY supports concurrent requests (send all the request headers early) as well as request prioritization. Sharding across multiple domains diminishes these benefits. SPDY is supported by Chrome, Firefox, Opera, and IE 11. If your traffic is dominated by those browsers, you might want to skip domain sharding.

UPDATE #3 (February 2018)

As Dean mentioned in the comments below, CSS sprites aren't really buying you very much now with HTTP/2 being supported in modern browsers. But you do have to get an SSL certificate, set up your site to work with HTTPS, and ensure your web server is configured for HTTP/2. Either that, or use a CDN that already has all of that set up for you. Once you've done all of that then you can probably skip both CSS sprites and domain sharding.
```
  * What are the exceptions?
* Name 3 ways to decrease page load (perceived or actual load time).
  * Prune CSS (Remove unused CSS)
  * minify JS
  * Optimize images (never scale down. If we have 700 x 700 png, don't scale down, make a 100 x 100 png instead)
  * Reduce HTTP requests
* If you jumped on a project and they used tabs and you used spaces, what would you do?

Follow the rules.

* Describe how you would create a simple slideshow page.

Load all images in DOM if not many

set CSS hidden

Set prev and next buttons

Add JS

* If you could master one technology this year, what would it be?

ReactJS

* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
* Explain what ARIA and screenreaders are, and how to make a website accessible.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
* What does CORS stand for and what issue does it address?
