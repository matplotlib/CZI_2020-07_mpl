## Progress Report

> Provide a short summary of progress towards the deliverables in your
> currently funded proposal (maximum of 250 words)

The current grant is supporting one developer at 40% (Thomas Caswell), one graduate
student (Hannah Aizenman) with partial summer support for her advisor (Michael Grossberg), and a full time
Research Software Engineer.  For the latter we ran a search and hired
Elliott Sales de Andrade who started in mid-March.

Elliott has focused on the maintenance and support aspect of the
grant.  We hit our target of a net reduction of open PRs by 50/quarter
and are making progress on reducing the number of open issues.  Our
initial estimates of the effort per issue closed were too optimistic;
however, we merged several mid-sized and high-impact projects
(documentation, JavaScript modernization, and a complex axes layout helper).
Additionally we drafted new governance and contributor onboarding
guidelines and had 2 feature and 4 bug-fix releases.


We presented our new architecture ideas to the scientific library development community at the SciPy 2020 maintainers track.  We designed the prototype API to have a clean separation between the `DataSource`, `Artist`, and rendering layers. We started implementing sample DataSources and Artists to formalize and validate the interface between them. Because the prototype is still developing rapidly, we are postponing working with a downstream partner until the API has stabilized.

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

> 247 words

Matplotlib is the foundational data visualization library for the
Scientific Python Ecosystem, with over a million users, including
researchers in bio-medical imaging, microscopy, and genomics. It has
been actively developed and maintained by a vibrant, primarily
volunteer, community for the past 17 years.
In the past 6 months, with supported developers, we reduced our backlog of open
Issues and Pull Requests. This is a marked change from the previous few years,
when both were steadily increasing with only volunteer effort. We propose to support an FTE of effort
to continue maintenance, mid-sized enhancements, and user support.
This has the direct effect of improving the library for our users and
improving the experience of our contributors and community. We also propose
committing approximately a quarter of FTE to community maintenance, inculding goverance.

Building on the theoretical and design work we have done in the past
year, we will begin to evolve Matplotlib to take advantage of the
new architecture.  We will continue to collaborate with domain specific libraries to
build tuned plotting tools.  We propose continuing support for
the graduate student who is leading this effort as her thesis work, along with partial summer support of her advisor, and the remainder of the developer effort.

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
triaging bug reports, fixing bugs, reviewing Pull Requests,
tagging releases, and keeping the continuous integration services
running. These tasks are essential for the project's health; though each
individually is small, they are frequently time critical and
tedious. They are best handled by a paid developer because
it is unfair and impractical to rely solely on volunteers to accomplish such tasks.
In addition, having these tasks promptly and reliably addressed
improves the contribution experience for everyone working on the project.
We propose to devote three quarters of a developer's time to handling these tasks.

In addition to routine maintenance tasks, there are substantial but incremental
improvements that require long blocks of dedicated work.
Examples of this work include fixing long-standing rendering and
performance issues, deep-dive documentation, homogenizing and
smoothing the API, and new user-facing functionality.
For example in the current grant cycle we implemented a new flexible, easier to use, axes layout API that
allows users to arrange named Axes in a complex Figure.
A candidate of similar scope is adding a color-blind simulation filter to the UI to facilitate accessible visualization.
Funding would allow us to tackle about 5 such medium-sized,
self-contained projects with about a quarter of an FTE.  Without
funding, this type of project can drag out for months or stall
altogether. We will identify high-impact improvements in collaboration
with down-stream bio-libraries.

We propose dedicating a quarter of FTE (distributed across funded personnel)
to community maintenance, including governance, outreach, communications,
and moderation. They will also facilitate discussions around proposed enhancements,
features, and API changes. The requested support is intended to complement,
not replace, crucial volunteer work.

Matplotlib needs to support use cases across a vast range
of science domains, enabling complex visualizations [1].  At
the same time, common visualizations in a domain need to be
fluid for the end-practitioners, tuned to the domain's standard data structures,
and with domain-specific customization options exposed.  To achieve both of these
goals, we need to continue to foster a two-layer ecosystem with a
shared core (Matplotlib) and many domain-specific libraries (seaborn, nipy, ...).

