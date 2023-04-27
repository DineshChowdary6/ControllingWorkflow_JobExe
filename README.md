# ControllingWorkflow_JobExe

# steps context
https://docs.github.com/en/actions/learn-github-actions/contexts#steps-context

# Operators
 https://docs.github.com/en/actions/learn-github-actions/expressions#operators

# Special  Conditional Functions
1. failure()
- Returns true when any previous step or job failes
2. success()
- Returns true when none of the previous steps have failed
3. always()
- Causes the step to always execute, even when cancelled
4. cancelled()
- Returns true if the workflow has been cancelled.

# cache 
https://github.com/actions/cache#outputs

- caching node_modules when using *npm ci* is not recommended because *npm ci* will always delete any existing *node_modules* folder and re-create it. 
- here we are preventing the *npm ci* step if cache *node_modules* folder is found
- if we cache *node_modules* and conditionally run *npm ci* (only if no cached *node_modules* folder exists we are saving time,) 

# Matrix


 continue-on-error: true
 
    strategy:
      matrix:
        node-verson: [12, 14, 16]
        operating-system: [ubuntu-latest, windows-latest]