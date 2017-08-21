# Game Code Review & Refactor

In this module we will explore the concept of _style_ in programming:
* **What does _Good Style_ look like in code?**
* **What are programming _Best Practices_ and how do you recognize them?**

## Style Guides

> _The point of having style guidelines is to have a common vocabulary of coding so people can concentrate on what you’re saying rather than on how you’re saying it._ -- Google HTML/CSS Style Guide

* [Airbnb ES5 Style Guide](https://github.com/airbnb/javascript/tree/es5-deprecated/es5)
* [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.xml)

**Exercise**: Take a moment to review your game code javascript.
* What style guide rules did you adhere to?
* Which rules did you break?


## Code Smells
In order to understand what _good_ code looks like, let's familiarize ourselves with some "anti-patterns" or "code smells" first. Here are some commmon "smells":

* Excessive Comments
* Dead Code (e.g. commmented-out, or completely unused code)
* Long Methods / Large Classes
* Inconsistent Naming
* Uncommunicative Naming
* Long Parameter Lists
* Inconsistent Interfaces
* Duplicated code
* Complex Conditionals
* Combinitorial Explosion
* Speculative Generality (aka "premature optimization")
* Inappropriate Intimacy (aka "entangled code")

> Source: [List of Code Smells](https://blog.codinghorror.com/code-smells/)

**Exercise**: Take a moment to review your game code javascript.
* What style guide rules did you adhere to?
* Which rules did you break?

## Code Review
On professional development teams it is common to go through a "code review" process before code is accepted/merged into the master branch. In this process, your colleagues will look closely at your code and try to find problems with it: Does it adhere to style guidelines? Does it work? Is it clear? Based on their feedback, you will be expected to revise and resubmit your code.

**Exercise**: Take a look at the three Game solutions in this repo. Ask yourself the following questions:

- What did they do well?
    + Good style
    + Helpful comments about complex logic
    + Indentation, Spacing
    + Good variable names & function names
- What could they refactor?
    - Code "smells"
    - Don't Repeat Yourself (DRY)
        + Modularity / Encapsulation / Abstraction
    - Keep it Simple, Stupid (KISS)
        + "Premature optimization is the root of all evil" -- Donald Knuth
    - Separation of Concerns (SoC)
        + Model View Controller (MVC)
            + **M**odel Logic (Data) - e.g. player 1, player 2
            + **V**iew Logic (Presentation Logic) - What it looks like
            + **C**ontrol Logic (Game Logic) - Rules of the game
    - Mixing styles -- Vanilla Javascript DOM Manipulation vs. JQuery DOM Manipulation
    - Overloading Functions
        + Accepts too many parameters (3 or fewer is best!)
        + Does too many things (could be broken down further)

## Issue Creation
For the remainder of this block, please create Github Issues for your game code.

Please create at least one issue for the following categories:
* Broken / Buggy Code
* Style Guide Adherance
* Code Smells

Finally, try to close an issue!
