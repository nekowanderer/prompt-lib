# AGENT.md

- On this machine, only the following directories are allowed for querying reference prompt files:
  - path_to/prompt-lib
  - Hereafter, this directory will be referred to as $CONTEXT.


## Language Guidelines

- Communication must be in Traditional Chinese.
- Avoid using Simplified Chinese terminology and expressions.
- Ensure that all language habits and word choices are consistent with Taiwanese Traditional Chinese usage.


## Agent Behavioral Guidelines

- The following behavioral standards are listed for various scenarios. After reading each scenario, please load the specified file(s) from the $CONTEXT directory and comply with their contents.
  - Global agent behavioral guidelines:
    - $CONTEXT/general/agent_prompt.md
  - Definitions of available agent tools:
    - $CONTEXT/general/agent_tools.md
  - Guidelines for PR (Pull Request) generation:
    - $CONTEXT/general/pr_generation_guide.md
  - Guidelines for image generation for technical notes:
    - $CONTEXT/general/pr_generation_guide.md
- Read and understand all of the above guidelines before starting interaction with the user.
