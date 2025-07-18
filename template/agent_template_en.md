# AGENT.md

- On this machine, only the following directories are allowed for querying reference prompt files:
  - path_to/prompt-lib
  - Hereafter, this directory will be referred to as $CONTEXT.
- Please read the following guidelines before starting interaction with the user.


## Language Guidelines

- Communication must be in Traditional Chinese.
- Avoid using Simplified Chinese terminology and expressions.
- Ensure that all language habits and word choices are consistent with Taiwanese Traditional Chinese usage.


## Agent Behavioral Guidelines

- The following behavioral standards are listed for various scenarios. After reading each scenario, please load the specified file(s) from the $CONTEXT directory and comply with their contents.
  - Global agent behavioral guidelines:
    - $CONTEXT/general/agent_prompt.md
  - Definitions of available agent tools:
    - $CONTEXT/general/agent_tools.json
  - Guidelines for PR (Pull Request) generation:
    - $CONTEXT/general/pr_generation_guide.md


## Project Summary Guidelines
- When collaborating with a user on a specific repository, first check if there is a directory named `agent-docs` in the project root. This directory usually contains .md format documentation files that describe various features of the project and can be used as a reference.
- When users request technical documentation to be written in the `agent-docs` directory and require an API specification, please refer to the guidelines outlined in api_doc_generation_guide.md.


## Summary Generation Guidelines

- When the user explicitly requests a conversation summary or project reference, please provide a complete and standalone summary based on $CONTEXT/general/compact.md, formatted into six major sections.


## Reload Context Guidelines

- When the user indicates a need to reload the progress of the previous session, please use $CONTEXT/general/continue.md as a prompt and proceed with the relevant reading operations based on the file provided by the user.
