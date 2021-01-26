**Open zOS Enablement**

**Vision:**

The purpose of the z/OS open environment project is to capture several
work efforts to enable different sets of users to experiment with
innovative ideas and other users to learn mainframe skills to increase
the vitality of the mainframe as its’ software.

**Problem Statement:**

Lack of access to z environments is a major impediment to the growth and
innovation on the platform. Type of uses targeted include:

       - Open Source Communities and new software development efforts  
       - Mentoring and new user growth, consistent with and attractive
to those who use other public cloud learning opportunities  
       - Experimentation and innovation on the edge of environment
stability like the Raspberry Pi Model  
   Impediments to these types of environments include:  
       - Critical knowledge and support in sysprogs for z systems  
       - Cost and control of donated resources (MIPs, software, storage,
etc.)  
       - Security and access control

This project intends to create code, processes and techniques which
reduce these impediments and enable broader use and development of the z
platform

**Core Requirements:**

The following gives a sense of Common Workstream elements no matter what
configuration is being provided:

1\. Software inventory of the z/OS instance or “Bill Of Materials” (BOM)

2\. Ability to request a known BOM instance and create a running
instance after applying required changes / additions (like users,
passwords, security tweaks, etc.) 

3\. Making the instance available to consumer such that the instance can
be quiesced, started, stopped or deleted.  (Quiesce presumes the user
could start it up again)

This is a common model used in things like Docker, Vagrant and other vm
image libraries and uses.

**Dimensional Requirements:**

Ways in which access to z/OS systems might be available has many
dimensions to it, some of which are shown below. 

Sample Dimensions  
  
   Tenancy:  Multi-tenant vs. Single-tenant  
   Operation:  Emulated vs. Bare Metal  
   Hardware:  Donated Hardware vs. Owned Hardware  
   OS:  Operating system Choices (zVM, zLinux, z/OS, etc.)  
   Emulator: (zD&T, zPDT, zVM, Docker, Vagrant, other)  
   User Organization Type: (community, single company, multi company,
other)  
   Sysprog support model: (shared vs. independent)  
 

The many different dimensions to this problem would mean the project
would become difficult to manage in all the various aspects. After
several meetings, the following dimensions have been considered fixed for
most important cases:

-   Mutli-tenant (single tenancy can be easier to handle)

-   Community (single or multiple companies are easier)

-   Both Analytical and Transaction workloads (Not critical for the
    tooling being considered)

-   Multi month use (as opposed to very short usages)

This then reduced the project dimensions to this table. This matrix
could provide different ways of attacking the problem space.

<table>
<thead>
<tr class="header">
<th></th>
<th>Emulated zPDT/zD&amp;T</th>
<th><p>Emulated</p>
<p>zPDT/zD&amp;T</p></th>
<th><p>Bare Metal or z/VM</p>
<p>Running z/OS</p></th>
<th><p>Bare Metal or z/VM</p>
<p>Running z/OS</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Donated or Shared</td>
<td>Owned</td>
<td>Donated or Shared</td>
<td>Owned</td>
</tr>
<tr class="even">
<td>Shared sysprog support required to establish the user’s z/OS environment</td>
<td></td>
<td></td>
<td>Tailored to sysprog as users</td>
<td>Tailored to sysprog as users</td>
</tr>
<tr class="odd">
<td>Sysprog activities required inside the user’s z/OS environment</td>
<td></td>
<td></td>
<td>Tailored to end users of z/OS</td>
<td>Tailored to end users of z/OS</td>
</tr>
</tbody>
</table>

There are multiple areas that have a need for a work stream. The chart
above is attempting to determine what areas are of high priority and
will have the most impact for the open source community.

## Not Intended to Cover:

The following topics are not intended to be covered in this working
group:

-   Access to z MIPs or to licensed software. The owners of those
    resources control them and contribute them directly to communities

-   Management of donated resources. This project is intended to enable
    donation, making donation easier, and ensuring ownership control of
    resources is controlled by owners, but does not provide management
    of environments.

## Next Steps

-   Sysprog assessment of tasks under each to be automated

-   Report back to TAC on framework and ask for direction and
    participation for Sysprog assessments

-   Are there sysprog training courses available?

-   Would a Share Session around this be useful?

## News and Discussion

You can connect with the community in a variety of ways...

-   [Public z
    environment](https://wg-public-z-cloud+subscribe@lists.openmainframeproject.org)

-   [Join the conversation on Open Mainframe Project
    Slack](https://slack.openmainframeproject.org/)

-   After requesting access with the above link, look for
    the [\#wg-public-z-cloud
    channel](https://openmainframeproject.slack.com/archives/C01711931GA)

**Contributing**

Anyone can contribute to the z/OS open environment project - learn more
at [<u>CONTRIBUTING.md</u>](https://github.com/genevaers/community/blob/master/CONTRIBUTING.md)

**Governance**

z/OS open environment is a project hosted by the [<u>Open Mainframe
Project</u>](https://openmainframeproject.org/). This project has
established its' own processes for managing day-to-day processes in the
project
at [<u>GOVERNANCE.md</u>](https://github.com/genevaers/community/blob/master/GOVERNANCE.md).

**Reporting Issues**

To report a problem, you can open
an [<u>issue</u>](https://github.com/genevaers/community/issues) in
repository against a specific workflow. If the issue is sensitive in
nature or a security related issue, please do not report in the issue
tracker but instead
email <wg-public-z-cloud+help@lists.openmainframeproject.org>.

## Meetings

See the [Open Mainframe Project public
calendar](https://lists.openmainframeproject.org/calendar). This WG
meets biweekly every other Thursday at 4:00 PM EST.

## Meeting notes

Meeting notes, recordings, and any presentations made during WG meetings
are
available [here](https://github.com/openmainframeproject/wg-public-z-cloud/blob/master/meetings).
