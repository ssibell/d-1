---
layout: pages
title: How It Works
permalink: /how-it-works/
---
![](/jekyll.png)
# Welcome
 
The aim of this tutorial is to be a guide to this website. How it works and how to do changes. We’ll cover topics such as getting your site up and running, creating and managing your content like posts, news, documentations and many more. And customizing the way this site works and looks. 

### So what is Jekyll?

Jekyll is a simple, blog-aware, static site generator. It takes a template directory containing raw text files in various formats, runs it through a converter (like Markdown) and our Liquid renderer, and spits out a complete, ready-to-publish static website ```(in _site folder)``` suitable for serving with your web server. Jekyll also happens to be the engine behind GitHub Pages, which means you can use Jekyll to host your project’s page, blog, or website from GitHub’s servers for free.

![](/quick.png)

### How does Jekyll work?

Jekyll actually only does one of a few things to your files, although it classifies files in many different ways. Jekyll either copies, omits or transforms files from your source directory into an output directory```(in _site folder)```.

1. When Jekyll transforms your file, it will always be in the following way, potentially skipping steps. 
2. If a file begins with yaml frontmatter, Jekyll will apply the following transformation to that file:

- liquid templating: liquid template parsing is run on the original content of the file, with several variables, like site or page provided as arguments your liquid templates can access. 
- converting the content: Jekyll asks converters whether they match your file’s extension, e.g. kramdown matches .md, and if so they run against the output from template parsing. Different converters run depending on your file’s extension, e.g. .md extension and the kramdown converter. 
- layout parsing: The output of conversion is passed as the ```content``` variable to either your default layout, or the layout specified in your file’s yaml frontmatter. The output of the layout is written to a file in your output directory, or omitted. Now I want to walk through an example of Jekyll applying this transformation. Later in Jekyll’s core and Testing a complete build we will look at the general structure Jekyll’s algorithm follows and what sorts of files get which treatment.


### Usage
The Jekyll gem makes a jekyll executable available to you in your Terminal window. You can use this command in a number of ways:
```
$ jekyll build
# => The current folder will be generated into ./_site

$ jekyll build --destination <destination>
# => The current folder will be generated into <destination>

$ jekyll build --source <source> --destination <destination>
# => The <source> folder will be generated into <destination>

$ jekyll build --watch
# => The current folder will be generated into ./_site,
#    watched for changes, and regenerated automatically.
```

Jekyll also comes with a built-in development server that will allow you to preview what the generated site will look like in your browser locally.
```
$ jekyll serve
# => A development server will run at http://localhost:4000/
# Auto-regeneration: enabled. Use `--no-watch` to disable.

$ jekyll serve --detach
# => Same as `jekyll serve` but will detach from the current terminal.
#    If you need to kill the server, you can `kill -9 1234` where "1234" is the PID.
#    If you cannot find the PID, then do, `ps aux | grep jekyll` and kill the instance.
```
```
$ jekyll serve --no-watch
# => Same as `jekyll serve` but will not watch for changes.
```

These are just a few of the available configuration options. Many configuration options can either be specified as flags on the command line, or alternatively (and more commonly) they can be specified in a ```_config.yml``` file at the root of the source directory. Jekyll will automatically use the options from this file when run. For example, if you place the following lines in your ```_config.yml``` file:
```
source:      _source
destination: _deploy
```
![](/config.png)

Then the following two commands will be equivalent:
```
$ jekyll build
$ jekyll build --source _source --destination _deploy
```
For more about the possible configuration options, see the configuration page.

## Index file

An HTML file called index.html (by convention) in the site’s root folder and display that as the homepage. Unless the web server you’re using is configured to look for some different filename as the default, this file will turn into the homepage of your Jekyll-generated site.

index file starts with 
```	
---
layout: no-wrapper
---
```

### Controlling the number of posts in main page

There are 3 categories in recent posts.

- Recent Release Notes/ posts
- Recent Updates
- News

