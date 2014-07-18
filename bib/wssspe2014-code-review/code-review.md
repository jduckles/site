# Code Review For and By Scientists: Preliminary Findings

Marian Petre
Open University
m.petre@open.ac.uk

Greg Wilson
Software Carpentry
gvwilson@software-carpentry.org

## Abstract

FIXME: abstract.

## Introduction

Since Fagan's work in the 1970s \cite{b:fagan1976,b:fagan1986},
dozens of studies have shown that code review is the most effective and time-effective way
to find bugs in software \cite{b:cohen2010,b:bacchelli2013}.
Despite this,
code review was still talked about more than done until the early 2000s.
What changed was the rise of distributed collaboration,
partiuclarly in open source projects whose participants rarely met face-to-face.

Ironically,
given that Fagan and others were inspired by academic peer review,
code review is still rare in scientific software development.
This is partly a case of the blind leading the blind
(faculty don't do code reviews, so they don't pass the skill on to their students),
partly because most authors don't publish their code,
and hence have little incentive to improve its quality,
and partly because most scientists do not understand code review's benefits or how to actually do it.

In 2013--14,
we ran two pilot studies to explore
the benefits of code review for typical scientist-coders,
and how to transfer the skill to them.
We use the word ``typical'' deliberately:
our focus was not the small minority of scientists who already use good software engineering practices \cite{b:hannay2009},
but the large majority who have never encountered them.

## Post-Hoc Reviews

Our first study,
done in conjunction with PLOS,
ran from August to October 2013.
In it,
professional developers working at Mozilla reviewed
samples of code taken from papers published in *PLOS Computational Biology* in the preceding 18 months.
Those reviews were then shared with the scientists,
and both groups were interviewed to explore:

* whether non-scientists could usefully review typical scientific software,
* whether those reviews were intelligible and useful to the scientists, and
* whether the participants felt the reviews were valuable.

We conducted semi-structured interviews \cite{b:rosenthal2007,b:bryman2008}
with 11 developers in late August and early September,
and with 4 authors whose code had been reviewed in late September and early October.
In them,
we asked authors if code review would be of value in their future practice,
and asked reviewers:

* to compare the review of the scientific code with their previous professional experience of code reviews,
* about their ability to engage with the scientific context, and
* if they felt they could offer useful commentary.

### Findings

#### 1: Scientists' starting points varied widely.

Scientists' prior knowledge and practices varied widely.
Some used engineering practices and tools like version control some of the time,
but documentation of the form developers expected was rare,
and practices like continuous integration were unknown or considered "very unusual".

In particular,
most scientists had never taken part in code review.
Some of the code authors we interviewed work in (or lead) teams in which they read each other's code,
but most participants had never,
or only rarely,
discussed their code with others.
Instead, they discussed the results the code produced.

#### 2: Developers felt limited.

Most developers also felt that they were in unfamiliar territory.
The lack of documentation, commenting, tests, and example data sets was noted repeatedly;
a typical comment was,
"Not having the project build is a big problem; I can't verify that the code is correct."
Equally,
most reviewers were frustrated at not being able to run the code as the first step in review,
making comments like,
"That's the easiest way to see if it works at all," and "It's a way to validate the intentions of the author."
Several commented that as a result, they had to make some assumptions in the review.

Few reviewers read in detail the paper with which the code was associated,
usually because they lacked the domain expertise to do so.
They could deduce what the code did and assess it in terms of its ability to perform that operation efficiently,
but could not tell if the code fulfilled its intended scientific role.
That,
combined with their isolation from the scientists,
left developers feeling that they were doing "drive-by" reviews.

#### 3: Standards and expectations were very different.

Many reviewers were struck by how scientists' code differed from theirs,
and remarked on the lack of commenting and explanation in the code.
Several suggested that the scientists appear to have "less concern for maintainability and readability"
and that the code was "not written for others to use".
Some also pointed out naive lack of complexity or abstraction,
redundancy in the code,
inconsistencies or ignorance of standards in formatting,
and unhelpful naming.

On their side,
the scientists all aspired to create readable and re-usable code,
but many noted that their code doesn't respect the common etiquette of open source:
for example,
they often don't make an effort to package their code for re-use by others.
One scientist commented that:
"[It's] not important to have something that's exact---only when we publish"
and reiterated the low status of code in their science:
"In the business of science, all that matters is the figures.
The quality of the code is just not on the critical path."

#### 4: Both sides wanted more contact.

