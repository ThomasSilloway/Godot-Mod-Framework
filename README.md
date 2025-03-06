# Godot Mod Framework
A Godot game template that is set up for mod support from the beginning

Inspired by: https://www.youtube.com/watch?v=tTdToEu6x8U and https://www.youtube.com/watch?v=K3MnEvrC8TA

## Purpose

Build the game as a collection of mods to ensure that your game properly supports modders upon release

## Versions

### Godot Mod Framework
 - Basic version that loads a single mod and prints a hello world message. Can be used as a solid baseline for custom implementation
 - (This repo)

### Mods built with this template
 - [Full Game Mod (Flappy Bird Clone)](https://github.com/ThomasSilloway/Godot-Mod-Framework-Flappy-Bird-Clone)

## Getting Started

This repository is set up as a GitHub template. To create your own project based on this template:

1. Visit: [Github Template Docs](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template)
2. Follow the instructions to create a new repository from this template

## Tech Details

- Each mod is a separate godot project
- `startup` is the main project that does loading mods. Handles global things too like Settings, Config

## Usage - Manual

- Export `start` project as an .exe (Turning on Export Console Wrapper is handy for testing)
  - Export folder: build
- Export mod projects as a .zip and put it into the 
  - Export folder: build/mods

- Run the `startup` executable and view the logs to see it's try to load mods, but none are found

## Usage - Automated
- Update `scripts/build.bat` to match your paths
- Run the build batch file to automatically create versioned builds

## Updating From Template

Info from: [Stack Overflow](https://stackoverflow.com/questions/56577184/github-pull-changes-from-a-template-repository)

If you need to pull in updates from this template after creating your game, you can do so using the following Git commands:

```bash
# Add this template repository as a remote
git remote add template [URL of the template repo]

# Fetch all changes
git fetch --all

# Merge changes from the template's branch to your current branch
git merge template/[branch to merge] --allow-unrelated-histories
```

For more details, see: https://help.github.com/en/articles/adding-a-remote

## Areas to explore in the future
I'm not sure if I'll be adding these features, but they are worth exploring if someone wants to tackle them
- Inside of a mod can you do this?
  - Can you print out all of the resources?
  - Can you print out any of the code?
  - Can you overwrite / update enums in a mod?
- Add a way to for mods to add their own options to "mod settings"
- Add a UI to show the mods that are loaded, ideally load and unload mods from inside the game

## Notes
 - You can overwrite the `startup` project's audio buses with your own custom names

