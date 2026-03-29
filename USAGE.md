# Usage

This document guides you on how to use the pipeline. Make sure you have installed the necessary software according to `INSTALLATION.md` first!

## Getting started

Once you have installed the necessary software, I recommend first taking the quick introductory tour of Better Notes. This is the pop-up that came up when you installed the plugin. If you skipped it, you can access it again through `Help > Open Better Notes User Guide`. **NB**: The user guide creates a "Welcome to Better Notes" note inside your library - remember to delete it unless you want to keep it!

## The pipeline

1.  Make a Shared Library and Git repo.
2.  Import references.
3.  Weed out false positives.
4.  Read and make tagged notes.
5.  Analyze in Obsidian.

### Step 1: Make a Shared Library and Git repo

For each literature review, make a new Shared Library in Zotero. Remember that you can easily copy references between libraries!

1.  On your profile page on Zotero.org, under Groups, select **Create a New Group**.
2.  Name it according to your project and choose the visibility you want.

> [!TIP]
> **Choosing visibility**
>
> Since you're doing science, you probably want a public visibility. However, if you wish, you can choose a restricted visibility for now, and update it at any time from your Zotero profile.

The Shared Library represents the repository of your literature review.

> [!TIP]
> **Why a group/shared library?**
>
> The main benefit from a group or shared library is that multiple people can easily edit and add to the reference list inside Zotero. However, since we use a Git repository, it could be feasible to move over to using Git only. This would have the added benefit of a single source of truth, but does require all your collaborators to also know Git - using just a shared library means that your review note system is optional, and your collaborators can easily continue just using Zotero with whatever note-taking system they prefer.

3.  On your machine, create a new Git repository.

In a folder of your choosing, create a new Git repository. You can give it any name, but I recommend using the same name as the Zotero group for simplicity:

```bash
mkdir my_repository
cd my_repository
git init
```

4.  On Github, select the `+` icon in the upper bar to create a new repository.
5.  Name it the same as your local Git repository, and give it your preferred visibility settings.

Leave the repository completely empty, i.e., make sure that all file-adding options are ticked off (e.g., a license file or a readme). You can add these later if you wish.

6.  On your machine, follow Github's instructions in the empty repository to make your initial commit and connect the remote Github repo to your machine's local repo.

Note, that you need *something* inside the repo in order to make your first commit and push. If you wish, you can make a file `README.md`, write a short explanation of your literature review, and commit that.

> [!WARNING]
> **Missing credentials?**
>
> If you just installed Git, you might be missing your appropriate credentials to push to Github. You need to authenticate to Github, using one of several methods. Since there are many ways to do this, I recommend following [Github's instructions](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github) and taking the recommended route. **Only deviate from the recommended route if you know what you are doing.**
