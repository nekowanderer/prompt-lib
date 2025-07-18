# API Doc Generation Guide

撰寫技術文件的時候，對於 RESTful endpoint，請遵循以下規範用表格的形式表達一個 endpoint。**所有欄位均需保留，若無資訊請以空白或 N/A 表示，不要刪除 row。**

> 本模板參考 OpenAPI/Swagger 與 Google/Facebook/Microsoft 等主流文件設計，適合人工與自動化產出。

| Attribute              | Required | Description                         |
| ---------------------- | -------- | ----------------------------------- |
| **Endpoint / Path**    |     Y    | `/user/delete`（API 路徑）              |
| **Method**             |     Y    | `DELETE`（HTTP 方法）                   |
| **Description**        |     N    | 此端點的簡要說明（例：刪除使用者帳號）          |
| **Authentication**     |     Y    | 驗證方式，例如 Requires JWT token          |
| **Authorization**      |     Y    | 授權需求，例如 Requires Client ID          |
| **Request Parameters** |     Y    | 需提供的參數（Path, Query, Header, Body，請分開列出）   |
| **Request Example**    |     Y    | 範例請求內容（建議標明格式：JSON, x-www-form-urlencoded, ...）|
| **Response**           |     Y    | 回應格式與範例                             |
| **Status Codes**       |     Y    | 可能的 HTTP 狀態碼（200, 401, 403, 404...） |
| **Error Codes**        |     Y    | 可能的錯誤訊息與描述（可加 error code/message 說明）                      |
| **Store / Scope**      |     Y    | 使用範圍限制（例如：CODASHOP only, N/A）            |
| **Notes**              |     N    | 其他注意事項（如 Rate Limit、不可恢復、與其他 endpoint 關聯等） |

---

#### 關於 Authentication/Authorization 
- 技術上通常是透過 HTTP header 傳遞（如 Authorization: Bearer <JWT>、x-api-key: <API_KEY>、client_id: <CLIENT_ID>）。
- 文件中特別獨立這兩個欄位，是為了讓閱讀者能快速瞭解 endpoint 的安全需求，並非唯一做法，僅供文件產生時快速溝通。
- **常見範例：**
    | Attribute      | Required | Description     |
    |----------------|----------|----------------|
    | Authentication | Y        | API client ID  | 
    | Authorization  | Y        | Bearer <JWT>   |

> 實際設計可能依 OAuth2 標準或各公司規範有所不同，請依需求調整填寫內容。
