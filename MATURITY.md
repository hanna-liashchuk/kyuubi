<!--
 - Licensed to the Apache Software Foundation (ASF) under one or more
 - contributor license agreements.  See the NOTICE file distributed with
 - this work for additional information regarding copyright ownership.
 - The ASF licenses this file to You under the Apache License, Version 2.0
 - (the "License"); you may not use this file except in compliance with
 - the License.  You may obtain a copy of the License at
 -
 -   http://www.apache.org/licenses/LICENSE-2.0
 -
 - Unless required by applicable law or agreed to in writing, software
 - distributed under the License is distributed on an "AS IS" BASIS,
 - WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 - See the License for the specific language governing permissions and
 - limitations under the License.
 -->

# Apache Kyuubi(Incubating) Maturity Self Assessment

## Overview

This is an assessment of the overall maturity of Apache Kyuubi(Incubating) as an Apache project, meant to inform the decision (of mentors, community, incubator PMCs, and ASF Board of Directors) to graduate Kyuubi as a top-level Apache project. It is based on the [Apache Project Maturity Model](https://community.apache.org/apache-way/apache-project-maturity-model.html).

Mentors and community members are encouraged to contribute to this page and comment on it, the following tables summarize our self-assessment against the **Apache Project Maturity Model**.

:white_check_mark: means that the related item is in good status.
:white_large_square: means that the related item need long-term attention.
:x: means that the related item need to be fixed ASAP.


## Code

| ID  | Description                                                                                                                                                                                                                                                     | Status                                                                                                                                                                                                                                                                                                                                                                                              |
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C10 | The project produces Open Source software for distribution to the public, at no charge.                                                                                                                                                                         | :white_check_mark: The project source code is licensed under the [Apache License, v2.0](https://github.com/apache/incubator-kyuubi/blob/master/LICENSE)                                                                                                                                                                                                                                             |
| C20 | Anyone can easily discover and access the project's code.                                                                                                                                                                                                       | :x: The source code is available on GitHub directly, :bangbang: Missing link on website                                                                                                                                                                                                                                                                                                             |
| C30 | Anyone using standard, widely-available tools, can build the code in a reproducible way.                                                                                                                                                                        | :x: The source code is automatically built for each Pull Request commit, with license checks, style checks, doc builds, unit and end to end tests, via GitHub actions and Travis. Development environment setup and build instructions to do the same locally are documented on the [website](https://kyuubi.apache.org/developer-tools.html). :bangbang: The site is not synced with the codebase. |
| C40 | The full history of the project's code is available via a source code control system, in a way that allows anyone to recreate any released version.                                                                                                             | :white_check_mark: The project uses git to manage source code, documentation and website, all releases are tagged. The commit history is available from the beginning of the project.                                                                                                                                                                                                               |
| C50 | The source code control system establishes the provenance of each line of code in a reliable way, based on strong authentication of the committer. When third parties contribute code, commit messages provide reliable information about the code provenance.  | :white_check_mark: The project uses GitHub repository managed by Apache Infra, it ensuring the provenance of each line of code to a committer. All code is checked in after review and approval via GitHub pull requests.                                                                                                                                                                           |

## Licenses and Copyright

| ID   | Description                                                                                                                                                                       | Status                                                                                                                                                                                                                                            |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LC10 | The Apache License, version 2.0, covers the released code.                                                                                                                        | :white_check_mark: The [LICENSE file](https://github.com/apache/incubator-kyuubi/blob/master/LICENSE) is in GitHub repository. [All releases](https://kyuubi.apache.org/releases.html) are verified by IPMC to contain the copy.                  |
| LC20 | Libraries that are mandatory dependencies of the project's code do not create more restrictions than the Apache License does.                                                     | :white_check_mark: [The list of mandatory dependencies](https://github.com/apache/incubator-kyuubi/tree/master/licenses-binary) have been reviewed to contain approved and compatible licenses only.                                              |
| LC30 | The libraries mentioned in LC20 are available as Open Source software.                                                                                                            | :white_check_mark: All mandatory dependencies listed in L20 are available as open source software.                                                                                                                                                |
| LC40 | Committers are bound by an Individual Contributor Agreement (the "Apache iCLA") that defines which code they may commit and how they need to identify code that is not their own. | :white_check_mark: All committers have iCLAs on file before they have an apache account.                                                                                                                                                          |
| LC50 | The project clearly defines and documents the copyright ownership of everything that the project produces.                                                                        | :white_check_mark: All files in the source repository have appropriate headers. [The Github workflow](https://github.com/apache/incubator-kyuubi/actions/workflows/license.yml) is in place to ensure every file has the expected license header. |

## Releases

| ID   | Description                                                                                                                                                            | Status                                                                                                                                                                                                                                                                                    |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RE10 | Releases consist of source code, distributed using standard and open archive formats that are expected to stay readable in the long term.                              | :white_check_mark: Recent releases are available via the [download page](https://kyuubi.apache.org/releases.html) on the website. All releases are available via the [apache archive](https://archive.apache.org/dist/incubator/kyuubi/).                                                 |
| RE20 | The project's PMC (Project Management Committee, see CS10) approves each software release in order to make the release an act of the Foundation.                       | :white_check_mark: All incubating releases have been approved by the Kyuubi community and the Incubator, all with at least 3 PPMC/IPMC votes and more +1 than -1.                                                                                                                         |
| RE30 | Releases are signed and/or distributed along with digests that anyone can reliably use to validate the downloaded archives.                                            | :white_check_mark: [Releases](https://kyuubi.apache.org/releases.html) are signed, the [keys](https://downloads.apache.org/incubator/kyuubi/KEYS) are available from the download page. Every release has a corresponding hash(sha512) to prevent content tampering.                      |
| RE40 | The project can distribute convenience binaries alongside source code, but they are not Apache Releases, they are provided with no guarantee.                          | :white_check_mark: Convenience binaries are distributed alongside source code at the same time via <ul><li>[Maven Central Repository](https://mvnrepository.com/artifact/org.apache.kyuubi)</li><li>[DockerHub](https://hub.docker.com/r/apache/kyuubi)</li><li>dist.apache.org</li></ul> |
| RE50 | The project documents a repeatable release process so that someone new to the project can independently generate the complete set of artifacts required for a release. | :white_check_mark: [Release guide](https://github.com/apache/incubator-kyuubi/blob/master/docs/community/release.md) is available. The releases of the project have been performed by 4 different release managers.                                                                       |

## Quality

| ID   | Description                                                                                                                                                                                    | Status                                                                                                                                                           |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| QU10 | The project is open and honest about the quality of its code. Various levels of quality and maturity for various modules are natural and acceptable as long as they are clearly communicated.  | :white_check_mark: All issues are tracked on Kyuubi's GitHub [Issues](https://github.com/apache/incubator-kyuubi/issues).                                        |
| QU20 | The project puts a very high priority on producing secure software.                                                                                                                            | :white_check_mark: Security issues are treated with the highest priority. We use Apache's default way to submit security related information.                    |
| QU30 | The project provides a well-documented, secure and private channel to report security issues, along with a documented way of responding to them.                                               | :white_check_mark: Website provides a link to https://www.apache.org/security/                                                                                   |
| QU40 | The project puts a high priority on backwards compatibility and aims to document any incompatible changes and provide tools and documentation to help users transition to new features.        | :white_check_mark: Each release note contains all related issues and pull requests in the milestone, and extract mainly updates and API changes from milestones. |
| QU50 | The project strives to respond to documented bug reports in a timely manner.                                                                                                                   | :white_check_mark: The community is very active in responding to bug reports and usually fixes them within a short time period.                                  |


## Community

| ID   | Description                                                                                                                                                            | Status                                                                                                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CO10 | The project has a well-known homepage that points to all the information required to operate according to this maturity model.                                         | :white_check_mark: The website describes of the project with download, user manual, technical details, how to contribute and team introduce.                                                                                          |
| CO20 | The community welcomes contributions from anyone who acts in good faith and in a respectful manner, and who adds value to the project.                                 | :white_large_square: Committers are really welcome contributions and the community is actively seeking for new committers. The community has elected 0 new PPMC members and 2 new committers during incubation, based on meritocracy. |
| CO30 | Contributions include source code, documentation, constructive bug reports, constructive discussions, marketing and generally anything that adds value to the project. | :white_check_mark: The community welcomes all contributions. The contribution guide refers to non source code contribution. The community is very clear about contributions being more than code.                                     |
| CO40 | The community strives to be meritocratic and gives more rights and responsibilities to contributors who, over time, add value to the project.                          | :white_large_square:. The community has elected 0 new PPMC members and 2 new committers during incubation, based on meritocracy.                                                                                                      |
| CO50 | The project documents how contributors can earn more rights such as commit access or decision power, and applies these principles consistently.                        | :x: ~The process to become a committer or PPMC member is documented on the website~. see, https://community.apache.org/newcommitter.html                                                                                              |
| CO60 | The community operates based on consensus of its members (see CS10) who have decision power. Dictators, benevolent or not, are not welcome in Apache projects.         | :white_large_square: The project works to build consensus. All PPMC votes have been unanimous so far.                                                                                                                                 |
| CO70 | The project strives to answer user questions in a timely manner.                                                                                                       | :white_large_square: The project typically provides detailed answers to user questions within a few days via dev mailing list, GitHub issues and Github Discussions.                                                                  |

## Consensus Building

| ID   | Description                                                                                                                                                                                                               | Status                                                                                                                                                                                                            |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CS10 | The project maintains a public list of its contributors who have decision power. The project's PMC (Project Management Committee) consists of those contributors.                                                         | :x: ~Committers and PPMC members are listed on the website’s community page~                                                                                                                                      |
| CS20 | Decisions require a consensus among PMC members and are documented on the project's main communications channel. The PMC takes community opinions into account, but the PMC has the final word.                           | :white_check_mark: The project has been making important decisions on the mailing lists.                                                                                                                          |
| CS30 | The project uses documented voting rules to build consensus when discussion is not sufficient.                                                                                                                            | :white_check_mark: The project uses the standard ASF voting rules.                                                                                                                                                |
| CS40 | In Apache projects, vetoes are only valid for code commits. The person exercising the veto must justify it with a technical explanation, as per the Apache voting rules defined in CS30.                                  | :white_large_square: The project has not used a veto at any point during incubation.                                                                                                                              |
| CS50 | All "important" discussions happen asynchronously in written form on the project's main communications channel. Offline, face-to-face or private discussions that affect the project are also documented on that channel. | :white_large_square: The project has been making important decisions on the project mailing lists. Minor decisions may occasionally happen during code reviews, which are also asynchronous and in written form.  |

## Independence

| ID   | Description                                                                              | Status                                                                                                                                                                                                                                                                     |
|------|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IN10 | The project is independent from any corporate or organizational influence.               | :white_large_square: The project team gathers people from different companies (China Mobile, eBay, NetEase, T3). No company or organization has significantly more influence than any other. We can note a growth of the contributions coming from different contributors. |
| IN20 | Contributors act as themselves, not as representatives of a corporation or organization. | :white_check_mark: The contributors act on their own initiative without representing a corporation or organization.                                                                                                                                                        |
