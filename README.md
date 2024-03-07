# Hosting an Online Website (Resume) using Etter's Modern Technical Writing Principles

## Purpose

The goal of this document is to describes the practical steps necessary to host a resume using Github Pages with related discussion around Andrew Etter's key principles found in his book [*Modern Technical Writing*](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS).

## Getting Started

These instructions will guide you through the process of hosting your resume on Github Pages as a static site. Note that this process was made with MacOS in mind. If you are using a different operating system the links provided may not be suitable for you. 

### Prerequisites

You must meet the following requirements:

- Have a [Github](https://docs.github.com/en/get-started/start-your-journey/creating-an-account-on-github) account.
- Have [Github Desktop](https://desktop.github.com) installed.
- Have a good understanding of Markdown including how to write in Markdown.
    - Refer to these [additional resources](#More-Resources) if needed.
- Have a Markdown editor capable of rendering [GitHub Flavoured Markdown (GFM)](https://github.github.com/gfm/) or use an in-browser editor. I recommend either downloading the [Pine](https://lukakerr.github.io/Pine/) Markdown editor or using [StackEdit](https://stackedit.io/) which is an in-browser editor.
- Have a resume formatted in Markdown.

### Instructions

1. Create a new Github repository.

    - Using Github Desktop, create a new repository by navigating to the menu bar >> File >> Create New Repository. Name your repository `[YourUsername].github.io`.
    - (Optional) You may choose to add a description for your repository.

        ![](Images/CreateNewRepository.png)
  
    > "Distributed version control systems \[such as\] Git... \[provide\] better performance, allow for offline work, and are superior for concurrent work on the same file," - Etter.

2. [Commit](https://github.com/git-guides/git-commit) your resume to your repository.

    - You should have a markdown-formatted resume. Make sure to rename it to `index.md` if it is not already. Github Pages looks for a file of that name when rendering the static site so you must name your file accordingly.
    - Use *Show in Finder* to open the local repository location and add your resume to the folder.
 
        ![](Images/OpenRepoInFinder.png)

    - Next commit your file using the *Commit to main* button at the bottom left of the application.

        ![](Images/CommitToMain.png)

3. [Push](https://github.com/git-guides/git-push) to remote repository.

    - Press the *Push Origin* button to commit your resume to the remote repository. Note that you may be prompted to [*pull*](https://github.com/git-guides/git-pull) commits from your remote repository before your push can go through. If that occurs first pull the remote changes into your local repository, then push your changes to the remote repository. 

        ![](Images/PushToOrigin.png)

    - After completing this step your resume should be visible in your remote Github repository. You can view your repository by visiting `github.com/[YourUsername]/[YourRepositoryName]`.

4. Set up Github Pages.

    - Navigate to your remote repository by visiting `github.com/[YourUsername]/[YourRepositoryName]`.
    - Now you need to edit your repository settings to tell Github Pages which directory to render.
        - Navigate to the repository settings by pressing the *settings* button which is located in the navigation bar at the top of the page. This will direct you to a new page.
        - Navigate to the 'Pages' tab under 'Code and Automation'.
        - Once there, change the 'Source' under 'Build and deployment' to 'Deploy from a branch'.
        - Change the branch to `main`, folder to `/root`, and finally press 'save'.

        ![](Images/GithubPages.png)

    > According to Etter, static websites offer speed, simplicity, portability, security, and ease of hosting. Github Pages hosts static sites by using Jekyll as its static site generator, thus it follows one of the principles

5. Adding a theme to your GitHub Pages site using [Jekyll](https://jekyllrb.com).

    - First you add a `_config.yml` file to your repository if one does not already exist. Yo can do this by clicking on 'Add file' then clicking on 'Create new file'.

        ![](Images/AddFile.png)

    - Now you should add the necessary information into your configuration file. Below is an example of a `_config.yml` file which you should use for reference.
  
      ```yml
      title: [PageTitle]
      description: [PageDescription]
      theme: [ChosenTheme]
      ```
      
    - Github Pages supports a number of [themes](https://pages.github.com/themes/).
    - Note if you do not include the description field the repository description you may have optionally chosen to set in step 1.
    
6. Your resume should be hosted.
    
    - You can view your resume at `https://[RepositoryName]`. Note this will only work if your repository is properly named with the schema `[YourUsername].github.io`.

    ![](Images/Resume.gif)

## More Resources

- Markdown
    - [Tutorial](https://www.markdowntutorial.com)
    - [Cheatsheet](https://www.markdownguide.org/cheat-sheet/)
    - [Basic Syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

## Authors & Acknowledgements

- **Billie Thompson** - *Provided README Template* - [PurpleBooth](https://github.com/PurpleBooth)

- [Casual-markdown-cv](https://github.com/casualwriter/casual-markdown-cv/blob/main/resume.md) - *Provided Resume Template* 

## FAQ

### Q: Why is markdown better than a word processor?

A: Markdown's simple and intuitive syntax make it extremely readable to most people. Since Markdown files are plain text files, they are compatible with version control systems like Git. It is a very portable language as it can be opened and edited with any text editor and can be converted to a number of other popular formats using software such as [Pandoc](https://pandoc.org).

### Q: Why is my resume not showing up?

A: Make sure your repository is properly named following the schema `[YourUsername].github.io` and your resume file was named `index.md`. Also, check that your repository settings were properly set in step 4.
