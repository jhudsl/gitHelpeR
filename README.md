### gitHelpeR

gitHelper accesses GitHub API from R and performs some course management functions, including retrieving chapter names and learning objectives for courses hosted on GitHub repositories.

## Installation

You can install `gitHelpeR` from GitHub with:

``` r
# install.packages("remotes")
remotes::install_github("jhudsl/gitHelpeR")
```

## Set up with GitHub token

If you want `gitHelpeR`, to have full capabilities you will need to give give your local RStudio a GitHub token.
To do this, run this command:

```
usethis::create_github_token().
```
You should only need to do this once per RStudio environment.
If you don't supply a token this way, then private repositories (or those you don't have permissions to access) will not be able to be accessed.

## Checks if a repository exists in GitHub

```
gitHelpeR::check_git_repo("jhudsl/DaSL_Course_Template_Bookdown")
```

## Get all repository names for an organization

```
gitHelpeR::retrieve_org_repos(org_name = "jhudsl", output_file = "jhudsl_repos.tsv")
```

## Get bookdown chapters for a repository

```
gitHelpeR::get_chapters("jhudsl/Documentation_and_Usability")
```

## Get all bookdown chapters for a all repositories in an organization
```
gitHelpeR::retrieve_org_chapters(org_name = "jhudsl", output_file = "jhudsl_chapter_info.tsv")
```
