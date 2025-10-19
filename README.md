# like-as-though-not-a-benchmark
the model and some similes and Dubliners 

Weakly supervised, strongly opinionated style coding for Joyce’s Dubliners

Linguistics first. ML can keep up.

What is this: repo trains and tests a Joyce-aware simile extractor and category classifier over Dubliners, using spreadsheet as seed supervision to generate silver labels for the full text. The goal is to push recall on Joycean comparators, model CST categories, and do it with style.

Why this exists: Because a lot of “language” work ignores linguistics. This does not. This mixes:
Seed rules / label functions from similes data
Weak supervision over the full Dubliners text
Simple, readable models (LinearSVC, LDA)
Error analysis that invites close reading, not just metrics
