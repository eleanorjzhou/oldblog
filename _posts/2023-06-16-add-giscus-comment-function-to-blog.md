---
title: Add Giscus Comment Board to Jekyll Blog (For Free!)
author: Eleanor
date: 2023-06-16 12:00:00 -0500
categories: [Web Dev, GitHub]
tags: [how-to]
render_with_liquid: false
---

By the time I created this blog, it's lacking the comment section for people to make comments. So I decided to add the function for more interactions on the blog. Looking at the `_config.yml` file of the theme the blog uses, I can see that templates for Disqus and Giscus are already included. All I have to do is pick one of them and setup the config. I ended up picking Giscus after trying Disqus as it's free and I can easily moderate or make changes since the App and all the content live on GitHub. As usual, this post will be a To-do list to show the setup process for the Giscus App and the `_config.yml` file.

# To-Do List

## 1. GitHub Repository Setup

- Create a new repository for the comments to live in. You can name it something like `YourBlogName-comments`.
- Make sure you set it to `Public` and have administrative access to the repository.

## 2. Giscus GitHub App Setup

- Access GitHub and go to the repository where you want to install Giscus.
- Go to the "Settings" tab of the repository.
- Scroll down to the "Features" section and enable GitHub Discussions if not already enabled.

## 3. Install Giscus App

- Go to the [Giscus App](https://github.com/apps/giscus), click install or Configure.
- Under Repository access, make sure to select `Only select repositories`, then select the repository `YourBlogName-comments` we want to install into
- Grant the necessary permissions for the GitHub App to access your repository.
- Confirm the installation or click Save, and Giscus will be added as the comment system for GitHub Discussions in your repository.

## 4. Jekyll Blog Integration

- Go to the [Giscus App configuration page](https://giscus.app/) and scroll down to Repository, enter the field as `YourGitHubUsername/YourBlogName-comments`, it should confirm that the repository meets all the criteria.
- Scroll down to the Features section, here you can change the display of the comment board
- Scroll down to Enable giscus section where it shows a script. This is where we get the inputs for for config file to integrate Giscus to our blog.
- In your Jekyll blog's theme (in this case the Chirpy theme), locate `_config.yml`. The only fields that matter in this file are `repo` and `repo_id`, the rest of the fields are optional.
- Add all the necessary configs provided by Giscus to the corresponding fields in the config file.
- Commit and push the changes to your GitHub repository.

## 5. Testing and Verification

- Visit your Jekyll blog and navigate to the page where you integrated Giscus.
- Verify that the Giscus comment section is visible and functioning correctly.
- Create test discussions, leave comments, and ensure that the comments are displayed and updated properly.