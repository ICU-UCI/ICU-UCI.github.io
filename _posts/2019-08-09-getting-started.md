---
title: Getting Started
date: 2019-08-09 20:55:00 +0800
categories: [Blogging, Tutorial]
tags: [usage]
comments: false
---


## Basic Environment

First of all, please follow the [Jekyll Docs](https://jekyllrb.com/docs/installation/)  to complete the basic environment (Ruby, RubyGem, Bundler and Jekyll)  installation.

In addition, the [Python](https://www.python.org/downloads/) and [ruamel.yaml](https://pypi.org/project/ruamel.yaml/) are required.

## Configuration

Check out the following files in `_data`:

```
_data/
├── meta.yml
├── profile.yml
└── settings.yml
```

Customize the variables in these files as needed.

## Install Jekyll Plugins

In the root direcoty of the project, run the following command:

```bash
bundle install
```

`bundle` will install all dependent Jekyll Plugins declared in `Gemfile` that stored in the root automatically.

##  Run Locally

Run the script in the root directory of the repository:

```bash
$ bash run.sh
```

>**Note**: Make sure the changes of `_posts` are committed before executing the script. Because the *Recent Update* required the last git log date for the posts.

Open the brower and visit [http://127.0.0.1:4000](http://127.0.0.1:4000) 

##  Publish to GitHub Pages

For security reasons, **GitHub Pages** runs on `safe` mode, which means the third-party Jekyll plugins (e.g. `jekyll-timeago`)  doesn't work, so we have to build locally rather than on GitHub.

There are two basic types of GitHub Pages sites, so you can choose one of them to finish the publishing.

###  User and Organization Pages sites

1) Build your site by:

```bash
$ bash build.sh
```

The build results will be stored in `_site` of the project's root directory.

2) Go to GitHub and create a new repository named `<username>.github.io`.

3) Copy the build results mentioned in **1)** to the new repository.

4) On GitHub, enable Pages service for the new repository.

5) Visit `https://<username>.github.io` and enjoy.

###  Project Pages sites

If you want to put the source code and build results within one repository, the **Project Pages sites** is for you.

> **Note**: Don't name your repository `<username>.github.io` !!

1) Build the site with baseurl `/<projectname>`:

```bash
$ bash build.sh --baseurl=/<projectname>
```

> **Tips**: Setting the variable `baseurl` in `_config.yml` can revoke the parameter option `--baseurl=/<projectname>` above .

2) Create a new branch `gh-pages` and ensure that there are no files in the new branch. Place the site files in folder `_site` into the root directory of the new branch, then push the new branch to the remote `origin/gh-pages`.

3) Go to GitHub website and enable Pages servies for the branch `gh-pages`
of the project.

4) Now your site is published at `https://<username>.github.io/<projectname>/`

## See Also

* [Customize the Favicon]({{ site.baseurl }}/posts/customize-the-favicon/)
* [Write a new post]({{ site.baseurl }}/posts/write-a-new-post/)
* [Text and Typography]({{ site.baseurl }}/posts/text-and-typography/)

<br>

****

[^pages]: [The Categories and Tags Pages for the posts]({{ site.baseurl }}/posts/write-a-new-post/#categories-and-tags) .
[^lastmod]: [Posts' last modified date]({{ site.baseurl }}/posts/write-a-new-post/#last-modified-date) .

