---
layout: page
title: Getting started
---
## Creating a new project

### Step 1

Its advisable when creating a new richmedia unit to first scaffold the initial project This will save you a lot of
time and effort. Generate (scaffold) a new banner project. This will generate all the necessary files and folder structure you need for
the project.

In the terminal, make your way to a new project folder of your choosing, e.g. _**documents/work/my-banner-project**_

$ `yo richmedia-temple`

![Screenshot install grichmedia scaffold](./assets/img/Screenshot_install_richmedia_scaffold.png)

If this is the first time you’re running this command, Yeoman will ask you the following:

```
We're constantly looking for ways to make yo better!

May we anonymously report usage statistics to improve the tool over time?

More info: https://github.com/yeoman/insight & http://yeoman.io

Up to you if you want to send them statistics. Hit either **Y** or **N**.
```

After you make your selection, the following menu appears

![Screenshot richmedia welcome](./assets/img/Screenshot_richmedia-welcome.png)

In this menu you can use the arrow keys to navigate the cursor.

### Step 2

We’re just going to create a standard banner in this guide, so in this case, just hit `Enter` to select

>**create a banner**

Enter the name of the project or just hit enter to use the default, which is the folder name.

![Screenshot banner name](./assets/img/Screenshot_banner-name.png)

### Step 3

Select the first unit you would like the generator to create. Use the arrow keys to navigate and hit `Enter`
when ready.

![Screenshot uniti size](./assets/img/Screenshot_select-unit-size.png)

Enter the directory where you wish the source files to be placed. Just hit enter to use the default, which is something 
like “./src/{size}x{width}”

Select the type of banner (refer to [types of banners](./banner-types.md) for more info)

![Screenshot banner type](./assets/img/Screenshot_banner-type.png)

For the purposes of this guide, select `plain`.

The generator will generate the basic template files and install the according node modules as well. This process will take 
a minute. When it’s done, you’ll end up with a directory looking something like this You now should see a few files in the 
directory that you executed the generator on.

| Filename                     | Description                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| node_modules                 | all the packages / libraries your project uses.                                                                                                            |
| src/300x250/[.richmediarc](./richmediarc.md)   | The configuration file for the `richmedia-temple-server`, This file is used so that the `richmedia-temple-server` knows what directories are richmedia units.  |
| src/300x250/script/main.js   | Javascript File this is referenced by the `.richmediarc` file.                                                                                               |
| src/300x250/script/Banner.js | The banner javascript code.                                                                                                                                |
| src/300x250/index.html       | Main html file, this file is referenced by the `.richmediarc` file.
| .editorconfig                | configuration file for you editor. So everyone atleasts uses the same basic settings.                                                                      |
| .gitignore                   | configuration file used by git so it knows which files to ignore.                                                                                          |
| .prettierrc                  | A configuration file for prettier printer
| [package.json](./package-json.md)                 | A configuration file for NPM / YARN, one of the most important files in your project.                                                                      |

![Screenshot project structure](./assets/img/Screenshot_project-structure.png)

To start developing you need to run a [webpack](https://webpack.js.org/) server. Setting up a webpack server is a bit of a 
hassle that's why the [generator](./generator.md) and the [richmedia-temple-server](./devserver.md) do this for you in conjuction 
with the [.richmediarc](./richmediarc.md) file.

### Step 4

Make sure everything works by running

$ `npm run dev` more info [here](./devserver.md).

This will start the server. You’ll see something like this.

![Screenshot install dev server](./assets/img/Screenshot_run_dev_server.png)

Press **N**

![Screenshot install localhost](./assets/img/Screenshot_localhost8000.png)

Your primary browser will launch, opening [http://localhost:8000/](http://localhost:8000/)

In your terminal, you’ll be able to see the output of webpack, compiling the source code.

![Screenshot compiling](./assets/img/Screenshot_webpack-compiling.png)

In your browser, the preview environment will load along with a preview of the compiled version of the banner you just 
created. The banner should display as a simple unit with a red background.

![Screenshot banner](./assets/img/Screenshot_banner-browser.png)

If there are no javascript errors and everything works fine, that’s it!

[To the Generator](./generator.md) or [How to adjust a banner](./adjusting-a-banner.md)