Following codes in the index.html will bring the recent posts from each categories.

       <ul class="post-list">
                      {% for post in site.categories.posts limit:5 %}
                        <li>
                          <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

                          <h2>
                            <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
                          </h2>
                          {{ post.excerpt }}
                          <p><a href="{{ post.url | prepend: site.baseurl }}">Read more</a></p>
                        </li>
                      {% endfor %}
                    </ul>
                    
We can control the number of posts display in the main page from there. 


## Includes
The include tag allows you to include the content from another file stored in the ```_includes``` folder:

```{% include footer.html %}```
Jekyll will look for the referenced file (in this case, footer.html) in the _includes directory at the root of your source directory and insert its contents.

There are 3 files in the includes, ```head.html``` ```header.html``` and ```footer.html``` We can easily change this files, the changes will appear in every pages in the website.

![_includes](/includes.png)

## layouts
In Jekyll we can use layouts to eliminate this repetition and make the site easier to maintain.

We have a directory called ```_layouts```. Inside this we have create some html files called blank.html, default.html, no-wrapper.html, page.html and post.html.
![_layouts](/layouts.jpg)

File default.html looks like this:
```
<!DOCTYPE html>
<html lang="en">

  {% include head.html %}

  <body>

    {% include header.html %}

    <div class="page-content">
      <div class="wrapper">
        {{ content }}
      </div>
    </div>

    {% include footer.html %}

  </body>

</html>
```

## Writing posts

The ```_posts``` folder is where your blog posts will live. These files are generally Markdown or HTML, but can be other formats with the proper converter installed. All posts must have YAML Front Matter, and they will be converted from their source format into an HTML page that is part of your static site.

### Creating Post Files

To create a new post, all you need to do is create a file in the ```_posts``` directory, either in News, or updates or Posts. How you name files in this folder is **important**. Jekyll requires post files to be named according to the following format:
```
YEAR-MONTH-DAY-title.MARKDOWN
YEAR-MONTH-DAY-title.md
```
Where YEAR is a four-digit number, MONTH and DAY are both two-digit numbers, and MARKUP is the file extension representing the format used in the file. For example, the following are examples of valid post filenames:
Examples: 
```
2011-12-31-new-years-eve-is-awesome.md
2012-09-12-how-to-write-a-blog.md
```
And every markdown file should shart like this if it in the news category:
```
---
layout: post
title:  "dCache 3.16"
date:   2017-09-04 10:27:23
author: Asif Mohiuddin
excerpt: dCache updates
category: news
---
```

## Where to configure permalinks

You can configure your site’s permalinks through the Configuration file or in the Front Matter for each post, page, or collection.

Setting permalink styles in your configuration file applies the setting globally in your project. You configure permalinks in your ```_config.yml``` file like this:

```permalink: /:categories/:year/:month/:day/:title.html```
If you don’t specify any permalink setting, Jekyll uses the above pattern as the default.

The permalink can also be set using a built-in permalink style:

```permalink: date```
``` date``` is the same as ```:categories/:year/:month/:day/:title.html```, the default. See Built-in Permalink Styles below for more options.

Setting the permalink in your post, page, or collection’s front matter overrides any global settings. Here’s an example:
```
---
title: My page title
permalink: /mypageurl/
---
```
Even if your configuration file specifies the ```date``` style, the URL for this page would be ```http://somedomain.com/mypageurl/```.

When you use permalinks that omit the .html file extension (called “pretty URLs”) Jekyll builds the file as index.html placed inside a folder with the page’s name. For example:
```
├── mypageurl
│   └── index.html
```
With a URL such as ```/mypageurl/```, servers automatically load the index.html file inside the folder, so users can simply navigate to ```http://somedomain.com/mypageurl/``` to get to ```mypageurl/index.html```.

### Where additional pages live

Where you put HTML or Markdown files for pages depends on how you want the pages to work. There are two main ways of creating pages:

Place named HTML or Markdown files for each page in your site’s root folder. Place pages inside folders and subfolders named whatever you want. Both methods work fine (and can be used in conjunction with each other), with the only real difference being the resulting URLs. By default, pages retain the same folder structure in _site as they do in the source directory.

### Named HTML files

