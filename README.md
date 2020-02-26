# Open SDG - Simple starter

This is a starter repository to help in implementing the [Open SDG](https://github.com/open-sdg/open-sdg) platform. [See here for documentation](https://open-sdg.readthedocs.io) on Open SDG.

## Overview

This starter repo is called "simple" because it combines the data and site into one repository. This is in contrast to the [open-sdg-site-starter](https://github.com/open-sdg/open-sdg-site-starter) and [open-sdg-data-starter](https://github.com/open-sdg/open-sdg-data-starter) repos, which together make an alternative approach that splits the site and data into separate repositories.

## Requirements

* Python 3 with [pip](https://pypi.org/project/pip/)
* Ruby 2 with [bundler](https://bundler.io/)

## Getting started

1. Make your own copy of this repository, by pressing "Use this template" or going [here](https://github.com/brockfanning/open-sdg-simple-starter/generate) and filling out the form.
2. Next, create a "personal access token" as described [here](https://help.github.com/en/github/authenticating-to-github/creating-a-personal-access-token-for-the-command-line#creating-a-token), choosing the "Repo" permission, as indicated.
3. At your new repository, choose "Settings" (top right) and then "Secrets" (left sidebar). Add a new secret named "token" and paste in your personal access token.
4. Go to the "Actions" section of your repository. You will see a "Deploy to staging" job which failed.
5. Click on "Deploy to staging" and then select the "Re-run all checks" option.
6. Watch as the your site is built and deployed to GitHub.
7. Afterwards, go back to your "Settings" page, and scroll down to the GitHub pages section. You should see "Your site is published at" with a link to your site.

## Automated testing

Each time you update your site there will be 3 steps:

1. Edit one or more files
2. Create a pull request
3. Merge that pull request

This repository is capable of automatically testing all pull requests, to ensure that nothing will be broken. You can enforce this by requiring that all tests pass before a pull request is merged.

To enable this, start by making any change using the 3-step workflow above. Try a simple README change:

1. In the list of files, click on README.md.
2. Click the pencil icon on the right (You can find it next to the History button.)
3. Make some changes to the file. (Any change is fine.)
4. Towards the bottom, select "Create a new branch for this commit and start a pull request."
5. Beneath this, click "Propose file changes".
6. Click on the green "Create pull request" button.
7. Wait a moment to see the message that says "Test PRs / test (pull_request) - in progress"
8. Wait until you see "All checks have passed". This takes about 5 minutes.
9. Click on the green "Merge pull request" button.

Next, go back to your "Settings" page.

1. In the left sidebar, click "Branches".
2. Under "Branch protection rules" click "Add rule"
3. Under "Branch name pattern" enter develop
4. Check the box "Require status checks to pass before merging"
5. Under "Status checks found in the last week for this repository" check the box for "test".
6. Click the green "Create" button.

## Local installation

To try out Open SDG using this starter on your local computer, use:

```
make install
make serve
```
