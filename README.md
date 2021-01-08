# Anastasia Powell's Resume

## About this project

This project showcases my resume. It was created using a static site generator [Hugo](https://gohugo.io/about) and hosted on [Netlify](https://www.netlify.com/). Continuous integration was setup as indicated with below [Netlify badge](https://docs.netlify.com/monitor-sites/status-badges/).

[![Netlify Status](https://api.netlify.com/api/v1/badges/636d486d-dea1-494b-aba0-8500896d1d6f/deploy-status)](https://app.netlify.com/sites/anastasiacodes/deploys)

### Hugo advantages

* performance
  * branded as the world's fastest static website engine (build times < 1 ms per page)
  * *all* HTML files are rendered on your computer
  
* secure
  * third-party components are not allowed to mount directories
  * utilizes Go Modules to manage dependencies with cryptographic checksums
  * Markdown is defaulted to escape potentially unsafe content

### Netlify advantages

* performance
  * scalable environments allows for 99.9% SLA
  * pre-built files served over CDN
  * build hooks allow both granular control and programmatic control of site
* secure
  * [SOC-2 certified](https://www.imperva.com/learn/data-security/soc-2-compliance)
  * [Jamstack](https://jamstack.org/) architecture abstracts microservice APIs
* continuous deployment
  * run build commands and deploy results to CDN when pushed to GitHub, GitLab, or Bitbucket repository
  * visual representation of site's status displayed in README via status badges
* custom domains & DNS
  * private domain name registration automatically configured to use Netlify DNS
  * allowance for external domains or utilize Netlify default subdomain

## Installations

Before beginning the project, Hugo must be installed. I installed Hugo on a Mac via [Homebrew](https://brew.sh/):

```zsh
brew install hugo
```

## Create a new Hugo site

Within the root of your Hugo project, use the following command `hugo new site` followed by the title of your site.

```zsh
hugo new site resume
```

If successful, Hugo creates a [directory structure](https://gohugo.io/getting-started/directory-structure/) with the following elements: archetypes, content, data, layouts, static, themes, and config.toml.

## Add a theme

If you do not want to build your own theme, you can access one of [Hugo's free themes](https://themes.gohugo.io/). I choose [DevResume](https://themes.gohugo.io/hugo-devresume-theme/) as my theme.

Clone the repo of the theme into your theme folder.

```zsh
git clone https://github.com/cowboysmall-tools/hugo-devresume-theme.git 
```

Open `config.toml` file and add your theme:

```zsh
theme = "hugo-devresume-theme"
```

Run the Hugo server to check to make sure your theme is installed on your site.

```zsh
hugo server
```

Open `localhost:1313` in a browser and view your website.

## Create content

As directed in the theme [README](https://github.com/cowboysmall-tools/hugo-devresume-theme/blob/master/README.md), copy the `config.toml` to the root of your site.

Change the `config.toml` input to match your resume input.

![config.toml](static/assets/images/config.toml.png)

Open `localhost:1313` in a browser to view your updated website.

![localhost](static/assets/images/localhost%20running%20site.png)

## Host Hugo site on Netlify

Create an account on [Netlify](https://app.netlify.com/signup). I signed up via GitHub. 

Provide Netlify with authorization to access your GitHub account.

## Create a new site with continuous deployment

select `New site from Git` button

Follow Netlify prompts to finish the repo connection.

Select the project repo. Select the branch, build command and deploy directory.

## Configure Hugo version in Netlify

set Hugo version in `netlify.toml` *and* `config.toml`

```zsh
[context.production.environment]
  HUGO_VERSION = "0.79.0"
  ```

## Automate Netlify build settings
