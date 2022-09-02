---
title: What I wish I’d known about website builders
layout: page
exclude: true
---

*Daniel Jackson*<br>
*August 31, 2022*

Static website builders like Jekyll and Hugo are handy and relatively easy to use. Once you get the hang of it, you save a ton of work and you can concentrate on your content and rarely ever look at any HTML or CSS. 

But learning the basics is much harder than it needs to be. The problem—as with a lot of software—is that the documentation (and even the starter tutorials) don’t seem to explain the most fundamental ideas, maybe because they assume you already know them. Either way, if you don’t, you end up having to infer the most basic stuff by reading between the lines.

So here’s a quick intro that explains some fundamentals. It’s what I wish I’d been able to read when I started. I’m writing this for my students in our Software Studio class, and it’s very far from what it could be, but hopefully some others will jump in and help improve it.

This intro is organized around the main concepts that you need to understand to use a static website builder. It doesn’t give you any syntax or specifics, but it does include some pointers. My hope is that this will give you the background you need to be able to use the more detailed documentation effectively, and without feeling quite so lost.

## Static website
First, what exactly is a static website? In short, it’s a website that has the property that users who access it through their browsers can only read the content of the site, and never write it (that is, update it). So every user sees the same site.

This doesn’t mean that the site can’t use dynamic code, but that code can only be JavaScript that executes in the browser. The pages themselves are just files that are served up by the web server.

More importantly, being static doesn’t mean that the site doesn’t change over time. Almost all static sites are frequently modified. What makes them static is that the modification happens by the site owner replacing the files on the server. A common way to do this is to place the files in a repo, and have the web server serve them directly from the repo. This is how GitHub Pages works. And because all the members of a team that have access to a repo can update it, this means that you can have a site that is maintained by a community. 

Content management systems (like Drupal or Wordpress) are similar, in that they typically have a larger population of viewers and a smaller group of users who modify the site. But with static websites, you edit the pages through conventional file editing mechanisms, and with CMSs you edit the files through the website itself (usually by switching to an editing mode). And in content management systems, the content is typically stored in a database, and not as plain files in the file system.

## Website builder

A static website builder is a tool that makes it easier to create and maintain a static website. It works by offering a special structure and language for expressing the website, which it then translates into standard HTML and CSS. So the general pattern is that you (a) write content in the special structure and language; (b) run the website builder to generate HTML and CSS; (c) deploy the website by moving the files to the server’s workspace.

Now onto the main concepts that enable website builders.

## Markdown

Markdown is a language for formatted documents that offers short and convenient syntax for marking text as headings, bullet points, bold/italic, etc., and for links and image insertions. Markdown is used as a source format in a variety of contexts, but is most commonly translated into HTML. 

Static website builders typically use markdown as the primary source language. There are several markdown variants, and you can often choose which variant you prefer in the configuration file.

When you need to express something that isn’t expressible in markdown, it’s usually possible to just write plain HTML, which will then be inserted at the appropriate place in the generated HTML.

## Template

A template is a file written in an extension of HTML that includes commands that generate HTML from the values of certain variables in scope. Templates are used by web frameworks for generating the pages that are returned by web requests; you can think of a template as a function from an environment (a collection of bindings of variables) to an HTML page. For example, a template might include the text

	Welcome, <b>{{name}}</b>!

This includes some standard HTML (eg, the bold tag) but also some special templating text, which is demarcated by the curly braces. Roughly speaking, templating text is treated as an expression to be evaluated. So in this case, the web app has presumably assigned to the variable *name* the string representing the user’s name.

Templating features typically include the ability to iterate over collections (that is, producing an HTML element for each member of the collection), conditionals, string processing functions (such as escaping or changing case), and so on.

There are many different templating languages, and most are based on a particular programming language and use its syntax for expressions and control flow. Jekyll uses Ruby, for example; Hugo uses Go.

## Layout
In the context of a static website builder, templates are called “layouts,” and they play a prominent role. Each layout is a file that holds a recipe for generating a particular kind of page. For example, there will be a layout for the home page, a layout for an index of posts, and a layout for posts themselves.