The simplest way of adding a page is just to add an HTML file in the root directory with a suitable name for the page you want to create. For a site with a homepage, an about page, and a contact page, here’s what the root directory and associated URLs might look like:

    .
    |-- _config.yml
    |-- _includes/
    |-- _layouts/
    |-- _posts/
    |-- _site/
    |-- about.html    # => http://example.com/about.html
    |-- index.html    # => http://example.com/
    |-- other.md      # => http://example.com/other.html
    └── contact.html  # => http://example.com/contact.html If you have a lot of pages, you can organize those pages into subfolders. The same subfolders that are used to group your pages in our project’s source will exist in the _site folder when your site builds.
Flattening pages from subfolders into the root directoryPermalink

If you have pages organized into subfolders in your source folder and want to flatten them in the root folder on build, you must add the permalink property directly in your page’s front matter like this:

	---
	title: My page
	permalink: mypageurl.html
	---
  
### Named folders containing index HTML files

If you don’t want file extensions (.html) to appear in your page URLs (file extensions are the default), you can choose a permalink style that has a trailing slash instead of a file extension.

Note if you want to view your site offline without the Jekyll preview server, your browser will need the file extension to display the page, and all assets will need to be relative links that function without the server baseurl.



# An overview of what each of these does:

<div class="mobile-side-scroller">
<table>
  <thead>
    <tr>
      <th>File / Directory</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <p><code>_config.yml</code></p>
      </td>
      <td>
        <p>
          Stores configuration data. Many of
          these options can be specified from the command line executable but
          it’s easier to specify them here so you don’t have to remember them.
        </p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>_includes</code></p>
      </td>
      <td>
        <p>
          These are the partials that can be mixed and matched by your layouts
          and posts to facilitate reuse. The liquid tag
          <code>{% raw %}{% include file.ext %}{% endraw %}</code>
          can be used to include the partial in
          <code>_includes/file.ext</code>.
        </p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>_layouts</code></p>
      </td>
      <td>
        <p>
          These are the templates that wrap posts. Layouts are chosen on a
          post-by-post basis in the
          YAML Front Matter,
          which is described in the next section. The liquid tag
          <code>{% raw %}{{ content }}{% endraw %}</code>
          is used to inject content into the web page.
        </p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>_posts</code></p>
      </td>
      <td>
        <p>
          Your dynamic content, so to speak. The naming convention of these
          files is important, and must follow the format:
          <code>YEAR-MONTH-DAY-title.MARKUP</code>.
          The permalinks can be customized for
          each post, but the date and markup language are determined solely by
          the file name.
        </p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>_sass</code></p>
      </td>
      <td>
        <p>
          These are sass partials that can be imported into your <code>main.scss</code>
          which will then be processed into a single stylesheet
          <code>main.css</code> that defines the styles to be used by your site.
        </p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>_site</code></p>
      </td>
      <td>
        <p>
          This is where the generated site will be placed (by default) once
          Jekyll is done transforming it. It’s probably a good idea to add this
          to your <code>.gitignore</code> file.
        </p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>.jekyll-metadata</code></p>
      </td>
      <td>
        <p>
          This helps Jekyll keep track of which files have not been modified
          since the site was last built, and which files will need to be
          regenerated on the next build. This file will not be included in the
          generated site. It’s probably a good idea to add this to your
          <code>.gitignore</code> file.
        </p>
      </td>
    </tr>
    <tr>
      <td>
        <p><code>index.html</code> or <code>index.md</code> and other HTML,
        Markdown, Textile files</p>
      </td>
      <td>
        <p>
          Provided that the file has a YAML Front
          Matter section, it will be transformed by Jekyll. The same will
          happen for any <code>.html</code>, <code>.markdown</code>,
          <code>.md</code>, or <code>.textile</code> file in your site’s root
          directory or directories not listed above.
        </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>Other Files/Folders</p>
      </td>
      <td>
        <p>
          Every other directory and file except for those listed above—such as
          <code>css</code> and <code>images</code> folders,
          <code>favicon.ico</code> files, and so forth—will be copied verbatim
          to the generated site. 
        </p>
      </td>
    </tr>
  </tbody>
</table>
