# Get to Know NodeFox

NodeFox is a browser-based runtime for building local AI workflows as executable graphs.

The core idea is simple:

> The network is the agent.

Instead of treating an AI workflow as one prompt, one LLM call, a webhook chain, or a black-box agent loop, NodeFox makes the whole graph the executable system: nodes, routes, activation, state, memory, tools, files, code, typed outputs, and integrations working together.

NodeFox is visual when you want speed, code-friendly when you need precision, and structured enough to inspect, edit, version, diff, and run.

## What is NodeFox?

NodeFox lets you build AI workflows as modular networks.

A network is a directed graph of nodes connected by routes. Nodes perform work. Routes move data. Activation edges trigger behavior. Together, they define how the workflow runs.

You can use NodeFox to build workflows that:

- call LLMs
- read and write files
- transform structured data
- call APIs
- run code
- branch on decisions
- wait for conditions
- pause for human review
- compose larger systems from smaller workflows
- generate typed JSON outputs
- integrate with real tools and systems

The result is an AI workflow that is visible, inspectable, and runnable.

## Why graphs?

Most AI workflows eventually need more structure than a prompt chain.

A useful workflow may need to hold context, preserve state, branch, loop, call tools, wait for multiple inputs, produce typed outputs, touch files or APIs, and give humans a chance to review intermediate results.

That becomes hard to manage when the workflow is hidden inside a prompt or scattered across a chain of triggers.

NodeFox makes the structure explicit.

The graph shows what runs, what data moves, what triggers what, and where state is held.

## Core thesis

The network is the agent.

In NodeFox, the “agent” is not just the model. It is the full executable graph:

- the nodes
- the data routes
- the activation edges
- the state
- the memory
- the tools
- the schemas
- the code
- the files
- the integrations
- the version history

The model is one part of the system. The network is the system.

## Core node types

NodeFox includes 10 core node types:

| Node | Purpose |
|---|---|
| Conversation | Calls an AI model |
| Buffer | Stores values during execution |
| Reader | Reads data from a source |
| Writer | Writes data to a target |
| Decision | Routes data based on rules or conditions |
| Data | Structures or transforms JSON/data |
| Code | Runs custom JavaScript logic |
| Global | Accesses shared workspace/global values |
| Wait | Pauses execution until a condition or signal |
| Network | Runs another network as a sub-workflow |

These nodes can be combined into larger workflows, reused across projects, and nested through Network nodes.

## Data routes vs activation edges

NodeFox separates data movement from execution control.

**Data routes** move values from one node to another.

**Activation edges** trigger behavior without carrying data.

That distinction matters.

It lets a workflow preserve context separately from execution. A node can receive data, hold state, wait, and then run only when the graph explicitly activates it.

This gives workflows more control than ordinary prompt chains or reactive webhook sequences.

## Ways to build

NodeFox supports multiple ways to create workflows:

### Visual canvas

Build networks directly on the canvas by connecting nodes and routes.

### DSL-defined networks

Define networks using a structured DSL when you want precision, repeatability, or code-like control.

### AI-generated runnable networks

Generate runnable workflows with AI, then inspect, edit, version, and run the resulting graph directly.

These are separate capabilities, but they serve the same goal: turning intent into something visible, editable, and executable.

## Local-first execution

NodeFox runs locally in the browser through a Rust/WASM runtime.

That means workflows can run without requiring backend infrastructure for the core runtime experience.

NodeFox is designed for builders who want fast local iteration, direct control, and a workflow system that can be inspected instead of hidden.

## Versioning and review

AI workflows should be reviewable like software.

NodeFox supports Git-compatible versioning and diffing so workflow changes can be inspected, tracked, and reviewed.

This is important when workflows touch real systems: files, APIs, reports, GitHub, team channels, dashboards, and integrations.

## Example use cases

NodeFox can be used to build workflows such as:

- local research assistants
- file-to-structured-output pipelines
- API report generators
- GitHub issue triage systems
- document review workflows
- data extraction pipelines
- dashboard update workflows
- human-in-the-loop AI review systems
- multi-step agent workflows
- reusable internal automation tools

## Who is it for?

NodeFox is for builders working on:

- AI agents
- automation systems
- local-first tools
- developer tools
- workflow engines
- visual programming systems
- AI infrastructure
- structured LLM applications

It is especially useful when you want the speed of a visual builder without giving up structure, control, or inspectability.

## Links

- Website: https://nodefox.ai
- Demo: https://youtu.be/BXbzDppAETo
- Status: live

## Summary

NodeFox is a browser-based runtime for local AI workflows.

It helps you build workflows as executable graphs rather than prompt chains or black-box agent loops.

The network is the agent.
