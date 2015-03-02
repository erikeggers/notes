# Credits
This guide is remixed from [thoughtbot's
Playbook](http://playbook.thoughtbot.com/). It is licensed as [Creative Commons
Attribution-NonCommercial](http://creativecommons.org/licenses/by-nc/3.0).

# Prerequisites
Before embarking on a project, it is important to read through the [git
guide](https://github.com/thoughtbot/guides/tree/master/protocol/git) first.

# Planning
One of our primary process goals is to make frequent, small releases of our
working software.

## Sketches
Sketch interfaces before implementing them.

## Feature Stories
We write [feature stories](http://dannorth.net/whats-in-a-story/) to specify the
desired behavior of the application.

## Wireframes
The designer will then refine the sketches into HTML and CSS wireframes. HTML
and CSS wireframes are built using Bourbon and Neat in the browser so the team
can understand the core experience as fast as possible. It also allows
developers to start implementing features within the wireframes.

It is crucial to keep the design of the application ahead of the development.
Focus should be placed on wireframing usability, user experience, and flows.

## Daily Standups

Every morning, we get together as a team for 10 minutes at 9 AM.

We say what we did yesterday, what we're going to do today, and if anything is
blocking us. We immediately resolve blockers or help the person after standup.

We do this in order to:

- See each other face-to-face.
- Learn what others are doing so you can help them.
- Build accountability and trust.

## Trello
### Lists
- Next Up
- Ready for Development
- In Progress
- Code Review
- Ready for Production
- Bugs

In any task management system, it's important to have a view into the product
development process like this. The Next Up list is the single prioritized list
to which the product team refers in order to know what to work on next. It
represents one week of work.

A card represents a user story, bug fix, engineering task, or general todo.

Cards start out as a simple idea, 1-2 sentences long. As they are pulled through
boards, detail is added, explaining why (from a business perspective) we're
focusing on it, and maybe notes on suggested implementation (though designers
and developers may take or leave it at their discretion; it's supposed to be
helpful, not prescriptive).

Once the cards in the Next Up list have been prioritized and vetted, they are
ready for design and development. A designer or developer "puts their face on
it" by assigning it to themselves and pulling it into the In Progress list.

The cards in the In Progress list are actively being designed or developed.
Etiquette is that you should never have your face on more than two cards at a
time. Work is done in a [feature
branch](https://github.com/thoughtbot/guides/tree/master/protocol/git).

When a designer or developer creates a pull request for their feature branch,
they move the card to the Code Review list. Any reviewers "put their face on it"
while reviewing.

# Development
## Pair Programming

Code that is written by two people who sit next to each other at the same
computer is [pair-programmed](http://www.extremeprogramming.org/rules/pair.html)
code. That code is considered high quality and should result in cost savings due
to less maintenance.

In the long run, this style of development saves money because fewer bugs are
written and therefore do not need to be fixed later.

An indication that pairing is beneficial and should be done more often is the
following example:

> When you are writing an important piece of code, don't you want another person
> to look it over before it goes into production?

While we don't pair program 100% of the time, we recognize the difficulty in
acting as a team when we work at a distance from each other. There is no better
collaboration between designers, developers, or between designers and developers
than at the keyboard.

## Test-Driven Development

[Test-Driven Development
(TDD)](http://www.extremeprogramming.org/rules/testfirst.html) is perhaps the
most important Extreme Programming (XP) rule that we practice.

Business benefits of TDD:

- Deliver more value, faster
- Always ship working software
- Adapt to change quickly

Code benefits of TDD:

- Readable specs and code
- Clean public interfaces
- Decoupled modules

Process benefits of TDD:

- Regression safety net
- Fearless refactoring
- Team trust

At a high level, how to test is very simple:

- Write test first.
- Red-Green-Refactor cycle.

## Acceptance Tests

Acceptance tests are code created from feature stories. This code is run against
the application. When executed for the first time, the test will fail. The
developer writes application code until the test passes.

When the test passes, the developer commits the code into version control with a message such as:

> Guest creates pledge

When the acceptance test is green for you and any other designers, developers,
or clients are satisfied that the feature story is complete on staging, the feature
can be deployed to production at will. This can result in features being pushed
to production very frequently, and therefore more value is being delivered to
customers sooner.

## Refactoring

The third step of the "red, green, refactor" step is refactoring, the process of
improving the design of existing code without altering its external behavior.
It's a critical step in the process, but often overlooked.

## Code Reviews

Here's the flow. Read [the git
protocol](https://github.com/thoughtbot/guides/tree/master/protocol) for the git
commands.

1.  Create a local feature branch based off master.
2.  When feature is complete and tests pass, stage the changes.
3.  When you've staged the changes, commit them.
4.  Write a [good commit
    message](http://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)
5.  Share your branch.
6.  Submit a [GitHub pull
    request](https://help.github.com/articles/using-pull-requests/).
7.  Ask for a code review in Slack.
8.  A team member other than the author reviews the pull request. They follow
    [Code Review](https://github.com/thoughtbot/guides/blob/master/code-review)
    guidelines to avoid miscommunication.
9.  They make comments and ask questions directly on lines of code in the GitHub
    web interface or in Slack.
10. When satisfied, they comment on the pull request "Ready to merge."
11. Rebase interactively. Squash commits like "Fix whitespace" into one or a
    small number of valuable commit(s). Edit commit messages to reveal intent.
12. View a list of new commits. View changed files. Merge branch into master.
13. Delete your remote feature branch.
14. Delete your local feature branch.

Test-Driven Development moves code failure earlier in the development process.
It's better to have a failing test on your development machine than in
production. It also allows you to have tighter feedback cycles.

Code reviews that happen right before code goes into master offer similar
benefits:

- The whole team learns about new code as it is written.
- Mistakes are caught earlier.
- Coding standards are more likely to be established, discussed, and followed.
- Feedback from this style of code review is far more likely to be applied.
- No one forgets context ("Why did we write this?") since it's fresh in the
  author's mind.
