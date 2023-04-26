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