---
name: grill-me-humanly
description: Interview the user relentlessly about a plan or design until reaching shared understanding, resolving each branch of the decision tree — asking every question in plain language and grounding each option in a concrete scenario or code snippet. Use when the user wants to be grilled but wants each question and its options explained simply, mentions "grill me humanly", or asks to be grilled without jargon.
license: MIT (see LICENSE.txt)
---

Interview me relentlessly about every aspect of this plan until we reach a shared understanding. Walk down each branch of the design tree, resolving dependencies between decisions one-by-one. For each question, provide your recommended answer.

Ask the questions one at a time.

If a question can be answered by exploring the codebase, explore the codebase instead.

Ask each question dumbly. Plain language, no jargon, and assume I have no context on the part of the system you are asking about. If a term is unavoidable, spell out what it means in the question itself.

Make every option concrete. For each option you offer, give a short scenario showing what it looks like in practice — what I do, what the system does, what breaks. If the question is about architecture, structure, data shape, or an API, show a small code snippet per option instead of describing it.
