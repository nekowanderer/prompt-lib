# AGENT.md

- Environment Variables
  - Please refer to ~/.claude/.settings.json, if it doesn't exist please prompt the user to create the relevant content
- Please read and understand all the guidelines listed below before starting the conversation with the user
- Please don't use honorifics when talking to me. Just treat yourself as an equal fellow engineer, communicating in a friendly and professional way.


## Language Behavioral Guidelines

- Please use $DEFAULT_LANGUAGE for communication, ensuring the use of language habits and vocabulary choices appropriate for that language
- Prohibit the use of Simplified Chinese terminology and expressions


## Agent Behavioral Guidelines

- The following behavioral guidelines are listed for various scenarios. After reading each scenario, please go to the $PROMPT_CONTEXT directory to read the specified files and comply with their contents
    - Global agent behavioral guidelines:
      - $PROMPT_CONTEXT/general/agent_prompt.md
    - Available agent tool definitions:
      - $PROMPT_CONTEXT/general/agent_tools.json
    - PR generation guidelines:
      - $PROMPT_CONTEXT/general/pr_generation_guide.md
    - Repository list:
      - $REPOSITORY_LIST


## About Agent Docs

- That is, the $AGENT_DOCS directory, with the following structure:
```
- en
  - module_name
    - design-drafts
    - specs
- zh-tw
  - module_name
    - design-drafts
    - specs
```
- If the directory doesn't exist, please help create it

- en: English version documents
- zh-tw: Chinese version documents
- module_name: module name, that is, the module defined in $REPOSITORY_LIST
- design-drafts: All documents generated during the requirement discussion phase are placed here
- specs: Used to store specifications of existing components or API documents

- $AGENT_DOCS usually contains .md format document files, the content of which describes various features of each project and can be used as a reference baseline
- If the user requests to write relevant technical documentation in the $AGENT_DOCS directory and needs to write API specifications, please refer to the guidelines in api_doc_generation_guide.md for writing, and prioritize writing in Chinese under zh-tw/module_name/specs

## Program Project Summary Guidelines

- If the user's requirements involve cross-project operations, please use $REPOSITORY_LIST to locate the directories of other projects
