# Teacher Workflow and Access Context

## Background

The project is being shaped from the perspective of a classroom teacher who primarily teaches 10th- and 11th-grade college-preparatory courses, with substantial prior experience and existing material for 9th grade as well.

Google Classroom has recently made standards-based planning more useful by supporting features such as:

- Tagging assignments with standards
- Connecting standards to rubric elements
- Tracking which standards have been attached to assignments over time

These features improve assignment-level alignment, but they do not provide durable repository-level memory. They cannot reliably answer broader planning questions such as:

- Which standards have been covered so far?
- Which standards have been emphasized repeatedly?
- Which standards remain underrepresented or untouched?
- How does coverage differ across courses, grade levels, units, or time periods?

That gap is one of the main reasons this project needs a repository-backed component.

## Core planning problem

The teacher already has many assignments, especially for 10th and 11th grade. Processing them one at a time is too slow and repetitive.

Even with strong instructions for tasks such as:

- Identifying applicable standards
- Accounting for Google Classroom constraints
- Designing rubrics that can be imported into Google Classroom
- Matching standards to rubric criteria

there is still repeated setup and processing latency for every individual assignment. A workflow that requires separate prompts and separate model runs for standards analysis, rubric generation, and formatting does not scale well across an existing body of course material.

The project therefore needs some form of batch-processing capability.

## Intended user-facing capability

The likely direction is an interface that allows the teacher to submit or select multiple assignment files and process them together.

The interface should support work such as:

- Analyzing existing assignments in batches
- Identifying relevant standards
- Producing Google Classroom-compatible rubric structures
- Connecting rubric elements to standards
- Preserving the resulting alignment data in a repository-level memory
- Making it possible to review coverage across assignments and over time

The exact interaction model is still open. The important point is that the workflow should reduce repetitive model startup, repeated prompting, and one-assignment-at-a-time processing.

## Data and privacy context

The anticipated source material is the teacher's own instructional content and process documentation.

At this stage, the system is not intended to process student information. That means the planning materials, assignment-analysis workflow, and generated standards/rubric artifacts may not require private hosting solely for student-data protection.

This may make a publicly accessible web interface acceptable, provided no student-identifying information is introduced later.

## Access requirement

The teacher needs to be able to use the system from a professional account and work environment. This is a major reason to consider a browser-based interface rather than a workflow tied only to a personal machine or account.

A website could provide a stable access point across contexts and reduce dependence on direct access to a local development environment.

## Hosting possibilities under consideration

Two broad deployment directions are currently visible:

### Hosted web application

A site deployed through a service such as Render could provide:

- Browser-based access from a professional account
- A consistent interface for file submission and batch processing
- Public or restricted access, depending on later requirements
- Separation between the teacher's daily workflow and the development machine

### Mac Mini-backed workflow

A Mac Mini already connected to coding agents such as Codex and Claude could potentially serve as:

- A local processing host
- A development and automation environment
- A private alternative to cloud deployment
- A backend supporting a lightweight interface

This may reduce hosting complexity or cost, but it could create access, reliability, networking, and maintenance tradeoffs.

## Current intent

The repository should eventually support both durable planning memory and practical batch processing.

The current objective is not to decide the implementation method. It is to preserve enough context that a later onboarding model can understand:

- The teacher's actual planning problem
- Why Google Classroom alone is insufficient
- Why repository-level memory matters
- Why batch processing is central rather than optional
- Why browser-based professional access is desirable
- Why both hosted and locally backed deployment remain plausible

## Open questions

- What file types will be submitted for batch processing?
- Should the primary unit of organization be course, grade level, unit, assignment, or school year?
- What standards framework or frameworks will be used?
- How should standards coverage be summarized over time?
- What exact output format is needed for Google Classroom rubric import?
- Should users review and approve generated standards before they are stored?
- Does the interface need authentication even if the source material contains no student data?
- Should the repository itself be the system of record, or should it back a separate database?
- Is the Mac Mini best viewed as a development environment, a production host, or only an optional processing node?
- Would a Render-hosted frontend and a Mac Mini-backed processor be useful, or unnecessarily complex?
