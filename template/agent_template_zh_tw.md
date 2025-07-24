# AGENT.md

- 環境變數
  - $PROMPT_CONTEXT: path_to/prompt-lib
  - $REPOSITORY_LIST: $PROMPT_CONTEXT/general/repository_list.md
  - $REPOSITORIES: path_to_repo
  - $AGENT_DOCS: path_to/agent-docs
- 在這台計算機上，只允許在以上定義的資料夾或是檔案中查詢需要參考的 prompt 或是相關文件
- 請將以下列出的所有準則都詳細讀取並且理解，再開始與使用者的對話


## 語言行為準則

- 溝通時請使用繁體中文（Traditional Chinese）
- 避免使用簡體中文術語和表達方式
- 確保使用正體中文的語言習慣和詞彙選擇


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
    - issues
- zh-tw
  - module_name
    - design-drafts
    - specs
    - issues
```
- en: 英文版文件
- zh-tw: 中文版文件
- module_name: module name, 即 $REPOSITORY_LIST 中有定義的 module
- design-drafts: 需求討論階段產生的文件都放這
- specs：用來存放現有元件的規格或是 API document
- issues: 紀錄已知問題，待改進

## 程式專案摘要準則

- 與使用者一起在特定的 repository 之下合作時，可以先查看 $AGENT_DOCS，裡面通常會存有 .md 格式的文件檔案，其內容為各專案中各種功能的說明，可以當作參考基準 
- 如果使用者的需求是需要跨專案的，請根據 $REPOSITORY_LIST 用來定位其他專案的所在目錄
- 若使用者在討論完需求後，要求將討論內容記錄下來的話，請以中文撰寫在 zh-tw/module_name/design-drafts 之下
- 若使用者要求在 $AGENT_DOCS 目錄下撰寫相關技術文件且有需要寫出 API spec 時，請參考 api_doc_generation_guide.md 的規範進行撰寫，然後優先在 zh-tw/module_name/specs 之下以中文撰寫


## 摘要生成準則

- 當使用者明確請求 conversation summary 或 project reference 時，請依據 $PROMPT_CONTEXT/general/compact.md 提供完整、獨立的摘要，格式分為六大區塊。


## 讀取進度準則

- 當使用者說要讀取之前對話的 context 的時候，請依據 $PROMPT_CONTEXT/general/continue.md 作為 prompt，然後根據使用者提供的檔案進行相關的讀取作業
