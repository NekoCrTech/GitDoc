---
icon: page
---

# Installation & Setup

### Git Is (Primarily) A Terminal Tool&#x20;

Git was created as command-line tool. To use it, we run various git commands in a Unix shell. This is not the most user friendly experience, but it's at the very core of Git!

### The Rise of GUI's

Over the last few years, companies have created graphical user interfaces for Git that allow people to use Git without having to be a command-line expert.

Popular Git GUI's include:

* Github Desktop
* SourceTree
* Tower
* GitKraken
* Ungit

### Pros and Cons

| GUI Pros                                                                                                                                                                                                                                           | GUI Cons                                                                                                                                                                                                                                                                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Way lower barrier-of-entry for beginners compared to the command-line.<br><br>Friendlier to use. Can be a much better experience (when it works).<br><br>Some people prefer the visual experience, even those who can use the command-line.</p> | <p>At times, there is lots of "magic" involved. The inner-workings of Git are obfuscated and hidden away with GUI's.<br><br>Often leads to dependance on a particular piece of software.<br><br>When things go seriously wrong, it can be very challenging to fix without the command-line.<br><br>The interfaces, buttons, and menus vary between different GUI's.</p> |



| Command Line Pros                                                                                                                                                                                                                                                                                                                                                               | Command Line Cons                                                                                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Git is a command-line tool. All the documentation and resources online will refer to the command-line.</p><p></p><p> The command-line can be way faster once you get comfortable with it! </p><p></p><p>Some of the more advanced Git features are only available on the command-line.</p><p></p><p>The commands are always the same, no matter what machine you are on!</p> | <p>Not beginner-friendly. At All. Can be difficult to learn and remember the commands at first. </p><p></p><p>Even for some practiced users, the command line interface is just not a good experience. It's really a matter of preference.</p> |



{% hint style="info" %}
Download and install git from [https://git-scm.com/](https://git-scm.com/)
{% endhint %}

### Configuring Git

Now that Git is hopefully installed, it's time to configure some basic information. You do not need to register for an account or anything, but you will need to provide:

* Your name
* Your email

&#x20;If you are using a GUI, it should prompt you for your name and email the first time you open the app.



To configure the name and mail that Git will associate with your work, run those two commands:

```bash
> git config --global user.name "Your Name"
```

```bash
> git config --global user.email your@mail.com
```
