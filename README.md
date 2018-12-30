# KEEP-math
A community-driven specification process for mathematics libraries in Kotlin

The purpose of this repository is to collect the ideas and use-cases for mathematics in Kotlin. And then create and support an API (or set of APIs) for further development. Also this repository will hold discussions on integration of different mathematical libraries and different implementations of proposals.

## Workflow
The workflow for this repository is similar to the one for general [Kotlin KEEP](https://github.com/Kotlin/KEEP). Requests and general proposals are discussed in issue section, while fully-formed contributions are made by pull-request of a document to appropriate section. The pull requests are discussed and then accepted or rejected by community.

## Discussion
The discussion for mathematics is done in [Kotlin slack](https://kotlinlang.slack.com) in ][#mathematics](https://kotlinlang.slack.com/messages/CE5HPKBRN/) and [#science](https://kotlinlang.slack.com/messages/CEXV2QWNM) channels.

## Sections
Currently repository contains following sections:

* **api** - the resulting accepted description of API and reference to the repository API code and possible reference implementation. Pull requests into this section are made only after approval of community.
* **features** - description of features to be added to API. New proposals go here. It is possible to have contradicting features in this directory. In this case some of them will be marked as **approved** and some as **rejected** later.
* **implementations** - a references to existing implementations of API and fully formed requests to add implementation (port existing library to API).
* **use-cases** - an example use-case for mathematic construct in programming. The example must describe mathematic or textual notation of the problem and field of application. All applications must be real-life examples.

## Workflow
Basic worflow for new features is the following. First an example use is posted to **use-cases** directory. Then more specific proposal is posted to **features** directory. Complete API description and reference is posted to **api**. When an external library implements the api, the appropriate **implementations** document is updated.

## Conflict resolution an community
Conflicts of opinion are unavoidable part of development. So they are expected in this project as well. At first stage conflicts are supposed to be resolved peacefully and politely by community members. Later independent referee will be probably invited to resolve such issues.
