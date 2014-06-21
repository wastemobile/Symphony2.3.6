# Symphony 2.3.6

- Date: 29th January 2014
- Release Notes: <http://getsymphony.com/download/releases/version/2.3.6/>
- Github Repository: <http://github.com/symphonycms/symphony-2/tree/2.3.6>

## 私人版本註記

- **v0.1** 僅升級了 Markdown Extension 到 1.18 的乾淨版本。Update [markdown](https://github.com/symphonycms/markdown) to 1.18 [@a6daee6](https://github.com/symphonycms/markdown/tree/a6daee62860e3946dacf5a7edf41f5c115c3c328)

## 資料庫處理

Symphony CMS 最麻煩的是資料庫的同步（包含升級），正因為它很方便的

* [CDI - Continuous Database Integration](http://symphonyextensions.com/extensions/CDI/) 不明原因無法安裝，不會出現在後台 Extensions 頁面中。
* 使用 [Database Synchroniser](http://symphonyextensions.com/extensions/db_sync/) 這個外掛：啟用後會增加這個 `/manifest/db_sync.sql` 檔案，記錄各種資料庫結構的異動。

**工作流程**

開發到一階段，將正式主機的資料庫拉回開發主機，測試各項資料無誤，再將 `db_sync.sql` 套用到正式主機。然後殺掉舊的 `db_sync.sql`（或是異名備份），繼續開發工作。

## Extensions

- 安裝 Database Synchroniser `git submodule add https://github.com/symphonists/db_sync.git extensions/db_sync --recursive`
- 安裝 Remote Datasource 並手動返回 1.1 版 `git submodule add https://github.com/symphonycms/remote_datasource.git extensions/remote_datasource --recursive`
- Server Headers `git submodule add https://github.com/symphonycms/serverheaders.git extensions/serverheaders --recursive`
- 安裝 Database Synchroniser 記錄資料庫結構的異動 `git submodule add https://github.com/symphonists/db_sync.git extensions/db_sync --recursive`
- 安裝 Entity Diagram 從後台清楚檢視資料庫的關聯性 `git submodule add https://github.com/symphonists/entity_diagram.git extensions/entity_diagram --recursive`
- 安裝 Import/Export CSV 處理單獨保留某 section 資料時使用 `git submodule add https://github.com/TwistedInteractive/importcsv.git extensions/importcsv --recursive`
- 安裝 APIPage 外掛，用於建立支援 `json|jsonp|xml` 的 API 頁面 `git submodule add https://github.com/iwyg/apipage.git extensions/apipage --recursive`
- 安裝 XML Importer 用於匯入本地或遠端的 XML 資源 `git submodule add https://github.com/symphonists/xmlimporter.git extensions/xmlimporter --recursive`
- 必要的前端會員管理外掛 `git submodule add https://github.com/symphonycms/members.git extensions/members --recursive`
