# QA principles

... that I use when I'm doing QA.

Motivation: Instead of having to explain the same concepts all the time, I want to refer to them here. 

## Reduce complexity / K.I.S.S

Someone else is going to maintain what you create. Make it easy for them.

More detailed problem description: https://news.ycombinator.com/item?id=34350446 (and some possible solutions: https://news.ycombinator.com/item?id=34351982)

This is not the best reference, but it's what I have right now.

Related:
* Rule of three: https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming)

## Don't make me think

When writing both documentation and code, I want whatever presented to be easy to understand.

Do not write that the reader should do something with X, and assume that the user knows what X is.

Examples:
* In a pull request: "After completing this PR, I will remove the other PR."
    * Which other PR? Don't make me think.
* In documentation: ""


## Forget documentation

If a PR submits a new Thing, unless it's very obvious what Thing is, I want it documented.

Examples:
* In Terraform, you've created a new module, but you haven't explained why it exists.
* "Open the X" - without mentioning what X is, nor is it clear from the context.
