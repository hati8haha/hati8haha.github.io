---
title: VARCHAR 跟 TEXT 的差別是什麼
tags:
- 資料庫
categories:
- 後端
---
### VARCHAR
通常字數較少會存成 VARCHAR，例如文章標題。

為可變長度（0 ~ 65,535）的字串，可自行設定最大的有效長度限制。

### TEXT
字數較長會存成 TEXT，例如文章內文。

純文字欄位，最大長度為同樣為 65,535，儲存時會附加 2 個位元組來記錄長度。