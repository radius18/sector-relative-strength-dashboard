# Sector Relative Strength Classification Dashboard

A Thinkorswim/ThinkScript portfolio project focused on requirements analysis, QA/UAT, debugging, workflow refinement, and decision-support design.

## Project Overview

I designed and iteratively refined a sector-relative-strength dashboard that classifies the 11 major SPDR sectors into four states:

- **Leaders**
- **Improving**
- **Weakening**
- **Laggards**

The dashboard compares sector behavior with SPY using relative-strength and momentum rules and presents the classification directly within the Thinkorswim chart environment.

The goal was to turn a relatively abstract sector-rotation concept into an explicit, testable, and configurable workflow that could provide useful market context without being treated as a standalone trading signal.

## Working Dashboard

![Sector Relative Strength Classification Dashboard](Screenshot%202026-10-06%20002023.png)

*Working-state dashboard showing sector classifications directly on the chart. The interface groups sectors into Leaders, Improving, Weakening, and Laggards while displaying supporting relative-strength context.*

## Design and Development

The project required translating the original idea into explicit classification rules and then repeatedly testing the resulting behavior.

Development work included:

- Defining relative-strength and momentum rules
- Ensuring sectors were assigned consistently to classification buckets
- Testing behavior across different chart timeframes
- Investigating missing or incomplete output
- Refining display behavior and readability
- Troubleshooting compiler and implementation problems
- Simplifying features that did not behave reliably
- Adding configurable user controls
- Retesting revisions against the intended behavior

AI was used as an implementation and debugging aid. Requirements, test decisions, acceptance criteria, and final validation remained human-controlled.

## Implementation and Debugging

![ThinkScript implementation and debugging](Screenshot%202026-10-06%20002929.png)

*ThinkScript implementation view from the iterative development process. The code includes configurable relative-strength and momentum parameters, optional filtering, explicit timeframe handling, and defensive checks for unavailable data.*

The implementation uses explicit aggregation logic so intraday charts can rely on a more stable daily relative-strength context rather than allowing lower-timeframe noise to dominate the classification.

The development process also included testing and simplifying visual features when their behavior was not sufficiently reliable.

## User Configuration

![Sector dashboard configuration controls](Screenshot%202026-10-06%20003955.png)

*User-facing configuration view showing adjustable display settings, relative-strength lookback, momentum length, optional RSI filtering, label positioning, and classification colors.*

The configuration layer allows the same underlying workflow to provide a relatively straightforward default presentation while still exposing additional controls for users who want deeper customization.

## Classification Framework

The dashboard uses relative strength versus SPY together with the direction of that relative strength:

- **Leaders** — relatively strong and strengthening
- **Improving** — relatively weaker but gaining strength
- **Weakening** — relatively strong but losing momentum
- **Laggards** — relatively weak and deteriorating

This is intentionally a simplified classification framework rather than a formal Relative Rotation Graph implementation.

## Skills Demonstrated

- Requirements Analysis
- Quality Assurance
- User Acceptance Testing (UAT)
- Debugging
- Technical Problem Solving
- Workflow Design
- Systems Thinking
- Decision-Support Design
- ThinkScript
- Technical Documentation
- AI-Assisted Prototyping

## Project Evidence

This repository contains selected portfolio-safe screenshots illustrating:

1. The working dashboard
2. The implementation and debugging process
3. The user-facing configuration layer

Additional historical development and testing evidence remains in the private project archive.

## Scope and Limitations

This is a technical development and QA portfolio case study.

The classification logic is a simplified relative-strength framework. It should not be interpreted as financial advice, a validated predictive trading model, a formal Relative Rotation Graph methodology, or evidence of trading performance.
