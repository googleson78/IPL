# Implementation of Programming Languages

This is the code of the website of a course on implementing a programming
language. The website is hosted at https://sofiacpp.github.io/IPL.

## Working with the website

The website is deployed as GitHub pages from the contents of the gh-pages branch
of this repository.


### Requirements

- Git and Git-Bash on Windows
- [hugo](https://gohugo.io)

### Checking out the code

Simply clone this repository.

### Setting up the clone

1. Make sure that `git` and `hugo` are in the path
2. Add the gh-pages as a *git worktree* under the public folder

        git fetch origin gh-pages:gh-pages
        git branch --set-upstream-to=origin/gh-pages gh-pages
        git worktree add public gh-pages

### Creating new content

#### Creating new posts

The normal hugo way of creating new posts applies

    hugo new content/posts/post.md
    hugo new content/page/page.md

#### Creating new slides

Creating new slides requires using a different template. You can use the
*content/slides* as boilerplate.

    cp -R content/slides/template content/slides/myslides
    edit content/slides/myslides/_index.md

### Checking out changes

Run

    hugo serve -D -F

to checkout the website locally with drafts (*-D*) and future articles (*-F*).
The `hugo` server will watch for changes and automatically reload the browser
tab.

### Publishing changes

1. Make any changes to the content and **COMMIT**
2. Run the publish.sh script

        sh publish.sh

    It will generate the new version inside the *public* folder, commit and push
    it.
