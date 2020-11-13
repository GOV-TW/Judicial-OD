# 司法院開放資料

司法院從 2017 開始推動開放資料，目前資料主要是以國發會開放資料平台為發布平台。同時提供兩支 API 來提供使用者下載七日前裁判書異動清單，和依照裁判書 JID 來取得裁判書內容開放資料。

- 國發會開放資料平台: https://data.gov.tw/datasets/search?qs=dtid:748
- 司法院每個月打包一次壓縮檔（更新至兩個月前）: http://data.judicial.gov.tw/
- 司法院每日更新（只保留最新兩個月）: https://bit.ly/judicial-od-jd

# 司法院裁判書開放資料 API
- https://data.gov.tw/dataset/63205
- http://data.judicial.gov.tw/jdg/api/JList : 依據當日日期提供7日前當日之裁判書異動清單 (jid 清單)
- http://data.judicial.gov.tw/jdg/api/JDoc/{jid} : 依據所輸入的 jid，提供該筆裁判書內容

# 問題與需求

目前司法院的裁判書以兩種方式發布。一個是每個月的打包壓縮檔（目前暫時停止提供），另一個是透過 API 的查詢。其中用來下載七日前的裁判書異動（發布，修正，移除）基本上就是一個清單的公布。**但是時間一過，我們就拿不到這個清單了**。

- 提供完整從 2017.11.25 到今天的所有每日 JID list 檔
- 持續更新（一直到司法院終於改變這個 API 為止）
- http://bit.ly/judicial-od-jid /JD/2017.11 - 2018.04

目前司法院在國發會平台上的開放資料一共 243 （2018.04.09）筆，這些資料一般都需要更好的重新組合與內容修正：資料優化。例如將所有的預算資料轉為 [Fiscal data package](https://frictionlessdata.io/specs/fiscal-data-package/)

- 完整備份司法院開放資料
- 提供整合後新的資料集清單和分類 (data package)
- 提供資料內容備份與下載

司法院開放資料主要以裁判書與法拍屋為最大宗，但是這兩個資料集和其內容都需要進一步的彙整與處理

- 裁判書資料與內容轉換與清洗
- 引入 Akoma Ntoso / LegalXML 格式
- 建立裁判書閱讀器


