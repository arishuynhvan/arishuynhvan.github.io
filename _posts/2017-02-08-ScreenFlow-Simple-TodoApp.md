---
layout: post
title: Introduction to Screen Flow - Minimal Todolist App
---

## Motivation
I applied to Codepath online course for Android Development, and was tasked to complete their pre-work of building a basic Todolist app during the application.

Thus, I followed the Codepath step-by-step intro tutorials below and completed the basic app with functionalities of adding/removing & saving todo items:

1. [Android Studio & Genymotion Emulator Installation](https://docs.google.com/presentation/d/1iD0sMc-qIG80yZ1AQfDU5nxSAl3Xe4nx-2W_g9yzMSM/edit?usp=sharing) and [video](https://vimeo.com/113893631)
2. [Android Pre-work: TodoApp](http://courses.codepath.com/snippets/intro_to_android/prework) and [video](https://vimeo.com/113893630)
3. [Walkthrough: Build the TodoApp in Android Studio](https://docs.google.com/presentation/d/15JnmfmFa0hJOEkBhG_TeymChLzDzpOTJvBlOj29A9fY/edit?usp=sharing) and [video](https://vimeo.com/72475810)
4. [Use Intents to Create Flows](http://guides.codepath.com/android/Using-Intents-to-Create-Flows)

However, when it come to editing the items, I found it quite challenging to follow the tutorial #4 to accomplish the [editting functionality](http://courses.codepath.com/snippets/intro_to_android/prework#heading-conceptual-overview).
Thus, I have created this this walkthrough tutorial to record my solution approach.

## My Todolist App

[The DodingDONE app](https://github.com/arishuynhvan/dodingDONE) features:
- User can successfully add and remove items from the todo list.
- User can tap a todo item in the list and bring up an edit screen for the todo item and then have any changes to the text reflected in the todo list.
- User can persist todo items and retrieve them properly on app restart.

![DodingDone v0.1.0 Demo](/images/dodingDONE-v0.1.0.gif)

The first 2 features are already guided in details in Codepath's tutorial #3 [Walkthrough: Build the TodoApp in Android Studio](https://docs.google.com/presentation/d/15JnmfmFa0hJOEkBhG_TeymChLzDzpOTJvBlOj29A9fY/edit?usp=sharing) and [video](https://vimeo.com/72475810),
so one may refer to that resource before continuing to read on with my tutorial.

### Things to note
- This solution doesn't incorporate SQLite for database, but save items in a local .txt file in the Android device.
- No fancy design of the view
- Compatible for Android 4.4 or later versions

# STOP!

Please check if your app looks like below before continuing:

![DodingDONE v0.0.1 Demo](/images/dodingDONE-v0.1.0.gif)

## Approach


