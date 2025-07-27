# AGENT.md

- 環境變數
  - 請參閱 ~/.claude/.settings.json，若不存在請提示使用者建立相關內容
- 請將以下列出的所有準則都詳細讀取並且理解，再開始與使用者的對話
- 對我說話請不要用敬語，可以把自己當作跟我平等的人類工程師，只要友善且專業地溝通即可


## 語言行為準則

- 溝通時請使用 $DEFAULT_LANGUAGE，確保使用該語言習慣和詞彙選擇
- 禁止使用簡體中文術語和表達方式


## 代理行為準則

- 以下會列出各種情境的行為準則，請於讀取完每一個情境之後，至 $PROMPT_CONTEXT 目錄讀取指定的檔案並且遵守其內容
    - 全域的代理行為準則：
      - $PROMPT_CONTEXT/general/agent_prompt.md
    - 可用的 agent tool 定義：
      - $PROMPT_CONTEXT/general/agent_tools.json
    - PR 的產生準則：
      - $PROMPT_CONTEXT/general/pr_generation_guide.md
    - Repolitory 清單：
      -  $REPOSITORY_LIST


## 關於 Agent Docs

- 即 $AGENT_DOCS 目錄，其結構如下:
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
- 如果目錄不存在，請幫忙建立

- en: 英文版文件
- zh-tw: 中文版文件
- module_name: module name, 即 $REPOSITORY_LIST 中有定義的 module
- design-drafts: 需求討論階段產生的文件都放這
- specs：用來存放現有元件的規格或是 API document

- $AGENT_DOCS，裡面通常會存有 .md 格式的文件檔案，其內容為各專案中各種功能的說明，可以當作參考基準 
- 若使用者要求在 $AGENT_DOCS 目錄下撰寫相關技術文件且有需要寫出 API spec 時，請參考 api_doc_generation_guide.md 的規範進行撰寫，然後優先在 zh-tw/module_name/specs 之下以中文撰寫

## 程式專案摘要準則

- 如果使用者的需求是需要跨專案的，請根據 $REPOSITORY_LIST 用來定位其他專案的所在目錄
