# CS 499 Capstone - todointc Enhancement Project

Student: Dylan Miller
Course: CS 499 Computer Science Capstone
Institution: Southern New Hampshire University
Term: Fall 2025

## About This Project

ToDoInTC is Decided, LLC's first in-house app. I founded Decided in March of 2024 as a Mobile and Web Application development company. ToDoInTC is a production iOS and Android app that consolidates all of Traverse City, MI events into one intuitive and user friendly app. This project will enhance the backend infrastructure and services to produce a more development friendly, and hosted environment as opposed to the services right now which run locally, and require tedious labor when switching from development to production environments.

This portfolio documents my work enhancing todointc services repository, a distributed event scraping system I built for aggregating local event data. The system uses four microservices that communicate through Kafka to discover, extract, and process event information from websites.

The enhancements focus on three main areas:
- Software engineering and design (infrastructure)
- Algorithms and data structures (service control and URL processing)
- Database management (API optimization)

## How It Works

The system has four services that work together:

**Scout** - Finds event-related URLs using a list of domains and AI classification
**Farmer** - Extracts specific event URLs from discovered pages with domains
**Miner** - Pulls structured data from individual event pages and/or event calendars
**Healer** - Transforms and validates data for the production database

They communicate through Kafka message queues, with Scout passing URLs to Farmer, Farmer to Miner, and Miner to Healer.

## What I'm Improving

### Infrastructure (Software Engineering & Design)
The current system runs everything in one Docker Compose environment with no separation between development and production. I'm implementing:
- **Blue-green development environment** - Complete separation of development from production environments using Kubernetes
- **Kubernetes context switching** - Ability to switch between dev and prod contexts for management and monitoring (kubectl logs, pod inspection, etc.)
- **Fly.io production deployment** - Production environment hosted on Fly.io with ability to pull new image artifacts to update one or more containers
- **Zero-downtime updates** - Deploy new versions without service interruption

### Service Control (Algorithms & Data Structures)
Currently, services can only be started or stopped via Docker Compose, requiring full restarts. I'm adding:
- **Container lifecycle management** - Start, restart, pause, and stop functionality for each individual container
- **Granular service control** - Ability to control services independently without affecting the entire system

### URL Processing (Algorithms & Data Structures)
Right now Scout processes all URLs from a static config file with no selective processing. I'm building:
- **URL flag system** - Command line flags to process a single URL or a range from a starting point to the end of the list
- **Flexible URL selection** - Target specific URLs for processing without running the entire list

### API Optimization (Database Management)
The system currently sends all scraped data to the OpenRouter API, wasting tokens on invalid or duplicate events. I'm implementing:
- **Pre-validation filtering** - Pass only description, title, and date to determine if the event is valid and/or a duplicate
- **Selective data transformation** - Only send full scraped data to OpenRouter API for events that pass validation
- **Token usage reduction** - Minimize API costs by filtering out invalid and duplicate events before transformation

## Tech Stack

Python, Docker, Kubernetes, Fly.io, Kafka, PostgreSQL, MongoDB, Playwright for web scraping, OpenRouter API for AI classification and data transformation

## Source Code Access

The actual code is in a private repository at github.com/dy1b0t/todointc since this is a real project I use in production. My instructor will have collaborator access to review everything.

This public repo just has the documentation and enhancement narratives without exposing the source code.

## Portfolio Contents

- Professional self-assessment
- Code review video (10-15 min walkthrough)
- Three enhancement narratives with before/after comparisons
- Pseudocode and flowcharts for the improvements

## Timeline

Week 1: Code review and initial plan
Weeks 2-3: Blue-green environment setup with Kubernetes and Fly.io deployment
Weeks 4-5: Container lifecycle management (start/restart/pause/stop)
Weeks 6-7: URL flag processing and API optimization
Week 8: Final testing and documentation

## Running It

If you have access to the private repo, the current setup includes the following:

```bash
git clone https://github.com/dy1b0t/todointc.git
cd todointc
cp .env.example .env
# add your API keys and database credentials
docker-compose up -d