---
title: "Shopware 6 Installation with devenv in windows"
draft: false
---

{{< prep >}}

- Use a clean Windows 11 installation.
- Set your system language to english.
- Clock should be hidden.
- Use this [Wallpaper](shopware_wallpaper_clean_4k.jpg) as background.
- Install [Firefox](https://www.mozilla.org/en-US/firefox/new/)
- Remove all existing entries in the [bookmarks toolbar](https://support.mozilla.org/en-US/kb/bookmarks-toolbar-display-favorite-websites).
- Add the [devenv install docs](https://developer.shopware.com/docs/guides/installation/devenv.html) to the toolbar.
- [Pin](https://support.microsoft.com/en-us/windows/pin-apps-and-folders-to-the-desktop-or-taskbar-f3c749fb-e298-4cf1-adda-7fd635df6bb0) Firefox to the taskbar
- Close firefox

{{< /prep >}}

## Introduction

{{< actions >}}

1. Show empty Desktop
2. Open Firefox
3. Open the devenv install docs from the bookmarks toolbar
4. Scroll down the page

{{< /actions >}}

{{< voiceover >}}
{{< do "While 1" >}} Moin Moin, and welcome everyone.
My name is Niklas Dzösch, I work at Shopware and this video will show you how to install Shopware for development.

So, this is how this video works: First, I will show you a quick rundown of what to do, and after that we'll make a breakdown of everything to give you a better understanding. In the end, you should not only be able to install Shopware on you local machine, but also understand how to troubleshoot potential roadblocks on your way.

Before we start, two important things:

- This video shows you how to install Shopware on Windows 11
- Installing Shopware this way, via devenv, is only meant for developing purposes. Never use devenv in production!
{{< /voiceover >}}

{{< voiceover >}}
{{< do "2" >}} In the documentation {{< do "3" >}} you will find everything you're about to see, minus the specifics regarding Windows 11. {{< do "while 4" >}}, so when you are more of a reader, go ahead and read the devenv section in the docs.

Everyone else: Let's start!
{{< /voiceover >}}

## Prerequisites

{{< actions >}}

1. Open https://learn.microsoft.com/en-us/windows/wsl/install
2. Open Powershell
3. Execute `wsl --install`
4. Close Powershell
5. Open the [Windows Terminal](https://aka.ms/terminal) (should be already installed)
6. Open a WSL Shell (Ubuntu option)
7. Execute `uname -a`
8. Execute `sudo apt update && sudo apt upgrade -y`

<!-- TODO check if git is needed -->

{{< /actions >}}

{{< voiceover >}}
<!-- TODO add voiceover -->
{{< /voiceover >}}

{{< actions >}}

1. Open https://code.visualstudio.com/
2. Open https://vscodium.com/ <!-- ! Codium has issues with WSL -->
3. Download & install VS Code from https://code.visualstudio.com/

{{< /actions >}}

{{< voiceover >}}
<!-- TODO add voiceover -->
{{< /voiceover >}}

## Preparation

### Install Nix

{{< actions >}}

1. Open Windows Terminal with WSL shell
2. Execute `sudo apt install git -y`
3. Execute `curl --proto '=https' --tlsv1.2 -sSf -L https://install.determinate.systems/nix | sh -s -- install`
4. Execute `nix-env -iA cachix -f https://cachix.org/api/v1/install`
5. Execute `echo "trusted-users = root ${USER}" | sudo tee -a /etc/nix/nix.conf && sudo pkill nix-daemon`
6. Execute `cachix use devenv`
7. Execute `nix-env -iA devenv -f https://github.com/NixOS/nixpkgs/tarball/nixpkgs-unstable`
8. Execute `cachix use shopware`
9. Execute `nix-shell -p php82 php82Packages.composer`
10. Execute `composer create-project shopware/production shopware-dev`
11. Execute `cd shopware-dev`
12. Execute `composer require devenv`
13. Execute `exit`
14. Execute `devenv up`
15. Execute `ss -tulpn | grep ':80\|:3306\|:6379'`
16. Edit `.env`:
    1.  ```
            # <PROJECT_ROOT>/.env
            DATABASE_URL="mysql://shopware:shopware@127.0.0.1:3306/shopware?sslmode=disable&charset=utf8mb4"
        ```
17. Start a new Terminal
18. Execute `cd shopware-dev`
19. Execute `devenv shell`
20. Execute `bin/console system:install --basic-setup --create-database --force`
21. Navigate to http://localhost:8000/admin
22. Change the default sales channel domain to `http://localhost:8000`

{{< /actions >}}

{{< voiceover info="Why, this is an info" >}}
Officia enim minim nisi excepteur fugiat laboris sint qui ex. Proident ea aute do nulla. Adipisicing ipsum sint culpa velit. Laborum proident occaecat occaecat ex velit. Ipsum aute adipisicing do sint reprehenderit ea velit. Consectetur culpa aliquip deserunt nulla ipsum. Ullamco officia eiusmod aliquip labore ad pariatur exercitation do officia esse excepteur laboris consequat.
{{< /voiceover >}}

### Set up Cachix

{{< actions >}}
Show terminal with Cachix setup command.
{{< /actions >}}

{{< voiceover >}}
Next, we'll set up Cachix. Use this command to add the Cachix binary cache...

```sh
# Command for setting up Cachix
```
{{< /voiceover >}}

### Install devenv

{{< actions >}}
Show terminal with devenv installation command.
{{< /actions >}}

{{< voiceover >}}
Now, let's install devenv. Run the following command in your terminal...

```sh
# Command for installing devenv
```
{{< /voiceover >}}

## Install Shopware

### Clone the Repository

{{< actions >}}
Show terminal with Git clone command.
{{< /actions >}}

{{< voiceover >}}
With our prerequisites in place, we can now clone the Shopware repository. Use the following Git command...

```sh
# Command for cloning the repository
```
{{< /voiceover >}}

### Start the Environment

{{< actions >}}
Show terminal with 'devenv up' command.
{{< /actions >}}

{{< voiceover >}}
After cloning, navigate to the project directory and run 'devenv up' to start the environment.

```sh
# Command for starting the environment
```
{{< /voiceover >}}

### Install Shopware

{{< actions >}}
Show terminal with installation command.
{{< /actions >}}

{{< voiceover >}}
Once the environment is up, let's initialize Shopware. Run this command to install Shopware...

```sh
# Installation command
```
{{< /voiceover >}}

## Configuration and First Start

### Edit .env File

{{< actions >}}
Show text editor with `.env` file.
{{< /actions >}}

{{< voiceover >}}
Now we need to configure the environment variables. Open the .env file and make the necessary changes.
{{< /voiceover >}}

### Start Shopware

{{< actions >}}
Show terminal with start command.
{{< /actions >}}

{{< voiceover >}}
With the configuration set, let's start Shopware. Run the following command...

```sh
# Command for starting Shopware
```
{{< /voiceover >}}

### Access Admin Interface

{{< actions >}}
Show browser with admin interface.
{{< /actions >}}

{{< voiceover >}}
Finally, open your browser and go to 'http://localhost:8000/admin' to access the admin interface.
{{< /voiceover >}}

## Conclusion

{{< actions >}}
Display summary of steps.
{{< /actions >}}

{{< voiceover >}}
We have successfully installed and configured Shopware 6 using devenv. Let's quickly recap what we did today...
{{< /voiceover >}}

{{< actions >}}
Display link to further documentation.
{{< /actions >}}

{{< voiceover >}}
For more detailed information, check out the official documentation linked in the description below.
{{< /voiceover >}}

{{< actions >}}
Display farewell text and credits.
{{< /actions >}}

{{< voiceover >}}
Thank you for watching! If you found this video helpful, please give it a thumbs up and subscribe to our channel for more tutorials. See you next time!
{{< /voiceover >}}