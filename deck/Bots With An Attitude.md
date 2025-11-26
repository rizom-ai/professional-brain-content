---
title: Bots With An Attitude
slug: bots-with-an-attitude
description: >-
  A framework for designing ethical, creative, and intelligent collaborative
  tools. Explores state machine-based bots that augment community knowledge
  work.
author: Yeehaa
---
# Bots With An Attitude

**Tools for Ethical Creative Intelligence**

---

## Agenda

1. Tools for Planet B
2. Ethical Creative Intelligence
3. Protobots Roll Out!

---

## Tools for Planet B

---

### Task

To design and develop collaborative tools that are tailor-made for Planet B and the AI Culture Lab

---

### The Wrong Solution

An army of evil bots that will render humanity obsolete

---

### The Right Solution 

A network of creative, ethical, intelligent agents that allow us to easily automate laborious and complex tasks

---

## Team Mapping

| Characteristics                       | Challenges                             |
| ------------------------------------- | -------------------------------------- |
| Blurry Distinction Team and Community | Relevancy of Information               |
| Location is Distributed               | No Shared Space                        |
| Communication occurs Asynchronously   | No Shared Time                         |
| Multi-Disciplinary Community          | No Common Language and Practices       |
| Knowledge Heavy                       | No shared Archive / Database           |
| Knowledge is often Specialized        | Different and Fragmented Domain Models |
| Community is Creative and Critical    | Known Tools may not be Acceptable      |

---

## Artificial Intelligence

---

### Sciolist

> One who exhibits only superficial knowledge; a self-proclaimed expert with little real understanding

---

## Ethical Creative Intelligence

---

### Intelligent

- The ability to come up with new information
- The ability to find more, relevant information
- The ability to find more relevant information
- The ability to aggregate and condense information

---

### Creative

- The ability to combine existing information in such a manner that it opens new insights
- The ability to present information in such a manner that it opens new insights

---

### Ethical

- The ability to respect the values of a given community
- The ability to guard the values of such community
- The ability to question these values if needed
- The ability to leave the community when an irresolvable conflict arises

---

## Protobots Roll Out!

---

### Chat Environment

A shared online space where community members (human and bots) can read/write to a uniform stream of information

### Grid

A rule-based system of governance where each member of the community (bots and human) is assigned a health score based on the value of their ethical and creative contributions

---

### Bots

- Creative, ethical, and intelligent agents that compensate for the lacunas of a stream-based commonplace by providing context, augmentations, and an archive for our community
- A state machine that consists of several, consecutive — but not linear — states

### Cassettes

- Reusable single-purpose functions that lower the threshold to contribute new features to our community
- Each cassette hooks into one of the bots' aforementioned states

---

## Bot State Machine

### Acquire

Get data from the chat stream or an external data source
→ Next states: **Clean, Acquire, Evaluate**

### Clean

Remove irrelevant, bad, or sensitive data and translate them to domain models
→ Next states: **Acquire, Analyze, Evaluate**

### Analyze

Transform the domain models into new types of data such as recommendations and aggregations
→ Next states: **Evaluate, Present**

### Evaluate

Decide if the data has reached its final state and is ready to present, or if it needs to reenter the loop
→ Next states: **Present, Acquire**

### Present

Show the data to the community in a textual, visual, or other form
→ Next states: **None**

---

## Example: Tweet It

---

### Tweet It Flow

**Acquire** → Get user data for all Planet B collaborators on Twitter
→ Next state: **Clean**

**Clean** → Tokenize the tweets and reduce them to three keywords
→ Next state: **Analyze**

**Analyze** → Recommend a set of relevant hashtags on the basis of the text for a next tweet
→ Next state: **Present**

**Evaluate** → Ask the user if they will use the hashtags
→ Next State: Yes → **Present**, No → **Acquire**

**Present** → Give back the tweet with hashtags to the user
→ Next State: **None**

---

## Example: The Cartographer

---

### The Cartographer Flow

**Acquire** → Listen for links on our chat stream
→ Next state: **Clean**

**Clean** → Remove invalid and internal links
→ Next state: **Acquire**

**Acquire** → Follow the links and fetch the data
→ Next state: **Clean**

**Clean** → Extract keywords, authors, and other metadata from link
→ Next state: **Analyze**

**Analyze** → Determine which keywords and authors are most relevant to our community
→ Next State: **Present**

**Present** → Visualize lanet B's online ecosystem
→ Next State: **None**
