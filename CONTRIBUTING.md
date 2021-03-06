

**Currently contribution needed**

Legal (especially Blockchain, Crypto, ICO)
Tax Advising (especially Blockchain, Crypto, ICO)
Marketers (especially Blockchain, Crypto, ICO)

All other expertise are welcome. 


**How to contribute**

Third-party patches are essential for keeping imusify great. We want to keep it as easy as possible to contribute changes that get things working in your environment. There are a few guidelines that we need contributors to follow so that we can have a chance of keeping on top of things.


**Getting Started**

Anybody can contribute. Be creative. Work must be done first. 
Tasks and Issues can be found at https://github.com/imusify/imusify/issues
The best work will be rewarded generously. 
All Payments are made in $ IMU. You can see amount of rewards for the task within the issue. If there is no existing issue, you can create a new issue with an offer. 
If you find a bug please fix and let us know. 
Rewards will be paid out after committed and approved by imusify.


Make sure you have a GitHub account.
Submit a ticket for your issue, assuming one does not already exist.
Clearly describe the issue including steps to reproduce when it is a bug.
Make sure you fill in the earliest version that you know has the issue.
Fork the repository on GitHub.


**Making Changes**

Create a topic branch from where you want to base your work.

This is usually the master branch.
Only target release branches if you are certain your fix must be on that branch.
To quickly create a topic branch based on master, run git checkout -b fix/master/my_contribution master. Please avoid working directly on the master branch.
Make commits of logical units.

Check for unnecessary whitespace with git diff --check before committing.

Make sure your commit messages are in the proper format. 

    Make the example in CONTRIBUTING imperative and concrete

    Without this patch applied the example commit message in the CONTRIBUTING
    document is not a concrete example. This is a problem because the
    contributor is left to imagine what the commit message should look like
    based on a description rather than an example. This patch fixes the
    problem by making the example concrete and imperative.

    The first line is a real-life imperative statement with a ticket number
    from our issue tracker. The body describes the behavior without the patch,
    why this is a problem, and how the patch fixes the problem when applied.
    
Make sure you have added the necessary tests for your changes.

Run all the tests to assure nothing else was accidentally broken.


**Writing Translatable Code**

We use gettext tooling to extract user-facing strings and pull in translations based on the user's locale at runtime. In order for this tooling to work, all user-facing strings must be wrapped in the _() translation function, so they can be extracted into files for the translators.

When adding user-facing strings to your work, follow these guidelines:

Use full sentences. Strings built up out of concatenated bits are hard to translate.
Use string formatting instead of interpolation. For example: _('Creating new user %{name}.') % { name: user.name }
Use n_() for pluralization. (see gettext gem docs linked above for details)
It is the responsibility of contributors and code reviewers to ensure that all user-facing strings are marked in new PRs before merging.


**Making Trivial Changes**

Documentation

For changes of a trivial nature to comments and documentation, it is not always necessary to create a new ticket in Jira. In this case, it is appropriate to start the first line of a commit with (docs) instead of a ticket number.

If a Jira ticket exists for the documentation commit, you can include it after the (docs) token.

    (docs)(DOCUMENT-000) Add docs commit example to CONTRIBUTING

    There is no example for contributing a documentation commit
    to the Puppet repository. This is a problem because the contributor
    is left to assume how a commit of this nature may appear.

    The first line is a real-life imperative statement with '(docs)' in
    place of what would have been the PUP project ticket number in a
    non-documentation related commit. The body describes the nature of
    the new documentation or comments added.
    
For commits that address trivial repository maintenance tasks or packaging issues, start the first line of the commit with (maint) or (packaging), respectively.


**Submitting Changes**

Sign the Contributor License Agreement.
Push your changes to a topic branch in your fork of the repository.
Submit a pull request to the repository in the puppetlabs organization.
Update your Jira ticket to mark that you have submitted code and are ready for it to be reviewed (Status: Ready for Merge).
Include a link to the pull request in the ticket.
The core team looks at Pull Requests on a regular basis in a weekly triage meeting that we hold in a public Google Hangout. The hangout is announced in the weekly status updates that are sent to the puppet-dev list. Notes are posted to the Puppet Community community-triage repo and include a link to a YouTube recording of the hangout.
After feedback has been given we expect responses within two weeks. After two weeks we may close the pull request if it isn't showing any activity.


**Revert Policy**

By running tests in advance and by engaging with peer review for prospective changes, your contributions have a high probability of becoming long lived parts of the the project. After being merged, the code will run through a series of testing pipelines on a large number of operating system environments. These pipelines can reveal incompatibilities that are difficult to detect in advance.

If the code change results in a test failure, we will make our best effort to correct the error. If a fix cannot be determined and committed within 24 hours of its discovery, the commit(s) responsible may be reverted, at the discretion of the committer and Puppet maintainers. This action would be taken to help maintain passing states in our testing pipelines.

The original contributor will be notified of the revert in the Jira ticket associated with the change. A reference to the test(s) and operating system(s) that failed as a result of the code change will also be added to the Jira ticket. This test(s) should be used to check future submissions of the code to ensure the issue has been resolved.


**Summary**

Changes resulting in test pipeline failures will be reverted if they cannot be resolved within one business day.
