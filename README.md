NOTICE: This working group is in Emeritus status and no longer maintained

**Open z/OS Enablement, OzE**

**Vision:**

The purpose of the open z/OS enablement project is to capture several
work efforts to allow experienced sets of users to try innovative
ideas and other users to learn mainframe skills to increase
the vitality of the mainframe as its' software.

**Problem Statement:**

Lack of access to z environments is a major impediment to the growth and
innovation on the platform. Type of uses targeted include:

- Open Source Communities and new software development efforts\
- Mentoring and new user growth, consistent with and attractive
to those who use other public cloud learning opportunities\
- Experimentation and innovation on the edge of environment
stability like the Raspberry Pi Model\
   Impediments to these types of environments include:\
   - Critical knowledge and support in sysprogs for z systems\
   - Cost and control of donated resources (MIPs, software, storage,
etc.)\
   - Security and access control

This project intends to create code, processes and techniques which
reduce these impediments and enable broader use and development of the z
platform

**Core Requirements:**

The following gives a sense of Common Workstream elements no matter what
configuration is being provided:

1\. Software inventory of the z/OS instance or "Bill Of Materials" (BOM)

2\. Ability to request a known BOM instance and create a running
instance after applying required changes / additions (like users,
passwords, security tweaks, etc.) 

3\. Making the instance available to consumer such that the instance can
be quiesced, started, stopped or deleted.  (Quiesce presumes the user
could start it up again)

This is a common model used in things like Docker, Vagrant and other vm
image libraries and uses.

**Dimensional Requirements:**

Ways in which access to z/OS systems might be accessed has many
dimensions to it, some of which are shown below. The reasons for
identifying the dimensions was to identify the area of most need and
priority of attack to impact the most open source needs.

Sample Dimensions\
\
   Tenancy:  Multi-tenant vs. Single-tenant\
   Operation:  Emulated vs. Bare Metal\
   Hardware:  Donated Hardware vs. Owned Hardware\
   OS:  Operating system Choices (zVM, zLinux, z/OS, etc.)\
   Emulator: (zD&T, zPDT, zVM, Docker, Vagrant, other)\
   User Organization Type: (community, single company, multi company,
other)\
   Sysprog support model: (shared vs. independent)\

The many different dimensions to this problem would mean the project
would become difficult to manage in all the various aspects. After
several meetings, the following dimensions will be considered fixed for
most important cases:

- Mutli-tenant (single tenancy can be easier to handle)

- Community (single or multiple companies are easier)

- Both Analytical and Transaction workloads (Not critical for the
    tooling being considered)

- Multi month use (as opposed to very short usages)

This then reduced the project dimensions to this table. This matrix
could provide different ways of attacking the problem space.
|    <br>Complexity     |    <br>Environment   Use                                                                                                                                 |    <br>Emulated zPDT/zD&T                                        |    <br>Emulated<br>   <br>zPDT/zD&T                                                                                    |    <br>Z Hardware (either Bare Metal or z/VM)                                              |    <br>Z Hardware (either Bare Metal or z/VM)                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
|    <br>               |    <br>                                                                                                                                                  |    <br>Donated or Shared                                         |    <br>Owned                                                                                                           |    <br>Donated or Shared                                                                   |    <br>Owned                                                                 |
|    <br>Simple         |    <br>Shared   sysprog support required to establish the user’s z/OS environment<br>   <br>(For example   simply Unix System Services)                  |    <br>Perhaps z/OS   on AWS with IBM ZD&T Code as a template    |    <br>1 Perhaps z/OS   on AWS with IBM ZD&T Code as a template (target audience MF Novices)                           |    <br>1 Marist   College or VCU environment template, with donated REXX from a company    |    <br>Company   enables employee experimentation using company resources    |
|    <br>Medium         |    <br>Sysprog   activities required inside the user’s z/OS environment<br>   <br>(This is   typically TSO Access which require more Sysprog support)    |    <br>Perhaps z/OS   on AWS with IBM ZD&T Code as a template    |    <br>2 Perhaps z/OS   on AWS with IBM ZD&T Code as a template (target Audience is Medium to   High MF Experience)    |    <br>2 Marist   College or VCU environment template, with donated REXX from a company    |    <br>Company   enables employee experimentation using company resources    |
|    <br>Medium Plus    |    <br>Other   Licensed and Enterprise Tooling Additions (CICS, DB2, ACF2, Endeavor,   Compilers) etc.                                                   |    <br>                                                          |    <br>                                                                                                                |    <br>                                                                                    |    <br>                                                                      |
|    <br>Complex        |    <br>Physical   Resource Control (i.e., Sysplex Enablement)                                                                                            |    <br>                                                          |    <br>                                                                                                                |    <br>                                                                                    |    <br>                                                                      |

