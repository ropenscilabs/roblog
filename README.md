# roblog

The goal of roblog is to provide helpers for authors of blog posts and tech notes on rOpenSci blog.

## Installation

``` r
install.packages("roblog", repos = "https://dev.ropensci.org")
```

## Current functionality

* (R) Markdown templates (see further)

* `ro_lint_md()` to be run on the path to your blog post (rendered, not the Rmd) to identify some potential problems and enforce: the use of complete alternative descriptions for image, of relative links to rOpenSci website, of Hugo shortcodes for tweets, of lower camelCase for rOpenSci name.

## (R) Markdown templates

If you want to execute code, use the R Markdown template. If not, use a Markdown template.

The helpers will create an untitled file with the template. Do not forget to save it.

### R Markdown template

Either

* Use the RStudio addin

* Select the template via File > New File > R Markdown > From Template

* Run `roblog::ro_blog_post_rmd()`

### Markdown template

Either

* Use the RStudio addin

* Run `roblog::ro_blog_post_md()`

## How to prepare your pull request

You'll need to fork https://github.com/ropensci/roweb2 and create a branch. You can either use your usual workflow for that, or use [`usethis` helpers](https://usethis.r-lib.org/articles/articles/pr-functions.html), see below.

* Create the fork and check it out locally:

```r
usethis::create_from_github("ropensci/roweb2")
```

* Create a branch

```r
usethis::pr_init(branch = "mypost")
```
* Work locally (adding your post)

* Open the PR

```r
usethis::pr_push()
```
* Get feedback and use it

    * Get changes from GitHub to local (e.g. Stef made a suggestion in the PR review and you accepted it)

    ```r
    usethis::pr_pull()
    ```

    * Get local changes to GitHub (e.g. you updated a paragraph and improved a figure from your laptop)
    
    ```r
    usethis::pr_push
    ```
