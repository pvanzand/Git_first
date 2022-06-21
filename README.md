# Git_first
Developing a repo on Github first


Given the instructions on https://happygitwithr.com/new-github-first.html, I've created this repo on Git first, then have established the connection through RStudio.

Here are the steps:

Enter this in the terminal:

usethis::create_from_github(
    "https://github.com/pvanzand/Git_first.git",
    destdir = "/Users/petervanzandt/Documents/data_science/R_projects/R4DS"
)

, where:

The first argument is repo_spec and it accepts the GitHub repo specification in various forms. In particular, you can paste the URL we just copied from GitHub.

The destdir argument specifies the parent directory where you want the new folder (and local Git repo) to live. If you don’t specify destdir, usethis defaults to some very conspicuous place, like your desktop. If you like to keep Git repos in a certain folder on your computer, you can personalize this default by setting the usethis.destdir option in your .Rprofile.

We’re accepting the default behaviour of two other arguments, rstudio and open, because that’s what most people will want. For example, for an RStudio user, create_from_github() does this:

Creates a new local directory in destdir, which is all of these things:
1. a directory or folder on your computer
2. a Git repository, linked to a remote GitHub repository
3. an RStudio Project

* Opens a new RStudio instance in the new Project
* In the absence of other constraints, I suggest that all of your R projects have exactly this set-up.

There’s a big advantage to the “GitHub first, then RStudio” workflow: the remote GitHub repo is configured as the origin remote for your local repo and your local main branch is now tracking the main on GitHub. This is a technical but important point about Git. The practical implication is that you are now set up to push and pull. No need to fanny around setting up Git remotes and tracking branches on the command line.

Now make local changes, save, and commit

Commit these changes to your local repo. How?

1. Click the “Git” tab in upper right pane
2. Check “Staged” box for any files whose existence or modifications you want to commit.
* To see more detail on what’s changed in file since the last commit, click on “Diff” for a Git pop-up
3. If you’re not already in the Git pop-up, click “Commit”
4. Type a message in “Commit message”, such as “Commit from RStudio”.
5. Click “Commit”

