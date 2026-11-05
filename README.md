# Alkaid CS2 共用商品資料

此公開資料庫僅發布 Alkaid CS2 使用的商品身分、別名字典及已簽章更新清單。程式原始碼、Facebook 貼文、登入資料、個人設定、GitHub 憑證和簽章私鑰不包含於本庫。

## 使用方式

Alkaid 0.63.0 以上，可在設定的更新來源填入：

`https://raw.githubusercontent.com/Alkaid-Delta/Alkaid-CS2-Origin/main/stable.json`

按「檢查並下載更新」，驗證通過後按「套用已下載更新」。也可自行選擇每六小時檢查與自動套用。來源無法連線或清單過期時，沿用已安裝商品資料。

需要離線使用時，下載 Releases 中的商品 ZIP，透過設定中的「檢查商品資料包」匯入。首次套用後可回復內建資料；回復不會立即被同一個線上更新覆蓋。

## 驗證與版本

更新清單與 ZIP manifest 都有 Ed25519 簽章。信任依據是程式內固定公鑰；本庫的公鑰檔僅供比對，不能自行新增程式的信任權限。SHA-256 不取代發布者簽章。

每個 ZIP 只包含五份 JSON 商品資料及 reference-release.json。它不包含價格行情，不修改個人的倍率或獲利門檻，也不包含可執行更新碼。貼紙資料僅供商品身分辨識，不代表加入槍皮估值。

清單預設有效七天。維護者可在商品不變時，以較高清單序號重新簽署，無須變更資料版本；過期不會刪除本機資料。

資料來源與授權見 [SOURCES.md](SOURCES.md)，格式見 [schemas](schemas)，版本紀錄見 [CHANGELOG.md](CHANGELOG.md)。
