# OWASP組織是什麼?
```
Open Web Application Security Project 開放網站應用程式安全計畫

我們可以透過網路上OWASP組織提供的防護方法以及弱點介紹，我們可以很快地檢視自己的網站是否有安全弱點。
OWASP是一個開放社群的非營利組織，致力於改善網站應用程式的安全性。
OWASP Top 10揭露常見的網站應用程式弱點，以供軟體開發安全參考。
```
# 注入攻擊(Injection)
```
SQL注入攻击（SQL injection），简称SQL攻击或注入攻击，是发生于应用程序与数据库层的安全漏洞。简而言之，是在输入的字符串之中注入SQL指令，
在设计不良的程序当中忽略了字符检查，那么这些注入进去的恶意指令就会被数据库服务器误认为是正常的SQL指令而运行，因此遭到破坏或是入侵。
```
# 無效身份認證 (Broken Authentication)
```
主要是因為網路應用程式必須進行身份認證和工作階段管理，此時若導入方式不正確，就有可能會讓攻擊者取得密碼、金鑰、工作階段存取令牌、…等
暫時或永久取得使用者的身份資訊。所以建議在可能的情況下落實多因素的身份驗證機制，以利避免無效身份認證的攻擊成功。
```
# 敏感資料外洩 (Sensitive Data Exposure)
```
主要是因為有許多網路應用程式對於金融資訊、健康資料和個人資料的保護不足，若是被攻擊者取得，將能夠進行信用卡詐欺、身份竊取或其它犯罪行為。
所以建議針對應用程式的處理、存儲或傳輸的資料進行分類，並且根據個人隱私法、監管機關的要求和業務的需求確定哪些資料是敏感性資料，以利進行額外的保護措施。
```
# XML 外部處理器漏洞 (XML External Entity，XEE)
```
主要是因為以 XML 為基礎的網路應用程式沒有管控好權限，直接處理 XML 語法的請求或上傳，此時攻擊者僅需要加入一個惡意的 XML 文件，
就能夠鎖定 XML 處理器漏洞進行攻擊，進而導致資料外洩的風險。
```
# 無效的存取控管 (Broken Access Control)
```
僅能藉由嚴格的存取控管，以利避免攻擊者利用漏洞存取沒有經過授權的功能或查看敏感資料。同時授權使用者、群組和角色存取的功能也是許多套裝軟體解決方案基本的安全功能之一，所以存限控管會是資安管理的首要第一步，有完善的存限控管機制將能夠降低被攻擊的資安風險。
```
# 不安全的組織設定 (Security Misconfiguration)
```
系統的安全性取決於應用程式、伺服器、平台的設定。因此所有設定值必須確保安全，避免預設帳號、密碼、路徑等。
甚至被Google Hacking直接取得攻擊弱點。

防護建議：

軟體、作業系統是否都有更新到最新版本？是否都有上最新Patch?
不需要的帳號、頁面、服務、連接埠是否都有關閉？
預設密碼是否都有更改？
安全設定是否都完備？
伺服器是否都有經過防火牆等設備保護？ 
```
# 跨站攻擊 (Cross-Site Script，XSS)
```
網站應用程式直接將來自使用者的執行請求送回瀏覽器執行，使得攻擊者可擷取使用者的Cookie或Session資料而能假冒直接登入為合法使用者。
此為目前受災最廣的攻擊。

攻擊流程如下:

受害者登入一個網站
從Server端取得Cookie
但是Server端上有著XSS攻擊，使受害者將Cookie回傳至Bad Server
攻擊者從自己架設的Bad Server上取得受害者Cookie
攻擊者取得控制使用受害者的身分
```
# 不安全的反序列化漏洞 (Insecure Deserialization)
```
主要是針對 Java 、 Node.js、…等平台常見的攻擊方式，簡單來說，序列化主要會將執行時的變數和程序物件轉換為可以儲存或傳輸形式的過程，形式主要有 JSON、XML 或二進位格式，反序列化則是將序列化形式轉換為記憶體變數和程序物件的相反過程，此時攻擊者若可以將資料進行反序列化，那將會對記憶體中的變數和程序物件產生影響， 之後將會導致遠端程式碼執行、重播攻擊、注入攻擊、特權升級攻擊、…等攻擊方式成功。所以建議針對任何序列化的物件落實完整性的檢查，像是數位簽章，以利防止惡意物件的建立或資料被篡改。
```
# 使用已有漏洞的元件 (Using Components with Known Vulnerabilities)
```
第三方的元件、框架或模組，經常是擁有完整的系統執行權限，所以一旦有已知漏洞被利用，
往往可能造成嚴重的資料遭竊或系統被綁架。

未經驗證的重新導向與轉送（Unvalidated Redirects
```
# 記錄與監控不足的風險 (Insufficient Logging & Monitoring)
```
記錄與監控不足的風險主要是因為微服務快速興起，卻沒有針對應用程式進行記錄和監控，此時因為記錄和監控的不足，所以當資安事件發生時就無法立即處理與解決問題，同時讓攻擊者有機會更進一步攻擊系統。所以建議確保所有使用者登入、存取控制失敗和伺服器端輸入驗證失敗皆進行記錄，以利識別可疑或惡意的帳戶，並且保留足夠的時間允許延遲進行數位鑑識分析
```
# 2017 OWASP TOP 10
```
A1  Injection(注入攻擊)
A2  Broker Authentication(無效身份認證)
A3  Sensitive Data Exposure(敏感資料外洩)
A4  XML External Entities (XXE)(XML 外部處理器漏洞)
A5  Broken Access Control(無效的存取控管)
A6  Security Misconfiguration(不安全的組織設定)
A7  Cross-Site Script (XSS)(跨站攻擊)
A8  Insecure Deserialization(不安全的反序列化漏洞)
A9  Using Components with Known Vulnerabilities(使用已有漏洞的元件)
A10 Insufficient Logging and Monitoring(記錄與監控不足的風險)
```
# 參考網址
```
https://www.ithome.com.tw/news/118411
https://ithelp.ithome.com.tw/articles/10189733
http://newsletter.ascc.sinica.edu.tw/news/read_news.php?nid=1917
https://leoyeh.me/2017/11/24/%E8%B3%87%E5%AE%89%E7%AE%A1%E7%90%86-OWASP-Top-10-1/
http://newsletter.ascc.sinica.edu.tw/news/read_news.php?nid=1917
```
