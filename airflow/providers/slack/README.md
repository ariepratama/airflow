<!--
 Licensed to the Apache Software Foundation (ASF) under one
 or more contributor license agreements.  See the NOTICE file
 distributed with this work for additional information
 regarding copyright ownership.  The ASF licenses this file
 to you under the Apache License, Version 2.0 (the
 "License"); you may not use this file except in compliance
 with the License.  You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing,
 software distributed under the License is distributed on an
 "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
 KIND, either express or implied.  See the License for the
 specific language governing permissions and limitations
 under the License.
 -->


# Package apache-airflow-backport-providers-slack

Release: 2020.9.7

**Table of contents**

- [Backport package](#backport-package)
- [Installation](#installation)
- [PIP requirements](#pip-requirements)
- [Cross provider package dependencies](#cross-provider-package-dependencies)
- [Provider class summary](#provider-classes-summary)
    - [Operators](#operators)
        - [New operators](#new-operators)
        - [Moved operators](#moved-operators)
    - [Hooks](#hooks)
        - [Moved hooks](#moved-hooks)
- [Releases](#releases)
    - [Release 2020.9.7](#release-202097)
    - [Release 2020.6.24](#release-2020624)

## Backport package

This is a backport providers package for `slack` provider. All classes for this provider package
are in `airflow.providers.slack` python package.

**Only Python 3.6+ is supported for this backport package.**

While Airflow 1.10.* continues to support Python 2.7+ - you need to upgrade python to 3.6+ if you
want to use this backport package.



## Installation

You can install this package on top of an existing airflow 1.10.* installation via
`pip install apache-airflow-backport-providers-slack`

## PIP requirements

| PIP package   | Version required   |
|:--------------|:-------------------|
| slackclient   | &gt;=2.0.0,&lt;3.0.0     |

## Cross provider package dependencies

Those are dependencies that might be needed in order to use all the features of the package.
You need to install the specified backport providers package in order to use them.

You can install such cross-provider dependencies when installing from PyPI. For example:

```bash
pip install apache-airflow-backport-providers-slack[http]
```

| Dependent package                                                                                              | Extra   |
|:---------------------------------------------------------------------------------------------------------------|:--------|
| [apache-airflow-backport-providers-http](https://github.com/apache/airflow/tree/master/airflow/providers/http) | http    |

# Provider classes summary

In Airflow 2.0, all operators, transfers, hooks, sensors, secrets for the `slack` provider
are in the `airflow.providers.slack` package. You can read more about the naming conventions used
in [Naming conventions for provider packages](https://github.com/apache/airflow/blob/master/CONTRIBUTING.rst#naming-conventions-for-provider-packages)


## Operators


### New operators

| New Airflow 2.0 operators: `airflow.providers.slack` package                                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------|
| [operators.slack.SlackAPIFileOperator](https://github.com/apache/airflow/blob/master/airflow/providers/slack/operators/slack.py) |


### Moved operators

| Airflow 2.0 operators: `airflow.providers.slack` package                                                                                         | Airflow 1.10.* previous location (usually `airflow.contrib`)                                                                                                             |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [operators.slack.SlackAPIOperator](https://github.com/apache/airflow/blob/master/airflow/providers/slack/operators/slack.py)                     | [operators.slack_operator.SlackAPIOperator](https://github.com/apache/airflow/blob/v1-10-stable/airflow/operators/slack_operator.py)                                     |
| [operators.slack.SlackAPIPostOperator](https://github.com/apache/airflow/blob/master/airflow/providers/slack/operators/slack.py)                 | [operators.slack_operator.SlackAPIPostOperator](https://github.com/apache/airflow/blob/v1-10-stable/airflow/operators/slack_operator.py)                                 |
| [operators.slack_webhook.SlackWebhookOperator](https://github.com/apache/airflow/blob/master/airflow/providers/slack/operators/slack_webhook.py) | [contrib.operators.slack_webhook_operator.SlackWebhookOperator](https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/operators/slack_webhook_operator.py) |


## Hooks



### Moved hooks

| Airflow 2.0 hooks: `airflow.providers.slack` package                                                                                 | Airflow 1.10.* previous location (usually `airflow.contrib`)                                                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [hooks.slack.SlackHook](https://github.com/apache/airflow/blob/master/airflow/providers/slack/hooks/slack.py)                        | [hooks.slack_hook.SlackHook](https://github.com/apache/airflow/blob/v1-10-stable/airflow/hooks/slack_hook.py)                                        |
| [hooks.slack_webhook.SlackWebhookHook](https://github.com/apache/airflow/blob/master/airflow/providers/slack/hooks/slack_webhook.py) | [contrib.hooks.slack_webhook_hook.SlackWebhookHook](https://github.com/apache/airflow/blob/v1-10-stable/airflow/contrib/hooks/slack_webhook_hook.py) |



## Releases

### Release 2020.9.7

| Commit                                                                                         | Committed   | Subject                                                                       |
|:-----------------------------------------------------------------------------------------------|:------------|:------------------------------------------------------------------------------|
| [720912f67](https://github.com/apache/airflow/commit/720912f67b3af0bdcbac64d6b8bf6d51c6247e26) | 2020-10-02  | Strict type check for multiple providers (#11229)                             |
| [0161b5ea2](https://github.com/apache/airflow/commit/0161b5ea2b805d62a0317e5cab6f797b92c8abf1) | 2020-09-26  | Increasing type coverage for multiple provider (#11159)                       |
| [f3e87c503](https://github.com/apache/airflow/commit/f3e87c503081a3085dff6c7352640d7f08beb5bc) | 2020-09-22  | Add D202 pydocstyle check (#11032)                                            |
| [9549274d1](https://github.com/apache/airflow/commit/9549274d110f689a0bd709db829a4d69e274eed9) | 2020-09-09  | Upgrade black to 20.8b1 (#10818)                                              |
| [fdd9b6f65](https://github.com/apache/airflow/commit/fdd9b6f65b608c516b8a062b058972d9a45ec9e3) | 2020-08-25  | Enable Black on Providers Packages (#10543)                                   |
| [d1bce91bb](https://github.com/apache/airflow/commit/d1bce91bb21d5a468fa6a0207156c28fe1ca6513) | 2020-08-25  | PyDocStyle: Enable D403: Capitalized first word of docstring (#10530)         |
| [3696c34c2](https://github.com/apache/airflow/commit/3696c34c28c6bc7b442deab999d9ecba24ed0e34) | 2020-08-24  | Fix typo in the word &#34;release&#34; (#10528)                                       |
| [2f2d8dbfa](https://github.com/apache/airflow/commit/2f2d8dbfafefb4be3dd80f22f31c649c8498f148) | 2020-08-25  | Remove all &#34;noinspection&#34; comments native to IntelliJ (#10525)                |
| [ee7ca128a](https://github.com/apache/airflow/commit/ee7ca128a17937313566f2badb6cc569c614db94) | 2020-08-22  | Fix broken Markdown refernces in Providers README (#10483)                    |
| [cdec30125](https://github.com/apache/airflow/commit/cdec3012542b45d23a05f62d69110944ba542e2a) | 2020-08-07  | Add correct signature to all operators and sensors (#10205)                   |
| [aeea71274](https://github.com/apache/airflow/commit/aeea71274d4527ff2351102e94aa38bda6099e7f) | 2020-08-02  | Remove `args` parameter from provider operator constructors (#10097)          |
| [7cc1c8bc0](https://github.com/apache/airflow/commit/7cc1c8bc0031f1d9839baaa5a6c7a9bc7ec37ead) | 2020-07-25  | Updates the slack WebClient call to use the instance variable - token (#9995) |
| [33f0cd265](https://github.com/apache/airflow/commit/33f0cd2657b2e77ea3477e0c93f13f1474be628e) | 2020-07-22  | apply_default keeps the function signature for mypy (#9784)                   |
| [df8efd04f](https://github.com/apache/airflow/commit/df8efd04f394afc4b5affb677bc78d8b7bd5275a) | 2020-06-21  | Enable &amp; Fix &#34;Docstring Content Issues&#34; PyDocStyle Check (#9460)              |
| [d0e7db402](https://github.com/apache/airflow/commit/d0e7db4024806af35e3c9a2cae460fdeedd4d2ec) | 2020-06-19  | Fixed release number for fresh release (#9408)                                |


### Release 2020.6.24

| Commit                                                                                         | Committed   | Subject                                                                       |
|:-----------------------------------------------------------------------------------------------|:------------|:------------------------------------------------------------------------------|
| [12af6a080](https://github.com/apache/airflow/commit/12af6a08009b8776e00d8a0aab92363eb8c4e8b1) | 2020-06-19  | Final cleanup for 2020.6.23rc1 release preparation (#9404)                    |
| [c7e5bce57](https://github.com/apache/airflow/commit/c7e5bce57fe7f51cefce4f8a41ce408ac5675d13) | 2020-06-19  | Prepare backport release candidate for 2020.6.23rc1 (#9370)                   |
| [f6bd817a3](https://github.com/apache/airflow/commit/f6bd817a3aac0a16430fc2e3d59c1f17a69a15ac) | 2020-06-16  | Introduce &#39;transfers&#39; packages (#9320)                                        |
| [5cf46fad1](https://github.com/apache/airflow/commit/5cf46fad1e0a9cdde213258b2064e16d30d3160e) | 2020-05-29  | Add SlackAPIFileOperator impementing files.upload from Slack API (#9004)      |
| [0b0e4f7a4](https://github.com/apache/airflow/commit/0b0e4f7a4cceff3efe15161fb40b984782760a34) | 2020-05-26  | Preparing for RC3 release of backports (#9026)                                 |
| [00642a46d](https://github.com/apache/airflow/commit/00642a46d019870c4decb3d0e47c01d6a25cb88c) | 2020-05-26  | Fixed name of 20 remaining wrongly named operators. (#8994)                   |
| [427257c2e](https://github.com/apache/airflow/commit/427257c2e2ffc886ef9f516e9c4d015a4ede9bbd) | 2020-05-24  | Remove defunct code from setup.py (#8982)                                     |
| [375d1ca22](https://github.com/apache/airflow/commit/375d1ca229464617780623c61c6e8a1bf570c87f) | 2020-05-19  | Release candidate 2 for backport packages 2020.05.20 (#8898)                  |
| [12c5e5d8a](https://github.com/apache/airflow/commit/12c5e5d8ae25fa633efe63ccf4db389e2b796d79) | 2020-05-17  | Prepare release candidate for backport packages (#8891)                       |
| [f3521fb0e](https://github.com/apache/airflow/commit/f3521fb0e36733d8bd356123e56a453fd37a6dca) | 2020-05-16  | Regenerate readme files for backport package release (#8886)                  |
| [92585ca4c](https://github.com/apache/airflow/commit/92585ca4cb375ac879f4ab331b3a063106eb7b92) | 2020-05-15  | Added automated release notes generation for backport operators (#8807)       |
| [578fc514c](https://github.com/apache/airflow/commit/578fc514cd325b7d190bdcfb749a384d101238fa) | 2020-05-12  | [AIRFLOW-4543] Update slack operator to support slackclient v2 (#5519)        |
| [4bde99f13](https://github.com/apache/airflow/commit/4bde99f1323d72f6c84c1548079d5e98fc0a2a9a) | 2020-03-23  | Make airflow/providers pylint compatible (#7802)                              |
| [be2b2baa7](https://github.com/apache/airflow/commit/be2b2baa7c5f53c2d73646e4623cdb6731551b70) | 2020-03-23  | Add missing call to Super class in &#39;http&#39;, &#39;grpc&#39; &amp; &#39;slack&#39; providers (#7826) |
| [97a429f9d](https://github.com/apache/airflow/commit/97a429f9d0cf740c5698060ad55f11e93cb57b55) | 2020-02-02  | [AIRFLOW-6714] Remove magic comments about UTF-8 (#7338)                      |
| [9a04013b0](https://github.com/apache/airflow/commit/9a04013b0e40b0d744ff4ac9f008491806d60df2) | 2020-01-27  | [AIRFLOW-6646][AIP-21] Move protocols classes to providers package (#7268)    |
| [c42a375e7](https://github.com/apache/airflow/commit/c42a375e799e5adb3f9536616372dc90ff47e6c8) | 2020-01-27  | [AIRFLOW-6644][AIP-21] Move service classes to providers package (#7265)      |
