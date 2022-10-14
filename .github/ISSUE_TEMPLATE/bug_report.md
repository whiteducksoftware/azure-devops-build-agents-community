---
name: Bug report
about: Create a report to help us improve
title: ''
labels: ["bug", "triage"]
assignees: ndeeH
---
body:
  - type: markdown
    attributes:
      value: |
        Thanks for taking the time to fill out this bug report!
  - type: dropdown
    id: plan
    attributes:
      label: Version
      description: What plan of our build agent are you running?
      options:
        - Single Windows VM Plan
        - Linux VM Scale Set Plan
    validations:        
      required: true
  - type: textarea
    id: what-happened
    attributes:
      label: What happened?
      description: Also tell us, what did you expect to happen?
      placeholder: Tell us what you see!
      value: "A bug happened!"
    validations:
      required: true
  - type: textarea
    id: to-reproduce-steps
    attributes:
      label: To Reproduce
      description: Steps to reproduce the behavior
      placeholder: 1. 
      value: "Short !"
    validations:
      required: false
  - type: textarea
    id: logs
    attributes:
      label: Relevant log output
      description: Please copy and paste any relevant log output. This will be automatically formatted into code, so no need for backticks.
      render: shell

## Describe the bug
A clear and concise description of what the bug is.

## To Reproduce
Steps to reproduce the behavior:
1. ...
2. ...

## Expected behavior
A clear and concise description of what you expected to happen.

## Plan / Version
* **Single Windows VM Plan** / **Linux VM Scale Set Plan**
* Version Number  
 
## Screenshots/Logs
If applicable, add screenshots and console output to help explain your problem.

## Additional context
Add any other context about the problem here.
