# Mathlore Vault

This repository allows for direct access to the public collection content available on [mathlore.org](https://mathlore.org).  To add content to Mathlore you can either use the [mathlore.org](https://mathlore.org) website or contribute content directly to this repo.

## Background

The [mathlore.org](https://mathlore.org) website is designed so that math knowledge can be contributed to the system without having to specify where it is located in a directory tree of math knowledge.  Instead, tag(s) are used to describe what area(s) of mathematics the knowledge relates to.

This works great for [mathlore.org](https://mathlore.org) where an advanced search system is used to find math knowledge.

Sometimes, however, it is nice to have direct access to the files containing the math knowledge organized in directories and files by the area of mathematics where the knowledge most closely aligns.  This respository allows for that type of direct access.

## Repository Layout

In particular, this repository contains an `upstream` directory and an `organized` directory.

The `upstream` directory contains a mirror of all of the content of [mathlore.org](https://mathlore.org) organized by each item's unique id.

The `organized` directory, on the other hand contains some of the contents of the `upstream` directory organized in directories and files based on areas of mathematics (for example, `organized/sets.math`).  It is also the place where modifications are made to MathLore through this repository.

Any math knowledge entry in the `organized` directory can be found in the `upstream` directory, but there might be items in the `upstream` directory that have not yet been manually organized in the `organized` directory.

Again, this structure is used to allow anyone using [mathlore.org](https://mathlore.org) to contribute math knowledge without having to determine exactly how it should be organized.  Instead, when the contents of [mathlore.org](https://mathlore.org) are synced to this repo, the maintainers here copy the data from the `upstream` directory to a subdirectory and file of the `organized` directory to organize the knoweldge.

Further, when a modification is made in the `organized` directory in this repository, custom toolilng updates the [mathlore.org](https://mathlore.org) website with the modification and syncs the changes back in `upstream` directory.  As such, this repository and [mathlore.org](https://mathlore.org) are always in sync.

## Contributing Content

The [GitHub workflow](https://jarv.is/notes/how-to-pull-request-fork-github/) is used to modify content in or contribute new content to Mathlore using this repo.  In particular, you will want to make your own fork of this repository and create a branch in that fork with your changes you want to contribute.

The math knowledge in this repository is recorded in the [MathLingua](https://github.com/DominicKramer/mathlingua) language.  To assist in authoring MathLingua code, it is recommended you use the [Visual Studio Code](https://code.visualstudio.com/) editor with the [MathLingua Language Support](https://marketplace.visualstudio.com/items?itemName=dominickramer.mathlingua-language-support) extension.

The instructions below assume you are working in your own fork of this repository in a new branch.

### Creating New Content

To create new content, either add content to an existing file in the `organized` directory or create a new file with your content.

If you do now know where exactly the content should be placed in the `organized` directory, simply place it in a new `organized/NEW.math` file.  When your contribution is accepted, the maintainers of this repository will organize the content for you.

### Modifying Existing Content

To modify existing content, find an item in the `upstream` directory you would like to modify and copy its contents to any new or existing file in the `organized` directory.  Then modify the content as needed.

Do not, however, modify the item's `id` since that is what is used to determine that your changes are a modification of an existing item.  Otherwise, they will be viewed as an addition of a new item.

### Deleting Content

To delete content from Mathlore, simply delete it from the file it is found in in the `organized` directory.  If there is no such file, you will first need to make a contribution that copies the content into the `organized` directory and then make a follow-up contribution that deletes the item.

### Contributing Your Changes To Mathlore

After you have made the changes you would like to make, create a GitHub pull request for your branch.  Your changes will be reviewed, and, if accepted, the maintainers of this repository will land your changes and tooling will be run to update this repository and [mathlore.org](https://mathlore.org) with your modifications.
