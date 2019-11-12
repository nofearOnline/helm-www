![github-banner-helm-helmwww](https://user-images.githubusercontent.com/686194/68531441-f4ad4e00-02c6-11ea-982b-74d7c3ff0071.png)


This is where you'll find all of the assets that make up [helm.sh](https://helm.sh/), the website for the [Helm](https://github.com/helm/helm) project. If you'll looking to edit docs, report a website bug or write a new blog post, you've come to the right place!


## Development

Helm.sh is a simple [Hugo](https://gohugo.io/) static site, built with a custom theme. To run the website locally, you'll need to first [install](https://gohugo.io/getting-started) Hugo and any dependencies.

```
brew install hugo
yarn install
```

You can then compile and run the site locally:

```
hugo serve
```

## Deployment [![Netlify Status](https://api.netlify.com/api/v1/badges/8ffabb30-f2f4-45cc-b0fa-1b4adda00b5e/deploy-status)](https://app.netlify.com/sites/helm-merge/deploys)

Changes are automatically deployed to [Netlify](https://app.netlify.com/sites/helm-merge/deploys) when merged to master. Build logs can be found [here](https://app.netlify.com/sites/helm-merge/deploys).


---

## Contributing

Anyone can submit a PR to edit Helm.sh. We require commits be signed - please refer to the [contributing guide](https://github.com/helm/helm/blob/master/CONTRIBUTING.md#sign-your-work).

Pull requests require [maintainer](https://github.com/helm/helm-www/blob/master/OWNERS) approval before merge.


### How to Edit The Helm Docs

Since the release of Helm 3, all project documentation is located in this repo under `content/docs/`. 

For earlier versions, see the `dev-v2` branch of the main Helm repo [here](https://github.com/helm/helm/tree/dev-v2/docs).


### How to Write a Blog Post

Blog posts are created via pull requests. The following steps are used to add them:

1) Add a new file to the `content/blog/` directory whose name is the published date and the title. The files must be markdown formatted. See the existing titles for examples of the format
2) Add the header meta-data to the file using this format (note the permalink structure). Recommended but optional fields are `authorname` which should be name(s); these are displayed verbatim. `authorlink` is the link used by `authorname`.
```yaml
---
title: "A Fancy Title"
slug: "fancy-title"
authorname: "Captain Awesome"
authorlink: "https://example.com"
date: "yyyy-mm-dd"
---
```
3) Add the content below the `---` as Markdown. The title does not need to be included in this section
4) Any images should be placed in the `/img/blog/` directory. Images should be losslessly compressed to reduce their size. Tools, such as [ImageOptim](https://imageoptim.com/), can be used.
5) To summarize the content on the blog index page, insert a `<!--more-->` break in your markdown. This will truncate the content with a _Read More_ link.

Blog PRs require approval from the core Helm [maintainers](https://github.com/helm/helm/blob/master/OWNERS) before merge.

---

### Code of Conduct
Participation in the Helm community is governed by the Helm [Code of Conduct](https://github.com/helm/helm/blob/master/code-of-conduct.md).

### Thank You!
We appreciate your contributions to our website and our documentation! :clap: