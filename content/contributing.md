---
title: "Contributing"
date: 2019-01-29T09:46:31+02:00
draft: false
---

# HowTo contribute to Eclipse Kuksa
Great that you are interested in contributing to Eclipse Kuksa. 
We really looking forward to receive your contribution.

In the project we agreed upon the following approach to add contributions to the project.

1. Meet the Definition of Done (DoD)
2. A review took place for the code
3. The new feature was at least once tested manually, deployed to a running test instance
4. Clearly outline third party dependencies

### Definition of Done
First, we have DoD for solved issues. Please check if you met all the items in the following list:

* File headers in file OK (see section License Headers for details)
  * EPL-2.0 license header
  * Or, if the file is too small, configuration file: license note (see code style)
  * Copyright and author

* New feature is in dev branch
  * Please use conventional branch names, which help to see who is responsible and to which issue the Pull Request corresponds
  * Should look like`<github-nickname>/<issue>/<description>`, e.g. bs-jokri/#2/fix-connection-handling
    
* Avoid (serious) compiler warnings

* New test
  * For new / added functionality

* No breaking test
  * Unit testing as it is already present
  * You have more - use them!

* Documentation
  * in the Github Wiki-Section, if you have done something new
  * At least a technical note for newly added functionality

* Commit style
  * Squash your commits into one or more logical units of work. No dozens of hourly/daily commits in your pull request, please. In the ideal case, a feature is contained in one commit.
  * Rebase onto current master so that a fast forward merge is possible, i.e. prepare merge to master.
  * If you are not a committer to the project our commits need to be signed of with a valid Eclipse user account. Check the Eclipse handbook for details ([Eclipse Project Handbook](https://www.eclipse.org/projects/handbook/#resources-commit)).

If you checked your code according to the DoD and you feel it can be merged to master, please create a PR to master. 
Each PR that is merged to master has to pass all tests and needs a code review of some other person of the project that looks onto your contribution from another angle, 
i.e. didn't work with you on the new feature. Probably a good idea is to have someone from another organization doing the review.
Maybe you already have someone in mind doing the review, then request a review from this person via the github review functionallity.
 
### Review
If you conduct a code review, please look at the following issues:

  * Is code style ok, not really formatting, but issues like style attributes in HTML tags or exception handling useful
  * Are DoD items reached
  * Are there any design / architecture issues
  * Does the new feature fit the overall project goal, is it suitable for the community

### Manual Test
If applicable the new  feature should at least be deployed and tested by someone before actually merged to master.
This could be done by the same person that is doing the review but could be performed  by another person.


After review and tests are finished it should be documented who actually did the review and the test.
Do this with the following lines in the comments of the PR.
```
review-by:email@domain.com
```
and
```
tested-by:email@domain.com
```

### Third party dependencies

If you use third party content (import / include ...), you are required to list each third party content explicitly with its version number in the documentation or your pull-request comment.
Please note that GPL software cannot be approved for Eclipse Kuksa.

### Licensing and file header

All files contributed require headers - this will ensure the license and copyright clearing at the end. Also, all contributions must have the same license as the original source.

If a file has relevant functionality add the official EPL-2.0 header as described here
https://www.eclipse.org/legal/epl-2.0/faq.php#h.q72cnghf29k0

We recommend to use the releng copyright tool at:
https://wiki.eclipse.org/Development_Resources/How_to_Use_Eclipse_Copyright_Tool


```
/*********************************************************************
* Copyright (c) {date} {owner} [and others]
*
* This program and the accompanying materials are made
* available under the terms of the Eclipse Public License 2.0
* which is available at https://www.eclipse.org/legal/epl-2.0/
*
* SPDX-License-Identifier: EPL-2.0
**********************************************************************/
```
(please adapt comment characters usage)

For small files such as property files, configuration files or standard XML files:

```
# Copyright <COPYRIGHT_HOLDER>, <YEAR>. Part of the Eclipse Kuksa Project.
#
# All rights reserved. This configuration file is provided to you under the
# terms and conditions of the Eclipse Distribution License v1.0 which
# accompanies this distribution, and is available at
# http://www.eclipse.org/org/documents/edl-v10.php
```