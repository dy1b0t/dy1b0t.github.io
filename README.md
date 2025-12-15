# CS 499 Capstone – ToDoInTC Backend Enhancement Project

**Student:** Dylan Miller  
**Course:** CS 499 Computer Science Capstone  
**Institution:** Southern New Hampshire University  
**Term:** Fall 2025  

---

## Project Overview

This repository supports my CS 499 Computer Science Capstone ePortfolio.  
It documents the enhancement of **ToDoInTC**, a production backend system developed by Decided, LLC to aggregate and normalize local event data for Traverse City, Michigan.

The objective of this capstone is to **demonstrate professional growth** by enhancing an existing real-world system across the three required computer science categories:

- Software Engineering and Design  
- Algorithms and Data Structures  
- Databases  

All enhancements were implemented with production constraints in mind, including reliability, cost efficiency, scalability, and operational control.

---

## Primary Artifact

**Artifact:** ToDoInTC backend services (distributed event ingestion pipeline)

This artifact includes multiple microservices responsible for discovering, validating, classifying, and persisting event data. The same artifact was enhanced across all three categories to clearly demonstrate technical growth and system-level thinking.

> **Note:** Production source code is private due to commercial use.  
> Instructor access can be granted upon request.

---

## Enhancement Overview

### Software Engineering & Design
- Environment separation (development vs. production)
- Blue-green deployment strategy
- Safer rollout and rollback procedures
- Improved operational readiness

Narrative:  
[Enhancement One – Software Engineering & Design](./narratives/enhancement-one-software-engineering.docx)

---

### Algorithms & Data Structures
- Index-based and range-based URL selection
- Deterministic input parsing and validation
- Persistent run-state tracking for pause/resume/restart
- Controlled ingestion without container restarts

Narrative:  
[Enhancement Two – Algorithms & Data Structures](./narratives/enhancement-two-algorithms-data-structures.docx)

---

### Databases
- Pre-validation layer to detect duplicates
- Reduced AI token usage via early rejection
- Improved data integrity and cost efficiency
- PostgreSQL and MongoDB integration

Narrative:  
[Enhancement Three – Databases](./narratives/enhancement-three-databases.docx)

---

## Code Review Video

An informal code review was recorded prior to implementing enhancements.  
The video explains existing functionality, identifies improvement areas, and outlines planned enhancements aligned to CS 499 course outcomes.

Code Review Video:  
[Watch the Code Review]([https://youtu.be/wECHh179bGc](https://youtu.be/wECHh179bGc))

---

## Professional Self-Assessment

The professional self-assessment serves as the formal introduction to the ePortfolio.  
It reflects on my growth throughout the Computer Science program and connects my coursework, enhancements, and career goals.

Professional Self-Assessment:  
[Professional Self-Assessment](./professional-self-assessment.docx)

---

## Tech Stack

- Python
- Docker
- Kafka
- PostgreSQL
- MongoDB
- Playwright
- Fly.io

---

## Repository Contents

This repository contains:
- Professional self-assessment  
- Code review video link  
- Three enhancement narratives  
- Pseudocode and flow diagrams  
- Supporting documentation for CS 499 review  

The live ePortfolio is hosted using GitHub Pages.

ePortfolio URL:  
[Here](https://github.com/dy1b0t/dy1b0t.github.io)

---

## Source Access

The private production repository is hosted at:

https://github.com/dy1b0t/todointc  

Instructor access is available upon request.  
This public repository exists solely to satisfy CS 499 ePortfolio presentation requirements.

---

## Course Outcome Coverage

This project demonstrates proficiency in all CS 499 course outcomes, including:
- Collaborative system design
- Professional technical communication
- Algorithmic problem solving
- Modern tools and deployment practices
- Security-aware and cost-aware data handling

Evidence is provided through artifact enhancements, narratives, and the professional self-assessment.
