## Progress Report

> Provide a short summary of progress towards the deliverables in your
> currently funded proposal (maximum of 250 words)

We identified and hired Elliott Sales de Andrade as an Software
Research Engineer who started in mid-March.  Since then we have hit
our target of a net reduction of open PRs by 50/quarter and are making
progress on reducing the number of open issues.  However, our initial
estimates of the effort per issue closed was too optimistic.  Several
of the issues closed were mid-sized and high-impact projects
(documentation, js modernization, and semantic Axes layout).  In
addition to the above work we have done 2 feature release and 5
bug-fix releases since January 2020.

We maintain a discourse forum to facilitate conversations with users and
drafted new code and community contributor onboarding guidelines.

<few sentences about the data / visual element / artist separation>.

* reached:

- Start dialog with downstream libraries We presented our new
  architecture model to the scientific library development community
  at the SciPy 2020 maintainers track.
- Start to identify the categories of `DataSource`s and `Artist`s and
  their relationships We are refactoring the library component roles
  and responsibility using functional programming ideas and have begun
  a list of constraints the library should preserve in
  transforming data visual representation.
- Work out API between `Artist` and `DataSource`
  * We are building prototypes of common visual representations to
    test if the new architecture is expressive enough to support current
    Matplotlib visualizations.

* moved:

- Review of architecture of other plotting packages, ready for
  submission to journal In working out the architecture, we scoped the
  literature review of architecture based on the proposed architecture
  change.

* missed:

- collect user stories of plotting needs We have been collecting user
  stories informally but need to do

## Proposal Purpose

> One sentence (maximum of 255 characters including spaces)

> 245 characters

To enable Matplotlib to continue as the core plotting library of the
Scientific Python Ecosystem, we will address the maintenance backlog
and begin Matplotlib's evolution to meet the community’s visualization
challenges for the next decade.


## Abstract/Proposal Summary
> A short summary of the application ​(maximum of 250 words)

> - keep up level of effort on maintenance
> - start to implement design work planned this year
> - engage with down-stream packages

> 252 words

Matplotlib is the foundational data visualization library for the
Scientific Python Ecosystem, used by over a million users, including
scientists in bio-medical imaging, microscopy, and genomics.  It has
been actively developed and maintained by a vibrant, primarily
volunteer community for the past 17 years.  Given the current scale,
scope, and importance of the project, we can not sustainably continue
on only volunteer effort.  It is critical that we continues to support
professional developers to maintain the project and community.

With supported developers we have been able reduce our backlog of open
Issues and Pull Requests, a marked change from the previous few years
when both were steadily increasing.  We propose to support a developer
to continue maintenance, mid-sized enhancements, and user support.
This has the direct effect of improving the library for our users and
improve the experience of our contributors and community.

A core strength of Matplotlib is the large and vibrant community of
contributors, down stream library developers, and users around the
library.  We propose committing approximately a third of the developer to
maintaining and fostering this community.

Building on the theoretical and design work we have done in the past
year we will begin evolve Matplotlib to incrementally make use of the
new architecture.  Simultaneously we will continue to unify and extend
the user facing API and collaborate with domain specific libraries to
build highly tuned plotting tools.  We propose continuing support for
the graduate student who is leading the this effort as her thesis work.

## Work Plan

> A description of the proposed work the applicants are requesting
> funding for, including resources the applicants will provide that
> are not part of the requested funding. For software development
> related work (e.g., engineering, product design, user research),
> specify how the work fits into the existing software project
> roadmap. For community outreach related activities (e.g., sprints,
> training), specify how these activities will be organized, the
> target audience, and expected outcomes (maximum of 750 words)

A major component of the proposed work is devoted to the continued
maintenance of the library.  This is a very broad scope of work that
includes every thing from fixing critical bugs, reviewing Pull
Requests, triaging and addressing bug reports, tagging release, and
keeping the continuous integration services running.  While critical
to keeping the project healthy and individually small, it is difficult
to accomplish them in a timely manner with only volunteer effort as
they are frequently reactive, you can not plan for a critical bug to
be found or a dependency to change, time critical, and not always fun.
By making sure these tasks are done we will improve the experience for
both new and existing contributors and improve the onboarding of new
contributors to the project.  We propose to devote three quarters of a
developers time to handling these tasks.

In addition to the reactive work there are incremental improvements
that require larger blocks of time.  These projects range from fixing
long standing rendering artifacts, to deep-dive documentation into the
why of the API choices, to performance improvements, to new user
facing features.  For example, we have a proposal to add filters to
the UI to preview what plots will look like under different types and
degrees of color-blindness.  To implement this we would need to
research how to properly implement the filters and consult with
color-perception experts in addition to the programming and design
work to add the feature.  Having a developer able to devote large
blocks of time to Matplotlib will enable work of this scale.  We will
aim to complete 5 of these projects and will work with downstream
bio-projects to identify what will have the greatest impact.

