---
title: "Shopware 6 Installation with devenv"
date: 2024-06-13T13:41:44+02:00
draft: false
---

# Shopware 6 Installation with devenv

## Introduction

{{< screen >}}
Display welcome text.
{{< /screen >}}

{{< voiceover >}}
Hello everyone, welcome to this video where we will walk through the installation of Shopware 6 using devenv. Whether you're a beginner or looking to refresh your knowledge, this guide will help you get started.
{{< /voiceover >}}

## Prerequisites

{{< screen >}}
Display list of system requirements and necessary software.
{{< /screen >}}

{{< voiceover >}}
Before we begin, let's ensure we have everything we need. You'll need Nix, Cachix, and devenv installed on your system. Additionally, the necessary ports should be available.
{{< /voiceover >}}

## Preparation

### Install Nix

{{< screen >}}
Show terminal with Nix installation command.
{{< /screen >}}

{{< voiceover >}}
First, we'll install Nix. Open your terminal and run the following command...

```sh
# Command for installing Nix
```
{{< /voiceover >}}

### Set up Cachix

{{< screen >}}
Show terminal with Cachix setup command.
{{< /screen >}}

{{< voiceover >}}
Next, we'll set up Cachix. Use this command to add the Cachix binary cache...

```sh
# Command for setting up Cachix
```
{{< /voiceover >}}

### Install devenv

{{< screen >}}
Show terminal with devenv installation command.
{{< /screen >}}

{{< voiceover >}}
Now, let's install devenv. Run the following command in your terminal...

```sh
# Command for installing devenv
```
{{< /voiceover >}}

## Install Shopware

### Clone the Repository

{{< screen >}}
Show terminal with Git clone command.
{{< /screen >}}

{{< voiceover >}}
With our prerequisites in place, we can now clone the Shopware repository. Use the following Git command...

```sh
# Command for cloning the repository
```
{{< /voiceover >}}

### Start the Environment

{{< screen >}}
Show terminal with 'devenv up' command.
{{< /screen >}}

{{< voiceover >}}
After cloning, navigate to the project directory and run 'devenv up' to start the environment.

```sh
# Command for starting the environment
```
{{< /voiceover >}}

### Install Shopware

{{< screen >}}
Show terminal with installation command.
{{< /screen >}}

{{< voiceover >}}
Once the environment is up, let's initialize Shopware. Run this command to install Shopware...

```sh
# Installation command
```
{{< /voiceover >}}

## Configuration and First Start

### Edit .env File

{{< screen >}}
Show text editor with `.env` file.
{{< /screen >}}

{{< voiceover >}}
Now we need to configure the environment variables. Open the .env file and make the necessary changes.
{{< /voiceover >}}

### Start Shopware

{{< screen >}}
Show terminal with start command.
{{< /screen >}}

{{< voiceover >}}
With the configuration set, let's start Shopware. Run the following command...

```sh
# Command for starting Shopware
```
{{< /voiceover >}}

### Access Admin Interface

{{< screen >}}
Show browser with admin interface.
{{< /screen >}}

{{< voiceover >}}
Finally, open your browser and go to 'http://localhost:8000/admin' to access the admin interface.
{{< /voiceover >}}

## Conclusion

{{< screen >}}
Display summary of steps.
{{< /screen >}}

{{< voiceover >}}
We have successfully installed and configured Shopware 6 using devenv. Let's quickly recap what we did today...
{{< /voiceover >}}

{{< screen >}}
Display link to further documentation.
{{< /screen >}}

{{< voiceover >}}
For more detailed information, check out the official documentation linked in the description below.
{{< /voiceover >}}

{{< screen >}}
Display farewell text and credits.
{{< /screen >}}

{{< voiceover >}}
Thank you for watching! If you found this video helpful, please give it a thumbs up and subscribe to our channel for more tutorials. See you next time!
{{< /voiceover >}}