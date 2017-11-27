# Tutorial: Continuous Integration for Serverless Applications

Continuous Integration is the practice of merging all working copies of
developer code into one shared mainline several times a day. Best practices
include automation of builds and deployments, with fast and self-testing
builds, as well as production-like testing environments. With serverless, the
continuous integration pipeline evolves from a one-lane, one-way street into a
multiple-lane, two-way highway.

In this tutorial, we take a simple serverless application and walk you through
the steps to set up unit testing, end-to-end testing, code coverage, code
analysis, code security, code performance, and peer code review. You can learn
how to use AWS serverless components in combination with GitHub, Travis-CI,
CodeClimate, Snyk and other serverless-friendly services.

## Getting Started

### Step 1: Your Serverless Application

> Step 1 Branch:
https://github.com/MitocGroup/tutorial-ci-for-serverless/tree/tutorial-step1

For this tutorial, we went with Single Page Application from
[todomvc.com](http://todomvc.com), transformed by our team into
[TodoMVC Serverless App](https://github.com/MitocGroup/deep-microservices-todomvc).
Similar approach can be applied to serverless applications described in
[Serverless Single Page Apps](https://pragprog.com/book/brapps/serverless-single-page-apps)
or [Serverless Stack](https://serverless-stack.com),
as well as any other serverless applications from
[Curated List of Awesome Serverless](https://github.com/anaibol/awesome-serverless).

```shell
# download locally todomvc serverless application codebase
git clone git@github.com:MitocGroup/deep-microservices-todomvc.git

# download locally tutorial repository codebase
git clone git@github.com:MitocGroup/tutorial-ci-for-serverless.git

# copy serverless application into a new branch, part of tutorial repository
cd ./tutorial-ci-for-serverless
git checkout -b tutorial-step1
cp -R ../deep-microservices-todomvc/src ../deep-microservices-todomvc/bin .
git commit -a -m "initial serverless application"
git push --set-upstream origin tutorial-step1
```

[Click to Continue with Next Step](https://github.com/MitocGroup/tutorial-ci-for-serverless/tree/tutorial-step2#step-2-setup-travis-ci)