---
title: "Shopware 6 Installation with devenv in windows"
draft: false
---

## Introduction

{{< actions >}}
Display welcome text.
{{< /actions >}}

{{< voiceover >}}
Hello everyone, welcome to this video where we will walk through the installation of Shopware 6 using devenv. Whether you're a beginner or looking to refresh your knowledge, this guide will help you get started.
{{< /voiceover >}}

## Prerequisites

{{< actions >}}
Display list of system requirements and necessary software.
{{< /actions >}}

{{< voiceover >}}
Before we begin, let's ensure we have everything we need. You'll need Nix, Cachix, and devenv installed on your system. Additionally, the necessary ports should be available.
{{< /voiceover >}}

## Preparation

### Install Nix

{{< actions >}}
Show terminal with Nix installation command.
{{< /actions >}}

{{< voiceover >}}
First, we'll install Nix. Open your terminal and run the following command...

```sh
# Command for installing Nix
```
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