## Step 1: Configure a collection

Welcome to GitHub Pages with Actions!

GitHub Pages uses a static site generator called Jekyll to transform Markdown files to HTML.  However, there are restrictions within the provided Jekyll environment, including what plugins may be used, and what Jekyll version is used.  

Every time a publishing source branch is pushed to in a repository with GitHub Pages active, a Pages build is triggered.  The Pages build process clones your repository to GitHub's web servers, runs some validations, runs your source files through a Jekyll build, and provides any error messages if necessary.

But did you know that you can actually bypass the Jekyll portion of the Pages build process if you have files that are already in HTML format?  Many developers prefer a more tailored Jekyll environment, or even to build their pages using a different framework entirely, such as with React, Angular, Hugo, or many others.  No matter the framework, pre-building Pages files allows customers more flexibility and control over their development and architecture choices.  

If you're interested in learning how to leverage the power of GitHub Actions to pre-build your files automatically, you're in the right place!

In this course, you'll use Actions to build and deploy a site developed in a Jekyll version that is not supported by Pages.  You will learn how to:

- Evaluate whether to use GitHub Actions-driven Pages builds or the standard (default) Pages build process for your GitHub Pages site
- Research and choose pre-built GitHub Actions from the Marketplace
- Construct and configure a GitHub Action workflow that builds a Jekyll v4.2.0 site and deploys the built files to GitHub Pages



### :keyboard: Activity: Update your Jekyll configuration

Jekyll Collections are a way to group related content.  You will notice that this repository has a folder named `_cats`.  This folder contains a _Jekyll collection_ of Markdown posts about various kitties.  Ordinarily, documents in a collection are sorted by date, or if no date is specified, alphabetically.  But suppose you want to sort the collection in some other way?     

Jekyll versions 4.0 and above now allow you to customize how you want to sort your collection.  The GitHub Pages build process uses Jekyll v3.9, so you will have to build your site using GitHub Actions instead.

First you will configure your custom collection in Jekyll.

1. Navigate to the **Code** tab of this repository, and browse to the `_config.yml` file
2. In the upper right corner, click the ![octicon-pencil] icon to edit the `_config.yml` file
3. Add the following:

```
collections:
  cats:
    output: true
    order:
      - nala-cat.md
      - princess-monster-truck.md
      - jabba-the-fluff.md
      - grumpy-cat.md
```

This will manually order our cats by order of cuteness instead of alphabetically.  We could also sort by a key if we wished.

4. Scroll to the bottom, type a commit message, and commit directly to the `main` branch.

> Once you have pushed your commit, I'll respond in this issue with next steps.

<hr>
<h3 align="center">Look for my next response in this issue.</h3>

[octicon-pencil]: https://unpkg.com/octicons/build/svg/pencil.svg
