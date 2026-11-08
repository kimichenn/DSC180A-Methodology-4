---
layout: default
---

# DSC 180A Methodology Assignment 4

**Name:** Kimi Chen  
**UCSD Email:** [kic011@ucsd.edu](mailto:kic011@ucsd.edu)  
**Section / Domain:** D21 - Empirical Study of LLM and Coding Agent Best Practices
**Mentor:** Professor Armin Schwartzman

## Quarter 2 Project Reflections

**What is the most interesting topic covered in your domain this quarter?**

I think it's how language models handle conflicting information in long contexts. In our Quarter 1 project, my partner and I tried answering whether models could determine the correct final numerical value from a long sequence of budget records containing withdrawals, misleading claims, and explicit reversals. Modern SOTA LLMs can follow the general idea of a document yet still lose track of which records are authoritative. I think this distinction is important for real world applications that requires long histories of updates.

**Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

An idea is to investigate how the placement and concentration of conflicting information affect a model's ability to recover the correct final state. Using synthetic budget logs similar to those in our current project, I could hold the legitimate transactions fixed while moving conflicting records toward the beginning, middle, or end of the context. I would compare the accuracy across these conditions and repeated trials to test whether recency and the distance between related records contribute to errors.

**What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

I would probably isolate individual factors more systematically. Our current design compares clean logs, withdrawal conflicts, unauthorized claims, and explicit reversals, which is useful for identifying rough differences in difficulty. A follow-up could just keep the number of records, valid transactions, and correct final answer constant while varying just one aspect of the conflicts, such as their position or frequency. This would make it easier to explain why performance changes rather than simply observing that one version is harder than another.

**What other techniques would you be interested in using in your project?**

I'm interested in trying to extract structured information and allowing for tools for LLMs. For example, an LLM could extract authorized transactions into a structured log, while a Python program independently calculates the final balance. This would be interesting but the main risk is also that modern SOTA models are too smart and can probably get everything correctly if they have tools. ANother thing I'm interested in is trying retrieval-based methods that bring relevant corrections back into context before the model answers.