All but one of the reviewers remarked that they miss the social context they normally associate with code reviews:
working relationships, understanding goals and priorities, and trust.
They would have preferred some form of dialog,
not least to provide them with the code context,
and to establish appropriate expectations for both reviewers and authors
(e.g., "knowing what kind of feedback the author wants").
A typical remark was, "It would have been easier if we were allowed to contact the scientist just to get a feel for his mindset."
Most referred to dialogs that are normally part of their code review experience,
whether spoken or on-line:
"Discussion catches details that get lost otherwise" such as "tiny changes in numerical interpretation that are important".
The reviewers also pointed out that the dialog has value for the reviewer, as well as for the author:
"When there is a dialog, you end up learning a lot yourself."

FIXME: more about scientists wanting more contact (and quotes) to justify the organization of the second study.

FIXME: more about wanting reviews during development, rather than at the end when it's too late.

## Transferring the Skill

Despite their frustrations,
all of the participants in the first study interviewed were positive about the pilot.
We therefore we set up a second study that paired experienced scientific programmers
with small groups of less-experienced ones to explore ways of transferring the practice itself.

Ten groups ranging in size from a couple of people to half a dozen initially signed up to take part in this study.
In interviews and early discussions, they identified four main reasons why they think they ought to do code review:

1. Rigor.
Scientists (understandably) want to get the right answer.
They also want to be able to reproduce it later,
but recognize that correctness and reproducibility aren't the same thing.

2. Reusability.
Most scientists are acutely aware of how their understanding of their own code dissipates over time
and of how much this costs them.
Equally,
they suspect that they spend a lot of time reinventing wheels.
They may not know how code review will help with that,
but they hope that it will.

3. Collaboration.
Many scientists hoped that they could use code review as an excuse for conversations about code with their colleagues---conversations
that simply don't happen right now.
Some believe that coding collaboratively would foster better testing,
encourage scientists to produce code that is easier to understand and share,
and make team members more aware of each other's research.

4. Opening doors.
Many participants said they wanted to use the study to learn about more than just code review.
They all felt that there must be a better way to build programs than what they're doing right now;
taking part in this study was,
for them,
a way to get mentoring from someone who could answer questions they didn't know to ask.

One thing that we *didn't* hear was people saying that they wanted to learn about the science embodied in the code being reviewed.
Rightly or wrongly, scientists seem to feel that "what it does" can be learned in others ways.

FIXME: describe study methodology

### Findings

Our biggest finding is how much perspective matters to collaboration.
Over time,
professional software developers (including scientists whose primary role has shifted to software development)
build up an overview of how software works and how to make working software.
They integrate skills and knowledge,
building up a standard vocabulary of terms, tools and conventions,
as well as a practical repertoire that it's easy to take for granted.

Most scientists don't (yet) have such an overview:
they are just getting a job done,
focused almost entirely on the purpose the code serves rather than the code itself.
They often lack the integrated understanding and skill that comes with experience,
which meant it was often very useful for mentors to actually state the obvious.

How to make the transition from the first perspective to the second is usually not clear to working scientists.
"Stuff that seemed like overkill makes sense now...
A lightbulb finally went off:
I understand how other people look at my code and how to make it work."
And what basics to articulate---where to look and how to look---is often not clear to experienced developers.
If the two are going to collaborate,
then at some point the different perspectives must be acknowledged and bridged.
Social mechanisms like courtesy, deference, and avoiding embarrassment tend to obscure this,
so it's crucial to articulate collaborators' perspectives explicitly for both sides,
and equally to help establish appropriate expectations explicitly.

This observation isn't new:
as Segal discussed in her study of industrial software engineers collaborating with scientists \cite{b:segal2005}:

  [Programmers] demand an up-front articulation of requirements,
  whereas the scientists had experience, and hence expectations, of emergent requirements.
  The project documentation does not suffice to construct a shared understanding.

For every mentor who says,
"I wish I knew more clearly what the scientists are expecting,"
there's a scientist who says, "I wish I knew what it's reasonable to expect."
One concrete step we could take is to show scientists what it actually looks like to do a code review:
not just the end result,
but the process itself.

different models of code review, and how they map onto different goals of code review

## Conclusions

FIXME: write conclusion.

should we have started with pair programming? is that feasible?

60-second checklist for others:  do you want to do this?

* your stuff is available (in a repository)
* you have a goal, a benefit in mind
* you commit a little time on a regular basis
* you understand that it's the code that's being reviewed (not you)

benefits experienced: why the mentors believe in code review

how to get started:  articulate goals/expectations, build rapport
(cf. Greg's question:  should have started with pair programming:  innate reciprocity?)

 seeing it done; doing it (or, why you need more than one scientist taking part)

returns from small investments: e.g., Why does Software Carpentry work?  One thing at a time and it will accumulate.

Bill's advice:  every time you touch a method, check the docstring and write a test; the work will accumulate