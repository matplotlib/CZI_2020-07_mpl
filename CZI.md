## Progress Report

> Provide a short summary of progress towards the deliverables in your
> currently funded proposal (maximum of 250 words)

We hired Elliott Sales de Andrade as Software
Research Engineed; he started in mid-March. We hit
our target of a net reduction of open PRs by 50/quarter and are making
progress on reducing the number of open issues; However, our initial
estimates of the effort per issue closed were too optimistic. Several
of the issues were mid-sized and high-impact projects
(documentation, js modernization, and semantic axes layout). We had 
2 feature releases and 5 bug-fix releases since January 2020. We drafted new 
governance and contributor onboarding guidelines.

To start dialog with downstream libraries, we presented our new architecture ideas 
to the scientific library development community at the SciPy 2020 maintainers track. 
To identify and work out the categories of `DataSource`s and `Artist`s and develop 
the API between them, we are building prototypes of common visual representations using functional programming ideas. In our prototype, we are generating a list of constraints the library should preserve when transforming data into a visual representation. Because the prototype is developing rapidly, we are postponing working with a downstream partner until the API has stabilized and are delaying the literature review to scope it to the architecture changes. 


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
scientists in bio-medical imaging, microscopy, and genomics. It has
been actively developed and maintained by a vibrant, primarily
volunteer community for the past 17 years. Given the current scale,
scope, and importance of the project, we can not sustainably continue
on only volunteer effort.  It is critical that we continue to support
professional developers to maintain the project and community.
<!--where in the grant workplan is anything about community? -->

With supported developers we have been able reduce our backlog of open
Issues and Pull Requests, a marked change from the previous few years
when both were steadily increasing.  We propose to support a developer
to continue maintenance, mid-sized enhancements, and user support.
This has the direct effect of improving the library for our users and
improving the experience of our contributors and community.

A core strength of Matplotlib is the large and vibrant community of
contributors, down stream library developers, and users around the
library.  We propose committing approximately a third of the developer's
hours to maintaining and fostering this community.
<!--where in the grant workplan is anything about community? how -->
Building on the theoretical and design work we have done in the past
year, we will begin to evolve Matplotlib to incrementally make use of the
new architecture.  Simultaneously we will continue to unify and extend
the user facing API and collaborate with domain specific libraries to
build highly tuned plotting tools.  We propose continuing support for
the graduate student who is leading this effort as her thesis work.

## Work Plan

> A description of the proposed work the applicants are requesting
> funding for, including resources the applicants will provide that
> are not part of the requested funding. For software development
> related work (e.g., engineering, product design, user research),
> specify how the work fits into the existing software project
> roadmap. For community outreach related activities (e.g., sprints,
> training), specify how these activities will be organized, the
> target audience, and expected outcomes (maximum of 750 words)


The continued maintenance of the library is a major component of the
proposed work. Maintenance covers a wide range of tasks including 
triaging bug reports, fixing some of those bugs, reviewing Pull Requests, 
tagging releases, and keeping the continuous integration services
running

These task are essential for the project's health and each
individually are small, but are frequently reactive, time critical, and 
often tedious. They are best handled by a paid developer because it is 
awkward to rely on solely volunteer effort to accomplish tasks that they often 
do not have intrinsic interest in carrying out. 

In addition to the inherent value of completing these tasks, having them 
promptly and reliably addressed improves the contribution experience for 
everyone working on the project.  We propose to devote three quarters of a 
developers time to handling these tasks.

In addition to the reactive work there are substantial but incremental
improvements that will benefit from long blocks of dedicated work.
Examples of this work include fixing long standing rendering and
performance issues, deep-dive documentation, homogenizing and
smoothing the API, and new user-facing functionality. For example, we
have a long-standing prototype for adding a color-blind simulation filter
to the UI.  To turn this prototype into user-ready functionality, we
need to do additional research to make sure we are implementing the
filters accurately in addition to the engineering effort.  We propose
to devote about a quarter of a developer to this effort which should
enable us to complete 5 of these projects.  
<!--confused about 5 'cause you only mentioned this color blind thing that feels random-->
We will work with downstream bio-projects to identify what will have the greatest
impact. <!--why? and then I think most of your grant time ends up spent on downstream libraries 'cause 3 points of contact - me & Elliot & you - sounds like it'll get messy fast--->

As a library Matplotlib needs to support use cases for
the full range <!--not vast range?--> of science domains and complex novel visualizations [1]. 
At the same time the most common visualizations in a domain need to be fluid 
<!--what does fluid mean?--> for the end-practitioners,
with the most commonly used and expected customization options exposed.  To achieve both of
these goals, we need to continue to foster a two layer ecosystem with
a shared core and many domain specific libraries.  Building on the
work done this year to design consistent internal data structures, we
will begin to develop simpler and more expressive user-level APIs, both
in collaboration with domain specific libraries and in core Matplotlib.

