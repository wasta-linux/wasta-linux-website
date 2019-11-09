# wasta-linux-website

The [wasta-linux-website](https://www.wastalinux.org) is built using [Hugo](https://gohugo.io/). Hugo is a lightweight website generator that is used to build static websites with an integrated theming engine. Pages are written in markdown allowing easy creation and maintenance.

A custom theme named _book-wasta_ that was based on [hugo-book](https://themes.gohugo.io/hugo-book/) is used. It has been modified to allow printing of pages in the case that users would like to print out the tutorial pages to use for training or reference for new Wasta-Linux users.

Below are the basics on using Hugo to run the site locally so contributors to the wasta-linux-website can see their changes before committing.

## Hugo Installation

The _extended_ version of hugo is needed to enable additional features that the wasta-linux-website uses. The easiest way to install on [Ubuntu](www.ubuntu.com) / [Wasta-Linux](www.wastalinux.org) is to install the snap package:

```
sudo snap install hugo --channel=extended/edge
```

Otherwise you can find binary builds (including .deb) of hugo-extended from their [releases page](https://github.com/gohugoio/hugo/releases).

## Contributing

To contribute to the wasta-linux-website, create a github account and click the`fork` button on this repository:

Then, you need to clone your fork down to your local computer:

```
git clone https://github.com/<USERNAME>/wasta-linux-website.git
```

Make sure that the master wasta-linux-website is linked to your fork:

```
git remote add upstream https://github.com/wasta-linux/wasta-linux-website.git
```

Then make your own branch for your changes:

```
git checkout -b "new-branch-name"
```

Make your changes, using the below information for the filestructure and how to test your changes.

Add any new files to the git repository this way:

```
git add --all
```

After each (significant) change, you will want to `commit` your changes:

```
git commit -am "<message here>"
```

Then, when you are ready to upload your changes for review by the Wasta-Linux team, push your changes up to github:

```
git push origin <new-branch-name>
```

Then, to make a `pull-request` to the original wasta-linux-website, go to your fork at Github and click the `pull request` button for your branch to contact the Wasta-Linux website maintainers. We will review your request and contact you to confirm the updates.

## Hugo Filestructure

* **content/**

  * **Source .md files:** See some of them to get a feeling for the different options available through Hugo.

* **public/**

  * **Generated Static Site:** Run the `hugo` command to re-generate the static site in the `public` folder. This folder then can be uploaded to the webserver.

* **static/img/**

  * **Images for the corresponding pages:** Please put the files for a page in a folder name matching the page, using a folder structure that matches the content organization.

* **themes/book-wasta**

  * **Hugo theme:** If there are any limitations to the theme, please let us know so that we can work together to address them.

* **config.toml:** base configuration items for Hugo

## Running Hugo Locally

From the `wasta-linux-website` directory you can start hugo locally this way:

```
hugo server -D
```

You will then find the locally running website here

[http://127.0.0.1:1313](http://127.0.0.1:1313)

## Additional Hugo Features

Use ```hugo --help``` to see other options.
