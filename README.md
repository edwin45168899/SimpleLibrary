# 📚 SimpleLibrary

SimpleLibrary 是一個基於 `.NET 10` 的實用工具函式庫，專門提供幾種日常開發常見的整合服務，包含檔案雲端上傳、電子郵件發送、通訊軟體通知以及壓縮工具。

---

## ✨ 核心功能 (Features)

這個函式庫封裝了以下實用功能，讓你可以更快地將其引入並用於自己的專案中：

*   **☁️ AWS S3 檔案上傳**
    提供簡易的 S3 操作介面，讓你迅速上傳單一檔案或是 Zip 壓縮檔至 AWS 指定的儲存桶 (Bucket) 中，並回傳限時的預先授權下載網址 (Pre-signed URL)。
*   **📧 GMail 寄送通知**
    基於 Google SMTP 功能封裝，只要提供 Gmail 帳號與密碼 (應用程式碼)，即可群發寄送支援 HTML 格式的電子郵件通知。
*   **💬 Line Notify 通知**
    只要填寫權杖 (Token)、URL 等基本資訊，就能輕鬆透過 POST 呼叫傳出機器人推播訊息，將警報或資訊送到 Line 聊天室。
*   **🗜️ Zip 檔案壓縮**
    利用 SharpZipLib 打造的便捷方法，能夠一次自動巡覽並將指定目錄與子目錄下的所有檔案壓縮起來，產生 `.zip` 壓縮檔。
*   **📝 彈性的 Logger 介面**
    提供支援依賴注入 (DI / Autofac) 的 Console 日誌工具。你能夠自訂要使用預設 `ConsoleLogger` 或是第三方的 `ColorfulLogger` 將彩色訊息記錄傳到最底層使用。
*   **🛠️ 其他輔助套件**
    內含部分常用的擴充方法 (Extension Methods，如 `IEnumerable` 的 `ForEach`) 及設計模式基底 (例如供繼承使用的快速 `Singleton` 類別)。

---

## � 技術與套件相依 (Tech Stack & Dependencies)

*   **Target Framework**: `.NET 10.0`
*   **Autofac**: 用於 Logger 注入。
*   **AWSSDK.S3 / Core**: AWS S3 整合。
*   **Newtonsoft.Json**: 用於解析 Line 等等 REST API 的 JSON 傳遞資料。
*   **SharpZipLib**: 提供底層的高效檔案壓縮機制。

---

## 📖 官方文件與範例

如果您需要了解如何將上述各個組件實際加入程式碼內使用：

� **[Wiki 中有更進一步的程式碼使用範例與細節](https://github.com/chiisen/SimpleLibrary/wiki)**

--------------------
