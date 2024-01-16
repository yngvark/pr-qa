# QA principles

... that I use when I'm doing QA.

Motivation: Instead of having to explain the same concepts all the time, I want to refer to them here.

**Note:** The principles below reflect my subjective opinion, but I'm always open for discussion on any of these points.

See also: [How to Make Your Code Reviewer Fall in Love with You](https://mtlynch.io/code-review-love/)

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
* In documentation: "Open the X" - without mentioning what X is, nor is it clear from the context.


## Remember to document stuff

If a PR submits a new Thing, unless it's very obvious what Thing is, I want it documented.

For instance, you've created a new Terraform module, but you haven't explained why it exists.

What to document varies, but common things to document can be:

* What does Thing do?
* Why does Thing exist?
* Example usage of Thing

## Do not assume people know what X is in "the X"

If you read some text that includes the words "the X", it isn't always clear what X is to everyone. Usually, reason for this is:

* The text have not previously explained what X is. Or if does, it is far away from the current line and not in the user's "working memory".
* The text assumes the readers knows what X is, but they do not, for whatever reason.
  * A reason can be that the readers belongs to a group with another background then the author assumes.

### Example

Let's say you read a guide that talks about how to install some tool. The guide contains the text

> In the terminal, enter this command:

... without ever having mentioned a terminal before.

When saying "the terminal", it communicates a specific terminal, but the guide hasn't yet talked about any terminals. This can make the reader of the guide get questions like "Uhm, which terminal does it mean? Did I fail to read some previous step somewhere?"

