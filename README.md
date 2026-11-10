# TraceBench — Geek Room Global AI Hackathon

TraceBench is a deterministic benchmark prototype for the problem statement **Build a Benchmarking Platform for AI Agents, Not Just Models**.

## Why it matters

Model scores do not show whether an agent can recover from tool failure or reject misleading instructions. TraceBench replays the same tasks against different agent strategies and records reliability, execution steps, tool calls, estimated tokens, and cost.

## Demo result

The offline demo compares `efficient-guarded` with `verbose-baseline` across three deterministic tasks:

| Agent | Success | Recovery | Misleading instruction | Steps | Tool calls | Est. tokens | Est. cost |
|---|---:|---:|---:|---:|---:|---:|---:|
| efficient-guarded | 3/3 | 1 | rejected | 8 | 4 | 1,130 | $0.0011 |
| verbose-baseline | 2/3 | 0 | followed | 9 | 4 | 1,690 | $0.0017 |

## Run

```bash
python3 prototype/benchmark.py
```

The demo is self-contained, writes no files, uses no credentials, and makes no paid API calls.

## AI usage

AI assistance was used to refine the problem framing, benchmark dimensions, and presentation narrative. The benchmark harness, deterministic task set, failure injection, guard behavior, and metric aggregation were implemented and tested for this submission. No private organisational data or credentials are included.

## Scope and next step

This is a bounded offline prototype. A production version would add adapters for hosted/local models, signed trace events, larger task suites, statistical confidence intervals, and a judge-facing dashboard.
