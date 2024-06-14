---
title: "Example Script"
date: 2024-06-14T10:01:43+02:00
draft: false
weight: 10
---

<!-- 
# Purpose of this file

This is an example script.
This text will not be shown in the output file, it is meant to tell you a bit about how this script works.
To add comments to a markdown file like this, we use the syntax from HTML: https://www.w3schools.com/html/html_comments.asp

Read along to learn how to create your own script.

Before we start, let's learn how comments can be used to either communicate with your future self ot other people that might want to use this in the future.

Depending on how a line in a comment starts, it can mean different things.
If you are using VS Code an the recommended extensions for editing this file, the different types of comments will even be colorized for your convenience.
VS Code is available here: https://code.visualstudio.com/

The comments differ in how they start. So only the first character or word decides, what type of comment we are looking at here.

Here is a list of all comment types we use in script creation:

# This is just an information

* This is important information

! This is a warning.

? This comment indicates: Something is unclear

// This is an information you want to keep, but it's no longer relevant.

TODO This indicates an unfinished task

-->

<!-- # Markdown

For structuring your video script, just use normal markdown.
You can learn markdown in 60 seconds here: https://commonmark.org/help/

-->

# The power of example.com

## Introduction

<!-- # Shortcode: Prep (Preparation)

When you write text between the elements {{< prep >}} and {{< /prep >}},
whatever you are describing in the text between those elements is meant to be
done by the person recording the video before the actual recording.

Things to describe here are what the environment should look like,
what tools they should use, or which version of specific tools.

! This should put the person reading this in the position to start recording
! and follow the steps described in the next steps. Basically, after all of
! what you described here is done, everything should be ready to record.

You can also use media files along with your description.

* Note the difference between {{< prep >}} and {{< /prep >}}:
* The second one indicating the end of the description has a preceding "/" character.

-->
{{< prep >}}
- Install Firefox
- Open Firefox
- Navigate to `example.com`

This is what the page should look like:

<!-- ! put your media files in a folder named as your md file to reference them directly -->
![screenshot: example.com](example.png)

- Put the browser in the center of your screen.
- Make sure your system clock is hidden
- Use the default Shopware wallpaper for academy recordings

{{< /prep >}}

<!-- # Shortcode: Actions

When you write text between the elements {{< actions >}} and {{< /actions >}},
whatever you are describing in the text between those elements is meant to be
done by the person recording on their computer and recorded for the resulting video.

This means between these tags, you are expected to describe a succession of events
on the screen of a computer that are recorded. Be as specific as needed, the goal
is that someone who is not you can take this description and use it to create content
based off of it.

You can also use media files along with your description.

* Note the difference between {{< actions >}} and {{< /actions >}}:
* The second one indicating the end of the description has a preceding "/" character.

-->
{{< actions >}}
Only the screen from the preparation is visible, no action is taken.
{{< /actions >}}

<!-- # Shortcode: Voiceover

When you write text between the elements {{< voiceover >}} and {{< /voiceover >}},
whatever you are describing in the text between those elements is meant to be
read aloud during whatever you have describes with the preceding "visuals" shortcode (see above).

* Note the difference between {{< voiceover >}} and {{< /voiceover >}}:
* The second one indicating the end of the description has a preceding "/" character.

-->
{{< voiceover >}}
Hello everyone, welcome to this video where we will walk through the depths of the example.com site!

My name is XXXX, and I am your host for this video. Let's dive right in!
{{< /voiceover >}}

## The example domain

{{< actions >}}
1. Click on the "More information..." link in the browser
2. Wait for the site to load
3. Highlight "please do not design applications that require the example domains to have operating HTTP service"
4. Click on the link "IANA-managed Reserved Domains"
5. Scroll down the page
{{< /actions >}}

<!-- # Linking actions and voicover

Until now, we only talked about leavin comments in the code of the script.
But what if you want to leave a comment in the voiceover to indicate when
specific actions should be taken, or to provide instructions like how
to say things, or when?

Use the shortcode {{< do "X" >}}. This has no closing tag as the other shortcodes, as it is meant to be used
inline in your text as shown below. The idea is to just provide the number of the action defined in the last 
"actions" block so the person recording (or cutting in postproduction) knows how to syncronise what is said
and done.

You can provide additional information that is shown when hovering over the action item if needed, like shown
in the second example.

-->
{{< voiceover >}}
As you can see, we are looking at the example.com home page, and this domain does not only exists, it is even meant to be used as an example!

Now the question is, who is behind this? Let's see {{< do "1" >}} what this link is all about.

{{< do "2" "This might take a while, just remain silent until everythin is loaded" >}}

What you see here is the home page of the oana, hich is basically the highest authority when it comes to domain names.
That means that not any ordinary company owns example.com, but the very organisation that has the power over all existing
domain names.

This gives us the security that it's not something that might change in the future or anything like that.
Still, as you can see here {{< do "3" >}}, while we can use the domain in any and every documentation or test, we still should
do this in a reasonable manner.

The question now is, are there other purpose-specific domains we can use? {{< do "4" "The loading will be cut, so you could also take a break here." >}}
{{< /voiceover >}}

<!--
# Splitting voiceovers

If you know that something can be recorded in multiple takes, end the voiceover block and create a new one.
This indicates to the person recording that this does not need to be recorded in one piece.

Remember, the goal of these scripts is to be easy to read and implement.
If something doesn't work just report it to the maintainers and we'll find a solution.

-->
{{< voiceover >}}
<!--
* Still, be so kind to reference the last step that led us here
* if things are complicated, add a new prep block between to make things easier
-->
{{< do "Pick up after 4">}}

{{< do "While doing 5">}}
As you can see here, there are also "Test IDN top-level domains", "Policy-reserved domains" and "Other Special-Use Domains".

<!-- # you can also use the info shortcode to add additional instructions and details, it works similar to the "do" shortcode -->
{{< info "Upbeat voice:" "Do not overdue it, but make sure you sound happy and friendly">}} I encorage you to take a look yourself and hope you are excited about example domains as I am! Have a great day, see you next time.
{{< /voiceover >}}