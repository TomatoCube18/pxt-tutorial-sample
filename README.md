 ## Sample Tutorial

This repository is an example of how to host a MakeCode tutorial on Github. This particular tutorial is for MakeCode Arcade, but this is fully supported for micro:bit and Minecraft as well. To create your tutorial repository:

* Open [https://arcade.makecode.com/](https://arcade.makecode.com/) (or makecode.microbit.org, minecraft.makecode.com)
* Click on **New Project**
* Give the project a descriptive name
* Click on the **Github Icon** # Create a Character

## Introduction @unplugged

First create a character to star in your game!


## Step One

**Set the background color**

---

- :tree: Open the <br/>
``||scene:Scene||``<br/>
toolbox drawer and drag <br/>
``||scene:set background color [ ]||`` <br/>
into **the empty** ``||loops(noclick):on start||`` container already in your workspace. 

~hint What does that mean? 🤷🏽

Use the ``||custom:make random background||`` block to add a background color.

```blocks
// @highlight
custom.makeRandomBackground()
```

## Step Two

Create a sprite with the ``||variables:set mySprite to||`` block.

```blocks
custom.makeRandomBackground()
// @highlight
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . .
    . . . . . . . . . b 5 b . . . .
    . . . . . . . . . b c . . . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . . . . b b 5 d 1 f 5 5 d f . .
    . . . . b 5 5 1 f f 5 d 4 c . .
    . . . . b 5 5 d f b d d 4 4 . .
    b d d d b b d 5 5 5 4 4 4 4 4 b
    b b d 5 5 5 b 5 5 4 4 4 4 4 b .
    b d c 5 5 5 5 d 5 5 5 5 5 b . .
    c d d c d 5 5 b 5 5 5 5 5 5 b .
    c b d d c c b 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
```

## Step Three

Add movement with the ``||controller:move mySprite with buttons||`` block.

```blocks
custom.makeRandomBackground()
let mySprite = sprites.create(img`
    . . . . . . . . . . b 5 b . . .
    . . . . . . . . . b 5 b . . . .
    . . . . . . . . . b c . . . . .
    . . . . . . b b b b b b . . . .
    . . . . . b b 5 5 5 5 5 b . . .
    . . . . b b 5 d 1 f 5 5 d f . .
    . . . . b 5 5 1 f f 5 d 4 c . .
    . . . . b 5 5 d f b d d 4 4 . .
    b d d d b b d 5 5 5 4 4 4 4 4 b
    b b d 5 5 5 b 5 5 4 4 4 4 4 b .
    b d c 5 5 5 5 d 5 5 5 5 5 b . .
    c d d c d 5 5 b 5 5 5 5 5 5 b .
    c b d d c c b 5 5 5 5 5 5 5 b .
    . c d d d d d d 5 5 5 5 5 d b .
    . . c b d d d d d 5 5 5 b b . .
    . . . c c c c c c c c b b . . .
`, SpriteKind.Player)
// @highlight
controller.moveSprite(mySprite)
```on the bottom toolbar next to the project name and sign in if prompted
* Click **Go ahead**

This will make an empty MakeCode repository in your Github account.

## Tutorial Files

By default, the content from the README file is loaded as a tutorial. You can view it using this URL:

> [http://arcade.makecode.com/#tutorial:https://github.com/shakao/pxt-tutorial-sample](http://arcade.makecode.com/#tutorial:https://github.com/shakao/pxt-tutorial-sample)

The url should be formatted as follows: `https://[editor URL]/#tutorial:[github-username]/[github-repository-name]`

You can also include additional tutorials in one repository. In this case, the `first-tutorial.md` and `second-tutorial.md`. If you add a new file, make sure it is included in the `files` list in `pxt.json`. If you add this file from the MakeCode Editor, it will be automatically updated. You can view these tutorials at the following URLs:

> [http://arcade.makecode.com/#tutorial:https://github.com/shakao/pxt-tutorial-sample/first-tutorial](http://arcade.makecode.com/#tutorial:https://github.com/shakao/pxt-tutorial-sample/first-tutorial)

> [http://arcade.makecode.com/#tutorial:https://github.com/shakao/pxt-tutorial-sample/second-tutorial](http://arcade.makecode.com/#tutorial:https://github.com/shakao/pxt-tutorial-sample/second-tutorial)

The url should be formatted as follows: `https://[editor URL]/#tutorial:[github-username]/[github-repository-name]/[path-to-tutorial]`

## Custom Blocks

A repository containing a tutorial may also contain custom blocks for use in the tutorial. The `custom.ts` file here exports two functions as blocks. These blocks can then be used in any tutorial in the same repository. As with new tutorial files, make sure any new TypeScript files are added to the list in `pxt.json`.

## Custom Localization

Localized versions of the tutorial can also be added to the repository, under a `_locales` folder. This folder contains a list of sub-directories with the correctly capitalized language code (eg. zh-CN, de-DE). The localized tutorial should have the same file name as the base tutorial. To view a localized version of the tutorial, add `?lang=[language-code]` to the URL, as follows:

> [http://arcade.makecode.com?lang=zh-CN#tutorial:https://github.com/shakao/pxt-tutorial-sample/first-tutorial](http://arcade.makecode.com?lang=zh-CN#tutorial:https://github.com/shakao/pxt-tutorial-sample/first-tutorial)

## Creating a Release

When you update the Github repository, it make take up to 20 minutes for your changes to be reflected in the MakeCode editor, due to caching. To force an update, you will need to create a "release":

* Open [https://arcade.makecode.com/](https://arcade.makecode.com/) (or makecode.microbit.org, minecraft.makecode.com)
* Click on **Import** on the right-hand side above the row of your projects
* Select **Your Github Repo** and sign into Github if prompted
* Select the repository with your tutorial
* In the MakeCode editor, click the **Github Icon** on the bottom toolbar by the project name
* In the **Release Zone** section of the page, click **Create a Release** and select whichever release type feels most appropriate.
