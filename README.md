# Code Review

In this module we will explore the concept of _style_ in programming:
* **What does _Good Style_ look like in code?**
* **What are programming _Best Practices_ and how do you recognize them?**

## Style Guides

> _The point of having style guidelines is to have a common vocabulary of coding so people can concentrate on what you’re saying rather than on how you’re saying it._ -- Google HTML/CSS Style Guide

* [Airbnb Style Guide](https://github.com/airbnb/javascript)
* [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.xml)

## Code Smells
In order to understand what _good_ code looks like, let's familiarize ourselves with some "anti-patterns" or "code smells" first. Here are some commmon "smells":

* Excessive Comments
* Dead Code (e.g. commmented-out, or completely unused code)
* Long Methods / Large Classes
* Inconsistent Naming (e.g. using `$` in front of jQuery variable names sometimes but not others)
* Uncommunicative Naming (`potato`)
* Long Parameter Lists
* Inconsistent Interfaces
* Duplicated code (could it be a loop or a function instead?)
* Complex Conditionals
* Combinatorial Explosion
* Speculative Generality (aka "premature optimization")
* Inappropriate Intimacy (aka "entangled code")

> Source: [List of Code Smells](https://blog.codinghorror.com/code-smells/)

**Exercise**: Take a moment to review your own code.
* What style guide rules did you adhere to?
* Which rules did you break?

## Code Review
On professional development teams it is common to go through a "code review" process before code is accepted/merged into the master branch. In this process, your colleagues will look closely at your code and try to find problems with it: Does it adhere to style guidelines? Does it work? Is it clear? Based on their feedback, you will be expected to revise and resubmit your code.

Since this is a common (universal?) part of being a developer, we want to give you practice with that process now. This might mean that you're reviewing someone's code who you think is a "better" developer than you, and while that can feel intimidating, that is a *normal thing* in industry! At Google, I was expected to start reviewing code for other people on my team within the first month I was there, even though I was writing HTML/CSS/JS for the first time ever, and the people on my team had been writing code on that team for literally years. Reviewing another developer's code both lets you point out things that you might notice that they didn't, AND lets you see how another person approaches problems; it can be a learning experience on both sides. Doing code reviews for more experienced developers helped me learn new tricks that I could apply the next time I had similar code to write. And, because I had a slightly different perspective from them, I could still notice places where I thought they should leave better comments, or where they could use a slightly different approach.

**Exercise**: Find a partner and read through each others' code. Here are the steps you will likely want to take:

1. Open their app and test it out. Do things work the way you expect? If you notice any bugs or incomplete features at this point, make note so you can look for those issues in their code.
2. Read their code all the way through. Make note to yourself of where in their code you get lost or want to come back and read through more closely. Your goal is to figure out which parts of their code are responsible for which pieces of their site's functionality.
3. Go back to any interesting parts of the code from the previous 2 steps: either code where you _expect_ to find a bug based on their site, or code that looked interesting/well-written/weirdly-written when you read through the first time. Those are the most important parts of the code to write comments for.
4. Now that you have more clarity on how the code is _supposed_ to work, read it through, closely, to see if anything surprises you. Anything that you found confusing, or where you notice any of the "code smells" from above, is a great place to leave a comment explaining what you notice. (If you have a suggestion that is ~one line of code, feel free to actually write the line of code you're suggesting, in addition to explaining why you're making that suggestion.)
Ask yourself the following questions:

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
        + Parts of the code that seem like they came from StackOverflow with no explanation/link
      - Overloading Functions
          + Accepts too many parameters (3 or fewer is best!)
          + Does too many things (could be broken down further)