There are multiple areas that have a need for a work stream. The chart
above is attempting to determine what areas are of high priority and
will have the most impact for the open source community.  A major
consideration is to ensure that the releases are functional, easy
to use and do as intended before release. 

## Not Intended to Cover:

The following topics are not intended to be covered in this working
group:

- Access to z MIPs or to licensed software. The owners of those
    resources control them and contribute them directly to communities

- Management of donated resources. This project is intended to enable
    donation, making donation easier, and ensuring ownership control of
    resources is controlled by owners, but does not provide management
    of environments.

## Results of First Year of Effort

During the first year, the working group formulated the basic focus of the group, and explored the following:

- Made contact with groups for potential code donation for internal environment allocation routines as a starting point for building out Bare Metal or z/VM offering

- Explored owners of z/OS and emulators to consider contribution so other platforms may be supported or supplied for emulated offering

- Found that the more rare skills of Sysprog can be an impediment to the objectives of the project, as now often they shoulder the burden of new users

- Established a Slack Channel Z assembler community to share expertise that cuts across existing projects (z-assembler-community at https://openmainframeproject.slack.com/archives/C030QUUN39C)

No code contributions were made in the first year.

The working group believes they helped impact the Open Mainframe Project's goal set in early 2022 to provide Z infrastructure for open source projects (https://www.openmainframeproject.org/blog/2022/01/05/2022-goals-for-the-open-mainframe-project)

The working group is ready to assist when this infrastructure is in place to allow for efficient management and wide-spread use of the resource--the haulmarks of Z environments.

## News and Discussion

On Feburary 10, 2022, the Open Mainframe Project's Technial Advisor Committee (TAC) approved the continuation of the working group for another year.

You can connect with the community in a variety of ways\...

- [Public z
    enablement](https://wg-open-zos-enablement+subscribe@lists.openmainframeproject.org)

- [Join the conversation on Open Mainframe Project
    Slack](https://slack.openmainframeproject.org/)

- After requesting access with the above link, look for
    the [\#wg-open-zos-enablement
    channel](https://openmainframeproject.slack.com/archives/C01711931GA)

**Contributing**

Anyone can contribute to the z/OS open environment project - learn more
at [[CONTRIBUTING.md]{.ul}](https://github.com/openmainframeproject/wg-open-zos-enablement)

**Governance**

z/OS open environment is a project hosted by the [[Open Mainframe
Project]{.ul}](https://openmainframeproject.org/). This project has
established its\' own processes for managing day-to-day processes in the
project
at [[GOVERNANCE.md]{.ul}](https://github.com/openmainframeproject/wg-open-zos-enablement).

**Reporting Issues**

To report a problem, you can open
an [[issue]{.ul}](https://github.com/openmainframeproject/wg-open-zos-enablement/issues) in
repository against a specific workflow. If the issue is sensitive in
nature or a security related issue, please do not report in the issue
tracker but instead
email <wg-public-z-cloud+help@lists.openmainframeproject.org>.

## Meetings

See the [Open Mainframe Project public
calendar](https://lists.openmainframeproject.org/calendar). This WG
meets the frist Thursday of the month at 4:00 PM EST.

## Meeting notes

Meeting notes, recordings, and any presentations made during WG meetings
are
available [here](https://github.com/openmainframeproject/wg-open-zos-enablement/blob/master/meetings).
