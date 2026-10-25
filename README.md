---
title: "wasdr — DumpToDo: Turn Brain Dumps into Actionable Tasks with Local AI"
tags: devchallenge, hf26challenge, ollama, opensource , gemma
---

*This is a submission for the [Hacktoberfest Open-Source AI Challenge Week 3: Slow and Steady](https://dev.to/challenges/hacktoberfest-week3-2026-10-19)*

## What I Built

Ever had a head full of tasks, ideas, reminders, and things you need to get done — but organizing all of them feels like another task?

That's the problem I wanted to solve with **wasdr — DumpToDo**.

wasdr is an offline-first, brain-dump-to-task management app designed to turn messy notes into actionable tasks. Instead of manually breaking down every thought, you can dump your thoughts into one place and let the app organize them into a structured task list.

The goal is simple: spend less time managing your to-do list and more time actually doing the work.

### What makes it interesting?

- **Brain dumps to tasks:** Turn unstructured notes into individual, actionable tasks.
- **Priorities and time estimates:** Organize work by urgency, category, and estimated duration.
- **Subtasks:** Break larger tasks into smaller steps.
- **Task management:** Track completion, review tasks, and organize your workload.
- **Markdown export:** Export organized tasks in formats suitable for keeping your notes and task workflows together.
- **Local AI integration:** Connect to Ollama running on your own computer instead of relying exclusively on a hosted AI API.
- **Standalone HTML edition:** Run the application from a self-contained HTML file without needing a traditional application server.

The idea is to make capturing and organizing work feel effortless.

## Demo

The project is available as a standalone HTML application.

To try the local build, open the HTML file in a supported browser ( either chrome or other ). For AI-powered processing, configure Ollama and select a model that is already available on your machine or download it .

## Code

The project is packaged as a standalone HTML file, with the interface and application logic bundled into the file.

**Project:** wasdr — DumpToDo

**Repository:** A public repository .

## How I Built It

I built wasdr around a simple workflow:

1. Capture unstructured thoughts in a brain dump.
2. Process the text into individual tasks.
3. Organize those tasks with priorities, categories, estimates, and subtasks.
4. Review the results and track completion.
5. Export the organized work when needed.

The application includes a local processing path and an integration with Ollama for local model inference.

### The local AI setup

Ollama provides the local model runtime. The application connects to the Ollama API at:

`http://localhost:11434`

My local setup includes the `qwen3:4b` model , and `gemma4:e4b-mlx`. The application also supports selecting a model through its configuration.

Because a browser page and a local Ollama server have different origins, browser access may require configuring Ollama's allowed origins using `OLLAMA_ORIGINS`.

Once the model is downloaded and the local service is configured, inference can run on the user's own machine without sending prompts to a hosted model API.

The standalone application also includes local task-processing logic, so its task organization workflow is not dependent on a remote AI service for every operation.

## Why Does Open Innovation Matter?

Open innovation makes local AI experimentation accessible to individual developers.

I can run an open-weight model on my own hardware, experiment with prompts and task-processing workflows, and choose a model that fits my machine and requirements.

I don't need to make a hosted AI API the foundation of the entire experience.

This also creates opportunities for privacy-conscious workflows. When local inference is used, the text sent to the local model can stay on the user's machine rather than being sent to a third-party inference service.

There are trade-offs, of course. Model quality, response speed, and memory usage depend on the model and the available hardware. Local setup also requires some configuration.

But having the freedom to experiment, customize, and run AI locally is exactly what makes open-weight models exciting.

## The Lazy Payoff

The biggest payoff is reducing the friction between *thinking about work* and *having a clear next action*.

A brain dump lets me capture everything without interrupting my train of thought. Turning that dump into structured tasks makes it easier to see what needs to happen next.

Instead of manually converting every note into a separate task, I can use the application's processing workflow to get started faster.

The real goal isn't to automate productivity for its own sake. It's to make the overhead of staying organized smaller.

## Prize Categories
Best use of Gemma: to run and used to power the task creation from messy of notes ! :)
