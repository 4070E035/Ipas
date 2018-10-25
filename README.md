# Ipas

# 主題三:存取控制與身分認
>* 3_1_存取控制與特權管理
>* 3_2_身分認證

# 存取控制的類別
```
預防性(Preventive)
讓不當的損害事件不會發生(消除威脅或弱點)

偵測性(Detective)
當發生不當的損害事件可被識別，以立即處理(入侵偵測)

指導性(Corrective)
發生不當的損害事件時可立即防治(滅火設備)

嚇阻性(Deterrent)
降低威脅發生的意圖，但無法阻擋(CCTV)

恢復性(Cornpensation)
對其它控制措施提供選項的控制措施
```
# 單點登錄(SSO,Single sign-on)
```
說得簡單點就是在一個多系統共存的環境下，使用者在一處登入後，就不用在其他系統中登入，也就是一次登入能得到其他所有系統的信任。
原文網址：https://itw01.com/WT2EJCP.html
相同的，單一登出（single sign-off）就是指，只需要單一的登出動作，就可以結束對於多個系統的存取權限。
```
# 資料存取控制
```
強制存取控制(mandatory access control, MAC)
以管理者授權為基礎，所有的資訊元件都需要經過管理者授權，才能被使用者所存取。

任意存取控制 (discretionary access control, DAC)
以創建資訊元件的元件持有者授權為基礎，不需要經過管理者授權，持有者授權可以決定使用者對於資訊元件的存取權限。

存取控制目錄 (access control list, ACL)
是最常見的任意存取控制的一種建置方式。
ACL 將使用者是否被允許存取每個物件以條列方式展開，並對權限作限制。

規則基準存取控制 (rule-based access control)
存取權限與使用者角色相依，資訊元件的存取被授權給角色，使用者需要先取得角色身份，才能透過角色身份取得存取權限。
例如，某公司有經理人與一般職員兩個角色，經理人可以存取A與B兩元件，但職員只可以存取B元件。
甲進入公司之後取得職員身份，依據角色存取控制方法，甲只能存取B資訊元件，直到獲得經理人角色之後，才可獲得A資訊元件的存取權限。

角色基準存取控制 (role-based access control)
是資訊安全領域中，一種較新且廣為使用的存取控制機制。
一種較新且廣為使用的存取控制機制，其不同於(強制存取控制)以及(自由選定存取控制)直接賦予使用者權限，而是將權限賦予角色。
在一個組織中，會因為不同的作業功能產生不同的角色，執行某項操作的權限會被賦予特定的角色。
組織成員或者工作人員（抑或其它系統用戶）則被賦予不同的角色，這些用戶通過被賦予角色來取得執行某項計算機系統功能的權限。
```
# 稽核追蹤(audit trail) 
```
依時間性記錄系統上的所有活動，藉由對系列活動的重整與判讀，就能找出可能的入侵行為或其他資訊安全事件。
記錄資料應包括系統、網路、應用程式、與使用者的各種活動。
記錄資料可用來警告可疑的事件，分析入侵的行為，並可用於電子犯罪調查甚至當作法庭(forensic)證據。
記錄資料量通常極大，遠超過系統管理員所能判讀，因此需要設定一些過濾機制。
應該有嚴格的控管，避免稽核追蹤記錄被竄改。
自動化的稽核追蹤工具很多，價格差異也很大，應該選擇最適合需要的工具，並因應稽核目的做適當調整。
```
# 主題四:事故管理與營運持續
 >* 4_1_事件與事故管理
 >* 4_2_備援與營運持續
# 人事安全原則
 ```
 應妥善定義組織內的角色與責任 (R&R)，並讓每個人都了解工作內容。
 讓員工知道自己工作範圍內所需要知道的機密即可。
 不要讓極重要或機密的事物掌握在一個人的手裡(separation of duties)。
 讓不同職務的人有機會主動或被動的輪調。
 ```
# 磁碟損毀與 RAID
```
失去資料有三種可能原因
1.技術性攻擊
2.實體破壞
3.磁碟損毀 (disk failure)
RAID (redundant array of independent disks, 磁碟陣列)
使用多餘磁碟進行資料複製，當一個磁碟損毀時，其它磁碟上的相同資料可以自動替補，使系統運作不會中斷。
```
# NIST 800-34 的七個步驟
```
1.建立緊急應變政策
2.進行業務衝擊分析
3.識別預防控制
4.訂定復原策略 
5.建立緊急應變計畫
6.訓練、測試、演練
7.計畫的維護
```
# 建立緊急應變政策
```
高階主管必須支持緊急應變方案，最適合的層級是組織的資訊長 (Chief Information Officer, CIO)。
緊急應變政策的主要成分應包括：
角色與責任
緊急應變計畫的範圍
所需要的資源和訓練
演練與測試的時間表
計畫維護的時間表
備份的頻率與媒體備份的存放
```
# 進行業務衝擊分析
```
業務衝擊分析 (business impact analysis, BIA)類似風險管理中的風險評鑑，是緊急應變程序的主要環節。
緊急應變協調人 (Contingency Planning Coordinator)由BIA釐清系統的需求、程序、與相互依存性，再決定緊急應變的需求與先後順序。
```
# 異地備援
```
冷備援(cold sites):具備足夠的基礎設施，但是沒有軟硬體設備或電話、傳真等辦公設備。
受災害衝擊的單位進駐後才重新建立系統，需數周時間恢復資訊服務。

暖備援(warm sites)：部分資訊與辦公室設備，平常地點及設備可能做為他用。
當緊急應變計畫啟動，受災害衝擊的單位進駐後，會在現有設備上重建系統，需要幾天到數周的時間復原資訊服務。

熱備援(hot sites)：隨時軟硬體及人員準備妥當，一旦緊急應變計畫啟動，可在幾小時內復原資訊服務。

全備援 (mirrored sites)：平時就與主機房完全同步備援，系統完全相同且資訊即時備份。一旦主機房服務中斷，備援系統立即啟動。
```
# 計畫的維護
```
為了因應業務需求，資訊系統經常升級或更新。當系統做重大變更時，就必須檢討並更新緊急應變計畫；否則至少一年檢討一次。
有些資訊則需要隨時更新，像是緊急連絡人資料。
```
