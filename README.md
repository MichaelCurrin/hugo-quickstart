# Hugo Quickstart
> Starter template for a Hugo static site

[![GitHub tag](https://img.shields.io/github/tag/MichaelCurrin/hugo-quickstart?include_prereleases=&sort=semver)](https://github.com/MichaelCurrin/hugo-quickstart/releases/)
[![License](https://img.shields.io/badge/License-MIT-blue)](#license)

[![Made with Hugo](https://img.shields.io/badge/Hugo-0.X-blue?logo=hugo&logoColor=white)](https://gohugo.io/)


This project was created using quickstart instructions on the Hugo website. See [Hugo resources](https://github.com/MichaelCurrin/code-resources/blob/master/resources/hugo.md) for links on starting out with Hugo and using the CLI.


## Preview

<div align="center">
    <img src="/sample.png" alt="Sample screenshot" title="Sample screenshot" width="400" />
</div>


## Use this project

<div align="center">

[![Use this template](https://img.shields.io/badge/Generate-Use_this_template-2ea44f?style=for-the-badge)](https://github.com/MichaelCurrin/hugo-quickstart/generate)

</div>


## Installation
> How to setup this project locally

### Install system dependencies

Follow the [Install Hugo](https://gohugo.io/getting-started/installing/) doc.

_Note: The approach recommended here is download and install Hugo globally. It is a single binary so can be in your `bin` directory. Some projects include Hugo version as a binary in a repo `bin` directory, but this needs to be done for 3 operating systems and needs to be updated manually if a newer version is needed. But it means a cloned repo that is updated will always get the exact version needed, regardless of a global version installed._

### Clone

Clone the repo and its submodules.

```sh
$ git clone --recurse-submodules git@github.com:MichaelCurrin/hugo-quickstart.git
```

You don't have to install any dependencies, as the theme was included with the submodule above.


## Usage

### Start dev server

```sh
$ hugo server
```

### Build

Run without arguments.

```sh
$ hugo
```

View the output in the ignored `public` directory.


## Deploy
> How setup and deploy on a remote server

This project can be setup easily to build and host a static site on [Netlify](https://netlify.com). You just need to add a build command.

You can also deploy and serve using [Github Pages](https://pages.github.com/), but since that runs Jekyll only you'll have to use [Github Actions](https://github.com/actions) to deploy it.


## Development

### Update themes

Update a theme to the latest version by executing the following command in the root directory of your project:

```sh
$ git submodule update --rebase --remote
```


## How to setup a fresh project

These are the steps which were followed to set this project up. These can serve as a reference for your new or existing Hugo projects.

### Create repo

```sh
$ hugo new site my-project
```
```
Congratulations! Your new Hugo site is created in my-project.

Just a few more steps and you're ready to go:

1. Download a theme into the same-named folder.
   Choose a theme from https://themes.gohugo.io/, or
   create your own with the "hugo new theme <THEMENAME>" command.
2. Perhaps you want to add some content. You can add single files
   with "hugo new <SECTIONNAME>/<FILENAME>.<FORMAT>".
3. Start the built-in live server via "hugo server".

Visit https://gohugo.io/ for quickstart guide and full documentation.
```

```sh
$ cd my-project
```

### Add a theme

Add a theme to the config.

```sh
$ echo 'theme = "ananke"' >> config.toml
```

Add the theme's repo as a Git _submodule_.

```bash
$ git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
```

This creates a [.gitmodules](.gitmodules) file and the `themes/ananke` directory and adds them both to staging. Those can then be committed.

Note that we added a subproject directory with its **own** version control, which is **not** stored by the top-level project's version control in the way that files normally are. The top-level project will keep track of which version of the submodule it needs by referencing a commit.

### Add a post

```bash
$ hugo new posts/my-first-post.md
```

### Run

Start the server, with _drafts_ enabled.

```bash
$ hugo server -D
```


## License

Released under [MIT](/LICENSE) by [@MichaelCurrin](https://github.com/MichaelCurrin).
