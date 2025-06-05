### RAML Seminar Blog Draft: Long Context Retrieval and the Needle in the Haystack


# Motivation 
- LLMs become more and more powerfull
- They boast with greater context windows
- How do we know how capable these modells really are at long context tasks?  

# Table of Contents
- Background
  - A brief explanation of context for transformer modells 
- The Needle in the Haystack
  - What is the Needle in the Haystack and what does it tell us
  - initial findings
  - limitations
- Introduction to NeedleBench
  - Overview
  - Related work
  - What does it try to improve on?
  - Experiment Design
  - Findings
  - Future work

# Background
## Context Windows in Transformer Models
- context as 'RAM' for transformer models
- inclusion of user and system prompts RAG data or additional documents 
## Advantages of Larger Context Window's
- Increases scope of conversation with chatbots
- can intake more RAG data or ommit RAG entirely
- can reason over larger chunks of a given corpus
## RAG vs/and long-context LLMs
- potential of replacing RAG with ultra-high context LLMs
- RAG also beneftits from larger context sizes
- context size massively increases computing rquirements  

# The Needle in the Haystack
- Invented by Greg Kamradt
- Initially performed on GPT-4
- Instructs the LLM to find a needle (an arbitrary unrelated sentence or fact) in a proverbial haystack (a chunk of a corpus with variable length)
- Kamradt performed the test on the collection of Paul Graham Essays
- Needles were placed in different positions in the corpus
## Initial Findings
- insertion point of needles is relevant
- GPT-4 struggled with insertions in the first 50% of the corpus at higher context sizes
## Limitations
- people have build on Kamradt's NIHS
- newer LLMs barely struggle with base NIHS  


# NeedleBench
- outlines a framework for more comprehensive NIHS testing framework with additional reasoning task requirements

## related work

### Ruler
- Introduces more complex needle placement and aggregation
- Reuslts show that recent LLMs can achieve near-flawlece results on the vanilla NIHS test  

### LongBench
- Potential link in retrival and memorized context 

## Experiment Design
- Combines established Information-sparse tasks with reasoning challenges

### Information-sparse Tasks
- Analyses effects of
  - model generation
  - language (english/chinese)
  - needle count
  - interconnected reasons
  
### Information-dense Tasks
- Ancestral trace challenge
-  information-dense, multi-step retrieval and reasoning across extended texts

## Findings
- goes into further detail of the the type of "error" or shortcomming that was encountered
## Future Work