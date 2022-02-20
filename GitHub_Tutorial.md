GitHub Tutorial
================
Michelle Slawinski
02-25-22

Git.. GitHub.. What are they? Why do they matter? In this tutorial we
will introduce you to Git and GitHub. This presentation is for
individuals with limited knowledge on Git and GitHub, although those
with robust knowledge or background are more than welcome to join!

# Learning objectives

1.  Develop an understanding of what Git and GitHub are
2.  Install Git, GitHub and RStudio
3.  Connect Git, GitHub and RStudio

# Git

## What is Git?

Have you ever tried working on a project or a specific piece of code
with another teammate? Or have you ever overwritten your code and had to
rewrite the chunk from the beginning?

Frustrating, right? Well, Git is software that allows you to do better.
Be a better coder, communicator and person because the time you will
save can then be spent elsewhere!

Now, I will preface by saying that there is a learning curve to Git. But
keep at it, take breaks, and do not ignore your mental health.

![Git Project Workflow](https://git-scm.com/book/en/v2/images/areas.png)
*Credit: * \* Working directory/tree: where you have one version of the
project checked out \* Staging area, or “index”: a file on what will go
into your commit \* Git directory is where your metadata is. This is
what is copied when you clone a repository from one computer to another.

## **Setup**

Let’s get started shall we!

First, check to see if you already have Git installed. On Windows, look
for an application called “Git Bash” and on Macs, search for an
application called “Terminal.” Type “git version” into the terminal. If
you have an output with the version, Git is installed, if you the
terminal is saying unknown command, then Git it not installed.

If you do not already have Git installed, navigate to
[Git](https://git-scm.com/) and click *Downloads.* Select the software
appropriate for your system and follow the remaining installation steps.

**Windows**

1.  Select **“Click here to download”** This should be the version you
    need however, you can look below to see additional options.
2.  Allow installer to download then open.
3.  “Do you want to allow this app to make changes to this device?” Yes,
    yes you do! You will need administrative access to your computer for
    this.
4.  Use the defaults throughout the installation process.

![1. License
Agreement](C:/Users/slawinskimc/OneDrive%20-%20Florida%20Department%20of%20Health/Documents/GitHub/GitHub-Tutorial/Set%20Up%20Images/1%20License%20Agreemement.png "1. License Agreement")
![2. Select
Components](C:/Users/slawinskimc/OneDrive%20-%20Florida%20Department%20of%20Health/Documents/GitHub/GitHub-Tutorial/Set%20Up%20Images/2.%20Select%20Components.PNG "2. Select Components")

**Mac** 1. 2. 3. 4.

## Git Resources

-   [Pro Git Book](https://git-scm.com/book/en/v2)
-   [Git Guides](https://github.com/git-guides/install-git)

## Git Dictionary

| Term   | Definition                                                  |
|--------|-------------------------------------------------------------|
| Modify | Changed the file but have not committed it to your database |
| Staged | Marked a modified file to go into your next commit snapshot |
| Commit | Save the state of your project in your local database       |
| Shell  |                                                             |

# Graphical User Interface (GUI)

## What are GUIs?

## GUI Resources

-   [GUI Clients](https://git-scm.com/downloads/guis)

# GitHub

## What is GitHub?

## Setup

## Repositories

# RStudio

## Setup

**Checking Your Current Version of R**

``` r
R.version.string
#> [1] "R version 4.0.5 (2021-03-31)"
```

**Introducing Yourself to Git**

``` r
#install if needed:
#install.packages("usethis")

library(usethis)
use_git_config(user.name = "Michelle Slawinski", user.email = "slawinsm@gmail.com") 
  #use.email should be the same as your GitHub account
```

**Setting up a token in RStudio**

``` r
usethis::create_github_token()
#> * Call `gitcreds::gitcreds_set()` to register this token in the local Git credential store
#>   It is also a great idea to store this token in any password-management software that you use
#> * Open URL 'https://github.com/settings/tokens/new?scopes=repo,user,gist,workflow&description=DESCRIBE THE TOKEN\'S USE CASE'
gitcreds::gitcreds_set
#> function (url = "https://github.com") 
#> {
#>     if (!is_interactive()) {
#>         throw(new_error("gitcreds_not_interactive_error", message = "`gitcreds_set()` only works in interactive sessions"))
#>     }
#>     stopifnot(is_string(url), has_no_newline(url))
#>     check_for_git()
#>     current <- tryCatch(gitcreds_get(url, use_cache = FALSE, 
#>         set_cache = FALSE), gitcreds_no_credentials = function(e) NULL)
#>     if (!is.null(current)) {
#>         gitcreds_set_replace(url, current)
#>     }
#>     else {
#>         gitcreds_set_new(url)
#>     }
#>     msg("-> Removing credetials from cache...")
#>     gitcreds_delete_cache(gitcreds_cache_envvar(url))
#>     msg("-> Done.")
#>     invisible()
#> }
#> <bytecode: 0x0000000015cdadc8>
#> <environment: 0x0000000015c87410>
```

## Information for reproducibility

R and R packages are continuously updated and examples that work under a
certain set of conditions may not work under another set. Ideally, you
would update your tutorial when key software is updated to maintain
working examples. However, that may not be feasible, and the next best
option is to provide learners with all the necessary information about
your computing environment. This can help them identify differences with
their computing environment that may be preventing the example from
running as expected.

**My computing environment:**

Session information

``` r
sessionInfo()
#> R version 4.0.5 (2021-03-31)
#> Platform: x86_64-w64-mingw32/x64 (64-bit)
#> Running under: Windows 10 x64 (build 18363)
#> 
#> Matrix products: default
#> 
#> locale:
#> [1] LC_COLLATE=English_United States.1252 
#> [2] LC_CTYPE=English_United States.1252   
#> [3] LC_MONETARY=English_United States.1252
#> [4] LC_NUMERIC=C                          
#> [5] LC_TIME=English_United States.1252    
#> 
#> attached base packages:
#> [1] stats     graphics  grDevices utils     datasets  methods   base     
#> 
#> other attached packages:
#> [1] usethis_2.1.5
#> 
#> loaded via a namespace (and not attached):
#>  [1] rstudioapi_0.13   knitr_1.33        magrittr_2.0.1    gert_1.5.0       
#>  [5] rlang_0.4.11      stringr_1.4.0     tools_4.0.5       sys_3.4          
#>  [9] xfun_0.22         cli_3.1.0         withr_2.4.3       htmltools_0.5.1.1
#> [13] askpass_1.1       gitcreds_0.1.1    openssl_1.4.4     yaml_2.2.1       
#> [17] digest_0.6.27     lifecycle_1.0.0   crayon_1.4.1      purrr_0.3.4      
#> [21] fs_1.5.0          credentials_1.3.2 glue_1.4.2        evaluate_0.14    
#> [25] rmarkdown_2.8     stringi_1.5.3     compiler_4.0.5
```

RStudio version

``` r
rstudioapi::versionInfo()$version
#> [1] '1.4.1106'
```

## Sharing your tutorial

### Slides

If you’re sharing your tutorial at an R-Ladies meeting, consider making
slides to go along with it.

See the [R-Ladies Gainesville presentations
repository](https://github.com/R-Ladies-Gainesville/presentations) to
download the the R Markdown file `tutorial_template.Rmd`. The
tutorial\_template presentation is created with the
[xaringan](https://slides.yihui.org/xaringan/#1) package and the RLadies
theme by [Alison
Hill](https://www.apreshill.com/project/rladies-xaringan/).

### Github

Now it’s time to add your tutorial to the R-Ladies Gainesville
[tutorials
repository](https://github.com/R-Ladies-Gainesville/tutorials). This
will make it easier for others to provide feedback and for people to use
your tutorial!

If you do not use Github, email your `.Rmd` file to R-Ladies Gainesville
at <gainesville@rladies.org>.
