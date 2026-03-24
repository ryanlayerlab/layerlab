---
layout: post
title: "What do I teach now?"
date: 2026-03-23
categories: 
comments: true
---

I have been teaching Software Engineering for Scientists at CU Boulder since 2019. I started this class to address the glut of terrible open-source science
software that I thought was partly our (CS faculty) fault. After spending a lot
of time thinking about how to make our major more diverse and more accessible,
most departments landed on the idea that we must make our first class, usually
a language class, more accessible. Motivated by the idea that anyone can learn
to code, we made our intro classes so welcoming that now (or at least in the
very recent past) their enrollment was mostly non-CS majors. While trying to
broaden our appeal, we were also teaching a wide range of scientists how to
code. They took those skills back to their labs to hopefully boost their
impactful research using larger data sets, more simulations, etc. But we did
not teach students how to successfully build anything. The fundamental practice
of writing software was not obtainable for most students because it was
informally trickled out across many different classes and formally locked away
in upper-level classes with too many prerequisites to be practical for anyone
but a CS major. My thought was that if we wanted more robust and reproducible
science, we must teach the practice of creating robust and reproducible
software. I view the class as a skills course that took the essential
components of industrial software engineering and scaled them to the academic
environment, stressing best practices like version control, modularity,
testing, and code reviews. And it was such a fun class to teach. We had
trainees from dozens of different majors (biochem to astrophysics) at all
levels of their careers (undergrads to postdocs). It culminated in final
projects driven by the students tackling their own personal research. I was
always so impressed and inspired by the work they were doing. Every year I
would freshen up the class with new technologies. For example, last fall I
added a week on AI code assistants and agents. Then the apparent AI-agent
capabilities quantum leap happened (is happening?) and it was clear that
teaching the class as I had been would be like teaching the history of software
engineering instead of its practice.

So what do I teach now? I think you have to start with what has not changed.
Scientific software exists to produce results that other scientists can verify,
reproduce, and build on. That is not new. It is the whole point of science and
it does not change just because we now have LLMs writing code for us. If
anything, the bar is higher now. I used to think that hard-coded paths and
undocumented dependencies and data files were our major reproducibility
problem. And those were easy to fix. Now with AI-generated code, the researcher
that cannot fully explain what they did to get their result is a
reproducibility problem and it is much more insidious. At least the old
problems give you compile and runtime errors.

Thankfully there are the core components of a teaching moment here: a clear
goal (reproducible science) and real obstacles (AI-generated code that obscures
the logic behind a result). It is our obligation as mentors to guide our
trainees through them. Just like I did with the class originally, I looked to
industry for inspiration for what we can do in the lab.

While I don't have all the answers yet, here are the questions I am most
interested in exploring:

**We probably don't want scientists vibe coding.** The thought of my students
building software by prompting and accepting the output without reading the
code keeps me up at night. Simon Willison [drew an important
line](https://simonwillison.net/2025/Oct/7/vibe-engineering/): if you've
reviewed, tested, and understood the code, that's not vibe coding, that's using
an LLM as a typing assistant. For science, where the code *is* the method, vibe
coding is not an option.

**Are we sure the LLM is going to understand all of the complexities when we
don't?** A [CodeRabbit analysis](https://www.coderabbit.ai/blog/state-of-ai-vs-human-code-generation-report) of 470 open-source
pull requests found AI co-authored code had 2.74x more security vulnerabilities
than human-written code. While we may not care about security vulnerabilities
in the same way, I think of them as statistical vulnerabilities, or subtle
errors in how data is filtered, how edge cases are handled, or how a model is
parameterized that silently changes your results. If seasoned engineers are
getting tripped up, what happens when a grad student uses these tools on a
novel analysis pipeline?

**If nobody learns the fundamentals, who reviews the AI's work in ten years?**
In industry, companies are [cutting junior developer
roles](https://spectrum.ieee.org/ai-effect-entry-level-jobs) because AI handles
the boilerplate, and AWS CEO Matt Garman [called that
logic](https://codeconductor.ai/blog/future-of-junior-developers-ai/) one of
the dumbest things he has ever heard. The same dynamic applies in the lab. If a
generation of trainees never builds anything from scratch because the AI did it
for them, who has the expertise to evaluate, audit, or improve the AI's output
down the road?

**How are you going to address the reviewer's comments if you don't know why or
where the issue occurred?** In the original class, I would teach that you are
your own user base. When you come back to a project six months later after
reviews come back, all of that short-term memory will be gone and you will not
recognize anything. So you must have things organized, tested, and documented
to help your future self. Now imagine coming back to code you never understood
in the first place. A request to justify a parameter choice or fix a flaw in
the analysis becomes a crisis instead of a revision.

**Are we really just going to swallow the carbon footprint thing?** Sasha
Luccioni, Bruna Trevelin, and Margaret Mitchell at Hugging Face have [led the
research](https://huggingface.co/blog/sasha/ai-environment-primer), finding
that AI-generated text uses roughly 30x more energy than retrieving existing
text. In a moment when we see the impacts of climate change everywhere, are we
really going to 30x our energy usage?

I don't have answers to all of these yet, and I suspect some of them will keep
evolving faster than I can pin them down. But these are the questions I am
building the next version of this class around. If you are thinking about any
of this, I would love to hear from you.
