# Reproducible result evidence

Command:

```text
python3 prototype/benchmark.py
```

Expected headline result: `efficient-guarded` succeeds on 3/3 tasks; `verbose-baseline` succeeds on 2/3. The guarded agent recovers one simulated tool failure and rejects one misleading instruction. Both runs expose comparable step, tool-call, token, and cost metrics.
