
## API 格式

### GET /posts
網址參數用法：
- 參數名 `timeSort` 是否有 `asc` 值，有值有舊到新；沒值有新到舊
- 參數名 q 使用正則表達式以 JS `new RegExp(<網址參數>)` 轉 mongDB 語法 `.find( parName: /<查尋字串>/)`，以物件包裝查找留言。

### POST /posts
``` JSON
// JSON 格式
{
  "userName": "邊綠小杰",
  "userPhoto": "https://unsplash.it/500/500/?random=4",
  "discussContent": "外面看起來就超冷…\n\r我決定回被窩繼續睡…>.<",
  "discussPhoto": "https://images.unsplash.com/photo-1485594050903-8e8ee7b071a8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=900&h=350&q=80"
}
```

## 環境與套件與指令

專案 clone 或是沒有 node_modules 資料夾情形下，而下指令透 NPM 載下專案所需的套件。
```
npm i
```

- 執行 `npm run dev`：開發時結合 Node 環境變數於指令使用，需與 `nodemon` 全域套件使用，在配合下指令 會直接由變數指向 mongoDB 本地端資料庫。
- 執行 `npm run server`：開發時結合 Node 環境變數於指令使用，需與 `nodemon` 全域套件使用，在配合下指令 會直接由變數指向 mongoDB Atias 遠端資料庫。
- `npm start`： npm 預設指令以遠端主機與遠端 mongoDB Atias 資料庫為主。

```
npm i nodemon --save
```

專案資料夾透過 `.env` 檔案，向遠端 mongoDB Atias，請參考 `ex.env` 檔做做設定


## 相關資料
- [第二週小組任務 - 文件與說明](https://hackmd.io/3a69ZWYYRWedOBFN3GZx0g?view)