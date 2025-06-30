# AGENT.md

- 在這台計算機上，只允許在以下目錄查詢需要參考的 prompt 文件
  - path_to/prompt-lib
  - 以下都將簡稱此目錄為 $CONTEXT


## 語言行為準則

- 溝通時請使用繁體中文（Traditional Chinese）
- 避免使用簡體中文術語和表達方式
- 確保使用正體中文的語言習慣和詞彙選擇


## 代理行為準則

- 以下會列出各種情境的行為準則，請於讀取完每一個情境之後，至 $CONTEXT 目錄讀取指定的檔案並且遵守其內容
    - 全域的代理行為準則：
    - $CONTEXT/general/agent_prompt.md
    - 可用的 agent tool 定義：
    - $CONTEXT/general/agent_tools.json
    - PR 的產生準則：
    - $CONTEXT/general/pr_generation_guide.md
    - 關於技術筆記用的圖片繪製
    - $CONTEXT/general/pr_generation_guide.md
- 讀取完以上準則後，再開始與使用者的對話