Each page of the generated site is produced by interpreting one layout. The input to the layout is either a single source file written by the user (this is how the layout for the home page or a single post is applied), or a collection of files (this is how the layout for the index page for all posts is applied). The choice of which layout is applied is generally set by default depending on the kind of page and its location in the directory structure, but can also usually be set manually.

## Front matter

You may be wondering: if a layout is just a template, and template is evaluated in the context of an environment binding values to variables, then how come a layout is applied to a *source file*?

Here’s the answer. Each source file implicitly generates an environment. The body of the source file, which is usually written in markdown, is automatically converted into HTML, which is bound to a special variable (typically with the name *content*).

Every source file also has a section at the top which includes a list of metadata fields and their values. For example, every post in a blog would have a title:

	title: "My first blog post"

Those metadata fields comprise what is known as the page’s *front matter*. They are compiled into an environment, so that the variable *title*, for example, can be accessed in the layout and will evaluate to the string specified.

The environment in which a layout is evaluated is actually a global environment (of metadata specified in a configuration file) extended with the environment produced from the front matter. The variables in the global environment are typically accessed using a special prefix. For example, *site.title* might refer to the title of the entire website, which is different from *title*, which refers to the title of this particular post.

## Partial

One of the strange things about HTML is that it’s never offered a simple way to include one HTML file in another. So, for example, if you want to have some HTML for a nav bar that is included on every page in your website, there is no easy way to do that. 

But layouts are not regular HTML, so they offer this feature: you can insert one layout into another. A layout that is intended to represent just part of a page and not a whole page is called a *partial*. For example, there will generally be a partial for the header and one for the footer. Partials can themselves be constructed from partials, so there’s a nice hierarchy of structural components. 

There are two benefits from having this tree structure. First, it eliminates repetition: you can define what goes in your header in just one place, for example. Second, static website builders let you place partials in a special directory that represent theme overrides. The way these work is that when a particular partial is called for, the website builder first looks for it by name in the special directory, and if it’s missing, finds it in the theme directory (see below). This let’s you override individual pieces of a layout. You may, for example, want to keep everything about how your them chooses to lay out the home page except for the way the copyright is shown at the bottom. Rather than modifying a layout for the whole page, you can modify just the footer (and make just a copyright partial)—and by using an overriding copy, you never have to actually modify the theme itself.

## Collection

For the most part, you place your source files in a directory hierarchy, and the generated HTML files will have paths that follow that structure (just like pathnames in Unix).

There are three exceptions to this:
- You can change the URL associated with a page, often in the front matter, or in a top-level configuration file.
- Certain directory names, file names and structures are predefined, and you’re not free to change them.
- A key concept in static site builders is that of a *collection*, in which a bunch of files are treated as members of a set.

Here’s how collections work. You identify a particular directory as containing a collection, either in the top-level configuration file, or by some convention in the directory name or structure. Every file in that directory then becomes a member of the collection, and the collection can be referred to by a variable of the appropriate name.

For example, if you create a directory that corresponds to a collection called *articles* then the variable *articles* would represent a set you could iterate over in a template, for example to generate an indexed listing of all the articles and their titles.

## Theme

Static site builders are useful because they separate two very different tasks: creating content, and laying out the context with HTML and CSS (and maybe JavaScript too). 

Most users of a static site builder only want to create content. Building the layouts is tricky and requires considerable effort, with coding in all the languages involved (HTML, CSS and the templating language), and graphic design to ensure that the site looks good, is responsive, etc. So typically the layouts are created by experts and are packaged into *themes*.

As a content creator, all you need to do is pick a theme and write your content. You can tweak the theme by overriding a partial (as explained above) or by adding some CSS rules.

It would be nice if there were a complete separation of style and content, so that you could change theme without changing the source files. Unfortunately this is rarely the case because themes typically make assumptions about the structure and names of directories, and they also require particular metadata fields to be defined in the global configuration file and in front matter. So pick your theme carefully, and make sure it not only has a look that you like but also that it includes the features you are likely to want down the line, and has enough users that it’s unlikely to have debilitating bugs.
