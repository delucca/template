# Issues

* [Asking for general help](#asking-for-general-help)
* [Submitting a bug report](#submitting-a-bug-report)
* [Proposing new features](#proposing-new-features)

## Asking for general help

To avoid mixing issues and feature requests with general questions and help requests, we've enabled the [discussions tab][discussions-tab]. There, you can start a new discussions, in the `Q&A` category, explaining your question. A member of our comunity will gladly answer your question there.

## Submitting a bug report

It's complicated to ensure quality and prevent unexpected bugs. There are so many corner cases that is impossible to prevent bugs from happening. So, one of the most important contributions you can give us is reporting issues and bugs.

Reporting bugs is not a simple task. Is not a simple "feedback form" where you can just type what happened and we will evaluate. While reporting bugs you need to keep in mind that **we need to reproduce your issue**, so, we need as much information you can give us.

The two most important pieces of information we need in order to properly evaluate the report is a description of the behavior you are seeing and a simple test case we can use to recreate the problem on our own. If we cannot recreate the issue, it becomes impossible for us to fix.

In order to rule out the possibility of bugs introduced by userland code, test cases should be limited, as much as possible, to using the minimum dependencies as possible. See [How to create a Minimal, Complete, and Verifiable example][creating-mcve].

To make it easier for our users, we [have a `bug-report` template][template-bug-report] that you can use while reporting a bug (you can select it while writting your issue). Please, fill all the sections while doing so.

## Proposing new features

Our system is only useful if it does what our users want. A huge part of our job is to prioritize the most relevant feature requests to code.

You can contribute to us by adding new issues with [the `feature-request` template][template-feature-request], where you can explain your idea, and what you want our system to solve that is not currently being solved yet.

Although our primary focus is in our users, keep in mind that some proposed features could be either too complex, or not even related to our primary domain. So, creating a feature request has no guarantee that it would be developed by our team.

[discussions-tab]: ./discussions
[creating-mcve]: https://stackoverflow.com/help/mcve
[template-bug-report]: .github/ISSUE_TEMPLATE/bug-report.md