---
title: Decisions in an uncertain and changing world
tag: reinforcement_learning
layout: research_topic
current: 1
people:
  - maarten
blurb: How do people learn to make better decisions from experience?
image: igor-ovsyannykov-440138.jpg
image_credit: Photo by Igor Ovsyannykov on Unsplash

---
Traditionally, research on decision making has focussed on
"decisions from description", for instance asking people to choose between
two monetary gambles. Decades of research in this paradigm has led to the
conclusion that human decisions are generally irrational (e.g., defying
the laws of expected utility theory). In daily life, however, people
rarely decide between options that are as precisely and exhaustively
described as the gambles in traditional decision-making experiments.
Rather, they need to learn to make decisions based on their own direct
experiences in uncertain and noisy environments. Results from traditional
studies often do not generalize to experience-based decision making. For
instance, given sufficient experience, violations of expected utility
theory tend to diminish {% include citation.md
tag="speekenbrink2013decisionmaking" cite = "(Speekenbrink & Shanks, 2013)" %}.
Even when descriptions are provided, people rely more strongly on their experience
{% include cite.md tag="weiss2016incorporating" text = "(Weiss-Cohen et al., 2016)" %}.

Experience-based decisions are initially highly uncertain: people can
only learn about the likely outcomes of their decisions by taking them
and experiencing their consequences. This leads to an
exploration-exploitation tradeoff: in uncertain environments, we should
sometimes forego actions that we think are most rewarding (exploitation)
in order to learn about the consequences of other actions with more
uncertain outcomes (exploration). For instance, rather than always
revisiting your favourite restaurant, it can be good to sometimes visit a
new restaurant in order to see whether it is better than your current
favourite. Exploration is especially pertinent in changing environments,
where once optimal options can be overtaken by once poor options. This
means the uncertainty about options should increase the longer they
haven’t been tried. We showed that explorative decisions are guided by
such uncertainty and that people explore more when the environment changes
rapidly {% include cite.md tag="speekenbrink2015uncertaintyproblem" text="(Speekenbrink & Konstantinidis, 2015)" %}. A relatively simple
mechanism accounted for people’s decisions, sampling for each option a
reward from a subjective predictive distribution and choosing the option
with the highest sampled reward. This results in a “probability matching”
strategy where options are chosen according to the subjective probability
that they provide the highest reward. Whilst probability matching has
long been thought irrational, this strategy naturally combines exploitation
and exploration and is near-optimal in complex and changing environments.
Subsequent research (Schulz et al., 2015) again showed evidence for this
probability matching strategy and further converging evidence comes from
previous work {% include cite.md tag="speekenbrink2010learningenvironment" text="(Speekenbrink & Shanks, 2010)" %} which showed that people make
predictions in changing environments by sampling from subjective
(Bayesian) distributions.