The most common visualizations in a domain need to be fluid for the
end-practitioners, with the "obvious" customization options exposed.
Much of the domain-specific specialization is carried in the
structure, semantics and assumptions of the data, and in the standard
visualizations of the domain.  These specializations can vary widely,
in contradictory ways, between domains.  Because no high-level API can
simultaneously satisfy all of the visualization needs, there will
always be a need for domain-specific visualization libraries.
Building on the work done this year to design consistent internal data
structures we will begin to develop simpler and more expressive
top-level APIs.  We will continue to work with down-stream bio
libraries to support them in implementing data sources, artists, and
user API.

The requested support for developers is intended to complement and
facilitate, not replace, crucial volunteer work. We aim to better
co-ordinate and nurture their efforts, with the goal of growing and
sustaining a diverse community of volunteer and paid expert
contributors.


---

- continue maintenance work
  - review work
  - bug triage
- improve new contributor on-boarding
- Finish architecture development & start to implement in core library
- start to re-design user API in a way that can make the most of the
  improved internal structure
- mid-sized new features
  - color blind filter
  - rendering accuracy improvements
  - performance

- work with down-stream libraries to use data sources

## Milestones and Deliverables

> List expected milestones and deliverables, and their expected
> timeline. Be specific and include (where possible) any goals for
> metrics the software project(s) are expected to reach upon
> completion of the grant (maximum of 500 words)

Quantitatively evaluating maintenance work can be tricky---some Issues
or PRs take minutes to review while others can take days to weeks of
effort---but we believe that there is value at looking at the total
number of open Issues and PRs.  We will reduce this number by closing
Issues and PRs faster than they are opened until a reasonable
equilibrium is reached.  We will aim to hit the following metrics:

- Initial response to all issues / new PRs within a week
- Resolve majority of new issues / PRs within 1 month
- ​​Reduce backlog of issues by 50 / quarter
- ​​Reduce backlog of PRs by 50 / quarter

During the current grant period we are developing a road map
addressing how we will homogenize the API, implement "smart" composite
Artists, and overhaul the data model.  In the second year we will
begin to execute on that road map.  While we are still developing the
road map, we expect it to include implementations the new
architecture, in both Matplotlib and domain specific libraries, ready
for early users.

Additionally, we anticipate that we will be able complete 5 projects
of the scope of adding a color-blind preview within the scope of this
grant.  We will identify the projects to be done based on our road map.

The focus of the design work in current grant is on the internal API
and data structures, in the second year we will begin to develop new
general-use user facing APIs.

- design documentation about new user-facing API
- ??


## Landscape Analysis

> Briefly describe the other software tools (either proprietary or open
> source) that the audience for this proposal is primarily using. How
> do the software projects in this proposal compare to these other
> tools in terms of size of user base, usage, and maturity? ​How do
> existing tools and the project(s) in this proposal interact? (maximum
> of 250 words)

> 191 words


Matplotlib is the mostly widely used and de-facto standard
visualization library in Python (over 1M monthly users) and is a
mature library (17+ years old) with over 1,000 individual code
contributors.  In addition to being directly used by scientist, there
are many libraries and applications that use Matplotlib, including
scikit-learn, CellProfiler, scanpy, starfish, nipy, and sickit-image
(all of been funded by CZI), to provide domain-spcefiic plotting.  To
aid users in discovering these extensions we have recently been
assigned a Trove classifier on pypi [1].

Given the centrality of visualization to data analysis across all
domains no single tool is going to be suited to fit all needs.  There
are a range of tools, see https://pyviz.org/tools.html for a long but
not exhaustive list, not built on Matplotlib that target use cases
that Matplotlib is not well suited for.  A goal of our work is to
increase the degree to which the tools can interoperate letting users
switch tools as needed to use the right tool for the job.

[1] https://pypi.org/search/?q=&o=&c=Framework+%3A%3A+Matplotlib


## Diversity, Equity, and Inclusion (DEI) Statement

> Advancing DEI is a core value for CZI, and we are requesting
> information on your efforts in this area. Describe any efforts the
> software project(s) named in this proposal have undertaken to
> increase diversity, equity, and inclusion with respect to their
> contributors and audience. Please see examples from successful second
> cycle applications ​(maximum of 250 words)

The Matplotlib project is committed to being an open and welcoming
project. Because our contributors come from a wide range of
backgrounds and experiences, we believe as a project that transparency
and explicitness of process and in communication are key to building
an inclusive, equitable, and diverse project.  In our effort to be
welcoming, we have also worked at being more explicit about how the
project operates and our norms and values.  To this end, we have put
major effort into documenting our governance, defining leadership
roles, and specific expectations for new code and community
contributors.  It is critical that all contributors, independent of
experience level both in general and with the project, feel safe to
make mistakes and learn in our community.  We embody these values in
our interactions on github, our community discussion forum
(discourse), mailing lists, and in our social media.  We hope that
these practices will empower and encourage people of diverse
identities to participate in Matplotlib.
