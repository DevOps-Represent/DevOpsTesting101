- [Contributing](#contributing)
  * [Pull Request Process](#pull-request-process)
  * [Module Guidelines](#module-guidelines)
    + [Good questions to ask](#good-questions-to-ask)
      - [1.) Who is it for?](#1--who-is-it-for-)
      - [2.) What are my learning outcomes?](#2--what-are-my-learning-outcomes-)
      - [3.) What does feedback look like?](#3--what-does-feedback-look-like-)
    + [Module Format](#module-format)
      - [1.) Talk and Theory (15-30 minutes)](#1--talk-and-theory--15-30-minutes-)
      - [2.) Self-driven practical (60-90 minutes)](#2--self-driven-practical--60-90-minutes-)
      - [3.) Knowledge check](#3--knowledge-check)
    + [Overall structure](#overall-structure)
      - [Option A.) The "Kata"](#option-a--the--kata-)
      - [Option B.) The "Castle"](#option-b--the--castle-)
- [Code of Conduct](CoC.md)


# Contributing

When contributing to this repository, please first discuss the change you wish to make via issue,
email, or any other method with the owners of this repository before making a change.

Please note we have a code of conduct, please follow it in all your interactions with the project.

## Pull Request Process

1. Update the CHANGES.md with details of changes to the modules - this includes corrections,
   syllabus updates for new features, or practical information.
2. You may merge the Pull Request in once you have the sign-off of another developer, or if you
   do not have permission to do that, you may request the reviewer to merge it for you.

## Module Guidelines

### Good questions to ask

Before making a DevOps Girls module, consider asking the following questions:

![Lean Canvas](/images/CONTRIBUTING/module-lean-canvas.png)

#### 1.) Who is it for?

It's important to identify who your target audience is, and what their knowledge baselines would be.
Put into practical terms: are you planning to cater for absolute beginners? Or do you aim to teach
people with existing backgrounds in tech?

Even then, it's important to identify the level of experience you're working with. This is critical as
you define the level of depth you want to dive in - e.g., do you assume that the attendees have experience
with the command line, or do you also need to cover CLI basics?

#### 2.) What are my learning outcomes?

It is also good to be able to articulate what you want the attendees to be able to do: the workshop aims to
empower people, and it's useful to declare where you'd want them to be by the end of the day.

To put it into questions: do you want the attendees to be able to *remember* what you covered, or do you
want them to be able to *create a solution*? Would they be able to *evaluate* between different solutions?

Consider using [Bloom's Taxonomy of Learning](https://en.wikipedia.org/wiki/Bloom%27s_taxonomy)
as a guide.

![Bloom's Taxonomy](/images/CONTRIBUTING/blooms-taxonomy.png)

#### 3.) What does feedback look like?

**Knowledge checks** are a powerful tool - they let you verify if the attendees understand your content,
while at the same time encouraging knowledge retention. This is why teachers usually structure lessons
so that there are quizzes at the end of it.

Feedback can take many shapes: a quiz, a poll, or a question at the end of your practicals. Maybe make it
fun even - have some small prizes for attendees who ask good questions.

### Module Format

#### 1.) Talk and Theory (15-30 minutes)

It's good to have a fun, informative talk before diving into the practicals. Consider covering the following areas:

 - The history and context of the particular technology
 - How it works
 - How and when to use it
 - How it's valuable to the business

Keep it short, but remember to pace down. It's better to take your time than rush too fast and risk leaving people
behind - remember: not everyone is willing to ask you to repeat concepts and facts.


#### 2.) Self-driven practical (60-90 minutes)

Consider running a practical exercise that the attendees can follow. A few things to keep in mind:

 - Make sure that everyone knows beforehand what they need to go through it. Do they need `awscli` installed? Do they need their own AWS account?
 - Make sure that the environments the attendees are deploying/building to are enclosed and free of dependencies.
 - Make sure that coaches have gone through the material beforehand.

If you're feeling up for it, *moonshots* are also a good idea - optional exercises for those who blitz through the material.

#### 3.) Knowledge check

Consider saving a portion of time for reflection and self-evaluation. Ask the attendees questions (whether in text or face-to-face):

 - What did you learn?
 - How would you apply this to something you want to do?

### Overall structure

It's worth thinking about the day as a whole. There's multiple ways that you can structure an all-day DevOps Girls workshop.

#### Option A.) The "Kata"

![The Kata](/images/CONTRIBUTING/the-kata.png)

The "Kata" is essentially a way of structuring your content so that all your modules produce roughly the same output.
Imagine an EC2, ECS, and Lambda modules all producing a standard webapp.

This approach works if you want to enable attendees by giving them the ability to distinguish between different
ways to approach a problem. *When do I use an EC2 versus a Lambda?* would be the kind of questions that they will
be able to answer.

#### Option B.) The "Castle"

![The Castle](/images/CONTRIBUTING/the-castle.png)

The "Castle" is a way of structuring your content so that your modules contribute to *one big thing*. Imagine an
EC2, RDS, and ELB module all contributing towards building a reasonably complex ecosystem.

This approach works if you want to enable attendees by giving them the experience of wiring up several systems
and making them understand how to make everything work together. AWS thrives on providing "lego blocks" that
you can stitch together, and this is a good way to highlight that.
