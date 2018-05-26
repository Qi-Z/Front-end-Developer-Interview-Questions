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
  * What are the exceptions?
* Name 3 ways to decrease page load (perceived or actual load time).
* If you jumped on a project and they used tabs and you used spaces, what would you do?
* Describe how you would create a simple slideshow page.
* If you could master one technology this year, what would it be?
* Explain the importance of standards and standards bodies.
* What is Flash of Unstyled Content? How do you avoid FOUC?
* Explain what ARIA and screenreaders are, and how to make a website accessible.
* Explain some of the pros and cons for CSS animations versus JavaScript animations.
* What does CORS stand for and what issue does it address?