In the current grant cycle we have been developing a new architecture that is
heavily invested in cleanly separating the three steps in a
visualization pipeline: data representation, encoding the data
as visual elements, and rendering those elements to
screen. We believe that a better delineation of these steps will allow
domain practitioners to more easily implement extensions.
Following on the work
done this year to design consistent data and artist abstractions, we will
develop simpler and more expressive user-level APIs in core Matplotlib and in
collaboration with domain-specific libraries.  This effort is led by
the graduate student as part of her thesis work.

[1] https://rgutzen.github.io/2020-06-25-visualizing_waves/


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
- Reduce backlog of issues by 50 / quarter
- Reduce backlog of PRs by 50 / quarter
- 5 mid-sized new features

The focus of the design work in the current grant is on the core API
and data structures. In the second year we will develop and deploy a
provisional implementation in Matplotlib and document how developers
can build tools that use this interface. Specific goals are to provide:

- provisional implementation using new architecture in Matplotlib
- developer-aimed documentation (API + narrative)
- proof of concept 3rd party user-facing library with a biology partner
- academic paper about building visualization tools on top of the core architecture

## Landscape Analysis

> Briefly describe the other software tools (either proprietary or open
> source) that the audience for this proposal is primarily using. How
> do the software projects in this proposal compare to these other
> tools in terms of size of user base, usage, and maturity? ​How do
> existing tools and the project(s) in this proposal interact? (maximum
> of 250 words)

> 181 words


Matplotlib is the most widely used and de-facto standard
visualization library in Python (over 1M monthly users) and is a
mature library (17+ years old) with over 1,000 individual code
contributors.  In addition to being directly used by scientists, it is
central to many libraries and applications that implement domain-specific
visualizations, including CZI funded projects such as scikit-learn,
CellProfiler, scanpy, starfish, nipy, and scikit-image. To aid
users in discovering these extensions we have recently been assigned
a Trove classifier on PyPI [1] (which we applied for due to a conversation
at the first CZI EOSS summit).

Given the centrality of visualization to data analysis across all
domains, no single tool can satisfy all needs.  There
are a range of tools not built on Matplotlib (see https://pyviz.org/tools.html
for a long but not exhaustive list) that target use cases
that Matplotlib is not well suited for.  A side effect of our work will be to
increase the interoperability of these tools, letting users
use the right tool (or mix of tools) for the job.

[1] https://pypi.org/search/?q=&o=&c=Framework+%3A%3A+Matplotlib

## existing support

- CZI cycle 1 grant (250k, Jan 2020-Jan 2021, EOSS-0000000100)
- NF small development grant (5k$ to support documentation, completed)
- NF small development grant (3k$ to support a hosted mac mini, 3yr)
- GSOC 2020 (1 student, summer 2020)


## Diversity, Equity, and Inclusion (DEI) Statement

> https://apply.chanzuckerberg.com/protected/resource/eyJoZnJlIjogOTQ1ODEyNDksICJ2cSI6IDEzOTQ5OH0/

> Advancing DEI is a core value for CZI, and we are requesting
> information on your efforts in this area. Describe any efforts the
> software project(s) named in this proposal have undertaken to
> increase diversity, equity, and inclusion with respect to their
> contributors and audience. Please see examples from successful second
> cycle applications ​(maximum of 250 words)

Matplotlib is committed to being an open and welcoming
project. We believe that transparency and explicitness
of process and in communication are key to building
an inclusive, equitable, and diverse project. In our effort to be
welcoming, we have worked at being more explicit about our norms and values
and how the project operates. To this end, we have put
major effort into documenting our governance, defining leadership
roles, and clarifying specific expectations for new code and community
contributors. It is critical that all contributors, independent of
experience level both in general and with the project, feel safe to
make mistakes and learn in our community. We strive to embody these values
in our interactions on github, our mailing list and community discussion forum
(discourse), and in our social media. We hope that these practices will
empower and encourage people who have diverse identities to participate in Matplotlib.
