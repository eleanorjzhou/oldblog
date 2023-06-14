---
title: Make a Blog with Jekyll Theme (And Make It Live on GitHub)
author: Eleanor
date: 2023-06-14 12:00:00 -0500
categories: [Web Dev, Ruby]
tags: [how-to]
render_with_liquid: false
---

If you're a developer looking to start documenting your learning with a simple and versatile blog for free, use a Jekyll theme may be a good choice.
In this post, I will share the steps I had gone through to make this blog using the Jekyll theme Chirpy.

# To-Do List

## 1. Install Required Software

- Install Git: [Download](https://git-scm.com/downloads) and install Git on your computer.
- Install Ruby: [Download](https://www.ruby-lang.org/en/) and install Ruby programming language.

## 2. Set Up a GitHub Repository

- Create a new repository on [GitHub](https://github.com/) to host your website.
- A quick and easy alternative would be using the [chirpy-starter](https://github.com/cotes2020/chirpy-starter) template to create your GitHub website.

## 3. Clone the Repository

- Open the command prompt or terminal.
- Navigate to the directory where you want to store your website files.
- Clone the GitHub repository to your local machine using the `git clone` command.

## 4. Install Jekyll and Bundler

- Change directory to the cloned repository.
- Install Jekyll and Bundler by running the command `gem install jekyll bundler`.

## 5. Configure Chirpy Theme

- Copy or clone the Chirpy theme files into your project directory.
- Customize the `_config.yml` file to set up your website's configurations.
- Customize the theme templates and content files as needed.

## 6. Build and Test Locally

- Run the command `bundle` to install the theme dependencies.
- Build the website by running `bundle exec jekyll serve`.
- Open your browser and navigate to `http://localhost:4000` to preview your website.

## 7. Commit and Push Changes

- Use Git commands (`git add .`, `git commit -m "Your commit message"`) to stage and commit your changes.
- Push the changes to your GitHub repository using `git push` command.

## 8. Configure GitHub Pages

- Go to your repository's settings on GitHub.
- Under the GitHub Pages section, select the branch you want to use for deployment (e.g., `main` or `master`).
- Save the settings.

## 9. Visit Your Deployed Website

- After a few moments, your website should be accessible at `https://your-username.github.io/your-repository-name`.


## Issue and Fix
- After making some changes in the `_config.yml` file, the deployed site shows nothing but `--- layout: home # Index page ---`. As long as something has been changed in the config file, the theme will not deploy properly.
- I went to the theme's Issues page and found a few reports sharing this problem. It's possible that the config file was not deployed properly via the source "Deploy from a branch".
- Through testing the deployment with a new branch, the solution was confirmed to be changing the source to GitHub Actions and configure the Jekyll workflow.


