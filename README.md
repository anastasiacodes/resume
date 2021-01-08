# Anastasia Powell's Resume

[![Netlify Status](https://api.netlify.com/api/v1/badges/636d486d-dea1-494b-aba0-8500896d1d6f/deploy-status)](https://app.netlify.com/sites/anastasiacodes/deploys)

## About this project

This project showcases my resume. It was created using a static site generator [Hugo](https://gohugo.io/about) and hosted on [Netlify](https://www.netlify.com/). 

### Hugo advantages

* performance
  
  * branded as the world's fastest static website engine (build times < 1 ms per page)
  
  * *all* HTML files are rendered on your computer
  
* secure
  * third-party components are not allowed to mount directories
  
  * uses Go Modules to manage dependencies with cryptographic checksums
  * Markdown is defaulted to escape potentially unsafe content

## Installations

Before beginning the project, Hugo must be installed. I installed Hugo on a Mac via [Homebrew](https://brew.sh/):

```zsh
brew install hugo
```

## Create a new Hugo site

In your terminal , be sure you are in the appropriate folder. From there, use the following command `hugo new site` followed by the title of your site.

```zsh
hugo new site resume
```

If successful, Hugo creates a [directory structure](https://gohugo.io/getting-started/directory-structure/) with the following elements: archetypes, content, data, layouts, static, themes, and config.toml.

## Add a theme

If you do not want to build your own theme, you can access one of [Hugo's free themes](https://themes.gohugo.io/). I choose [DevResume](https://themes.gohugo.io/hugo-devresume-theme/) as my theme. 

Clone the repo of the theme you desire into your theme folder.

```zsh
git clone https://github.com/cowboysmall-tools/hugo-devresume-theme.git 
```

## Host on Netlify

## Continuous builds on Netlify