Much of the domain-specific specialization is carried in the
structure, semantics and assumptions of the data, and in the standard
visualizations of the domain. These specializations can vary widely,
in contradictory ways, between domains. Because no high-level API can simultaneously satisfy all of the visualization needs, there will always be a need for domain-specific visualization libraries.
In the current grant cycle we have been developing a new architecture that 
is heavily invested in  cleanly separating the three steps in a visualization pipeline: data representation, the encoding of that data in visual variables, and the rendering of those variables to screen. We believe that a better delineation of these steps will more easily allow domain 
practitioners to reuse our functionality and drop in their own as needed. 


We will continue to work with down-stream bio libraries to support them in building tools that  
use the new API. This partnership will also yield important feedback on what users expect out of this
new API. 

The requested support for developers is intended to complement and
facilitate, not replace, crucial volunteer work. We aim to better
coordinate and nurture their efforts, with the goal of growing and
sustaining a diverse community of volunteer and paid expert
contributors.

1 https://rgutzen.github.io/2020-06-25-visualizing_waves/
---

- continue maintenance work
  - review work
  - bug triage
- improve new contributor onboarding
- Finish architecture development & start to implement in core library
- start to re-design user API in a way that can make the most of the
  improved internal structure
- mid-sized new features
  - color blind filter
  - rendering accuracy improvements
  - performance

- work with down-stream libraries to use new API

## Milestones and Deliverables

> List expected milestones and deliverables, and their expected
> timeline. Be specific and include (where possible) any goals for
> metrics the software project(s) are expected to reach upon
> completion of the grant (maximum of 500 words)

Quantitatively evaluating maintenance work can be tricky---some Issues
or PRs take minutes to review while others can take days to weeks of
effort---but we believe that there is value at looking at the total
number of open Issues and PRs. 
<!--we wrote this in our progress report--> 
We will reduce this number by closing Issues and PRs faster than they are opened until a reasonable
equilibrium is reached.  We will aim to hit the following metrics:

- Initial response to all issues / new PRs within a week
- Resolve majority of new issues / PRs within 1 month
- ​​Reduce backlog of issues by 50 / quarter
- ​​Reduce backlog of PRs by 50 / quarter

During the current grant period, we are developing a road map
addressing how we will homogenize the API, implement "smart" composite
Artists, and overhaul the data model.  In the second year we will
begin to execute on that road map.  While we are still developing the
road map, we expect it to include implementations of the new
architecture, in both Matplotlib and domain specific libraries, ready
for early users.
<!-- this is not a coherent sentence--->

Additionally, we anticipate that we will be able complete 5 projects
of the scope of adding a color-blind preview within the scope of this
grant.  We will identify the projects to be done based on our road map.
<!-- you didn't really explain what that scope is -->

The focus of the design work in the current grant is on the internal API
and data structures, in the second year we will begin to develop new
general-use user facing APIs. <!--on top of implementing the old API under the hood?-->

- design documentation about new user-facing API
<!-- so the original plan had been to shim the API under the old user facing API - 
  is there a pressing need for new user-facing API? While yes this is my happy place,
  while yes this is my happy place, I think shimming is how we sort out the actual user needs-->
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
contributors.  In addition to being directly used by scientists, there
are many libraries and applications that use Matplotlib to provide 
domain-specific plotting, including CZI funded projects such as scikit-learn, 
CellProfiler, scanpy, starfish, nipy, and scikit-image. To aid 
users in discovering these extensions we have recently been assigned 
a Trove classifier on pypi [1], which we applied for due to a conversation 
at the first CZI EOSS summit. 

Given the centrality of visualization to data analysis across all
domains, no single tool is going to be suited to fit all needs.  There
are a range of tools not built on Matplotlib (see https://pyviz.org/tools.html 
for a long but not exhaustive list) that target use cases
that Matplotlib is not well suited for.  A goal of our work is to
increase the degree to which thsee tools can interoperate, letting users
switch tools as needed to use the right tool (or mix of tools) for the job.

[1] https://pypi.org/search/?q=&o=&c=Framework+%3A%3A+Matplotlib


## Diversity, Equity, and Inclusion (DEI) Statement

> Advancing DEI is a core value for CZI, and we are requesting
> information on your efforts in this area. Describe any efforts the
> software project(s) named in this proposal have undertaken to
> increase diversity, equity, and inclusion with respect to their
> contributors and audience. Please see examples from successful second
> cycle applications ​(maximum of 250 words)

The Matplotlib project is committed to being an open and welcoming
project. Because our contributors have a diverse range of identities 
and experiences, we believe as a project that transparency and explicitness 
of process and in communication are key to building
an inclusive, equitable, and diverse project. In our effort to be
welcoming, we have worked at being more explicit about how the
project operates and our norms and values.  To this end, we have put
major effort into documenting our governance, defining leadership
roles, and clarifying specific expectations for new code and community
contributors.  It is critical that all contributors, independent of
experience level both in general and with the project, feel safe to
make mistakes and learn in our community.  We embody these values in
our interactions on github, our mailing list and community discussion forum
(discourse), and in our social media.  We hope that these practices will 
empower and encourage people of diverse identities to participate in Matplotlib.
