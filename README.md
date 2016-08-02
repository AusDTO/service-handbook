# Service Handbook

This is a single place for the DTO's guides to Discovery, Alpha and onwards to be published. It supercedes the previous discovery-guide repository.

The guide is written in Markdown and is managed through this GitHub repository.

## Making a change to this guide

To propose a change to this guide, you first need to [create a GitHub account](https://github.com/join).

Once you're signed in, you can browse through the folders above and choose the content you're looking for. You should then see the content in Markdown form. Click the Edit icon in the top-right corner to start editing the content.

![](https://raw.githubusercontent.com/AusDTO/service-handbook/gh-pages/_docs/edit-link.png)

The content is written in the Markdown format. [There's a guide here on how to get started with it](https://guides.github.com/features/mastering-markdown/).

You can preview your changes using the tabs at the top of the editor.

When you're happy with your change, make sure to create a pull request for it using the options at the bottom of the page. You'll need to write a short description of the changes you've made.

![](https://raw.githubusercontent.com/AusDTO/service-handbook/gh-pages/_docs/opening-pull-request.png)

A pull request is a proposal for a change to the content. Other people can comment on the change and make suggestions. When your change has been reviewed, it will be "merged" - and it will appear immediately in the published content.

Take a look at [this guide on GitHub about pull requests](https://help.github.com/articles/using-pull-requests/).

### Checking the guide for broken links, invalid HTML, and overall completeness

Before proposing changes, we'd appreciate you checking that all the links are correct, and the guide is valid and complete HTML.
We use [html-proofer](https://github.com/gjtorikian/html-proofer) to automatically check the guide for us.
If you've forked our github repository, html-proofer is already configured, but you'll need to follow a few simple steps to get it going:

**1. Use bundler to manage your dependencies**

We use [bundler](http://bundler.io/) to handle configuration and dependency management for our guides. We think it's fantastic and can't recommend it enough. It's powerful and simple to use:

 > $ bundle install


**2. Use jekyll to generate a version of the site that html-proofer can check**

We deploy our guides on github-pages, under a directory name corresponding to the guide, in this case 'ausdto.github.io/**service-handbook**/'.

The links jekyll generates expect the site to be hosted under a directory called 'service-handbook', and you'll need to instruct jekyll to do that for you before html-proofer will work

 > $ bundle exec jekyll build -d \_site/service-handbook/

**3. Run html-proofer over your generated jekyll site**

html-proofer will check all the internal and external links exist, examine your html is valid, and ensure that good practices are followed, like having alt tags for images.

> $ bundle exec htmlproofer ./_site

#### Automating html-proofer

Internally, we use [Travis-ci](https://travis-ci.org/) to automatically run html-proofer whenever we commit to the guide. If you're making lots of changes, or building your own guide, we think you should investigate using Travis.
