# Vibe Code Karma (AI債贖罪券)

> "Redeeming the karma from your vibe-driven code, one commit at a time."
> 一次一個 commit，償還技術債XD。
>
> "Ask not what AI can do for you, ask what you can do for AI."
> 你不要問AI為你做了什麼，要問你為AI做了什麼。

## 📖 專案簡介

這是一個針對Vibe Coding工具使用者的技術庫和思維參考。Vibe Coding的應用範圍很廣，其實也不止寫程式。所以這裡的涉獵可能也很雜。
網上針對各種技術的文章大多是從程序員、筆記專家這樣的角度切入，而少有從AI輔助工作的思維角度切入的。所以希望能拋磚引玉。
祝福大家都能享受「Vibe Coding」但不要產生一堆資安和可維護性都很可怕的東西。
作者也是大小白，一起來償還AI輔助產生的技術債吧~

## 🎯 什麼是 Vibe Coding？

Vibe Coding是什麼？簡單暴力的說法就是用嘴巴指揮LLM來寫程式、寫網站、寫內容。
這種工具的核心是有一個人機交互界面、以及一個（或數個）大語言模型，

還有！**人的大腦！！**沒錯人還是最重要的，只要你敢想，就可以Vibe！

## 🛠️ Vibe Coding 應用場景

### 🚀 編程

Vibe Coding最常見的應用當然還是編程。
快速開發上線網站、應用，自己做一個windows批量小程式讓工作更簡便等……
不同於傳統程序員要考慮開發週期、語言的學習曲線，Vibe Coding的開發在語言、框架等選擇上更考慮效能、搭配，以及適用場景。不用再被哪個語言束縛的同時，要如何選擇最適合的反而是難度和智慧所在。
這裡提供一些現在主流的開發語言介紹、對比，以及它們在AI輔助開發的場景下的應用。

Vibe Coding時應該不用再去關心代碼內容，而更應該注重是否了解整體開發的架構、框架、語言或LLM應用的優劣和選擇。

使用場景：
在商業應用的時候，能夠快速完成原型的交付（功能確認），但很難完成最後的代碼交付。
對個人應用來說，可以無腦完成個人用或者一次性用的程式。可以輔助開發個人程度可上線的內容。

#### 📱 移動開發

📄 **[Mobile Development Guide](mobile-development.md)** - 移動開發語言選擇指南 - 原生 vs 跨平台開發對比、Kotlin/Swift/React Native/Flutter 優劣分析、AI 時代的移動應用開發策略

#### 💻 桌面開發

📄 **[Desktop Development Guide](desktop-development.md)** - 桌面開發語言選擇指南 - 原生開發 vs 跨平台開發 vs 網頁技術封裝、C++/C#/Swift/Tauri/.NET MAUI/Electron 技術選型、AI 時代的桌面應用開發策略

#### ⚙️ 系統管理

📄 **[System Management Guide](system-management.md)** - 系統管理語言指南 - PowerShell/Bash/Python 在不同平台的應用場景、個人開發者實務應用案例、AI 輔助系統自動化

#### 💎 通用程式語言

📄 **[General Programming Guide](general-programming.md)** - 通用程式語言分析 - Ruby/Java 在 AI 時代的定位、為什麼個人開發者應選擇專門化工具、企業級與個人開發的技術選型差異

#### 🌐 Web 開發

📄 **[Web Development Guide](web-development.md)** - Web開發語言選擇指南 - 前端/後端技術對比、JavaScript/TypeScript/Python/PHP/Node.js 優劣分析、AI 時代的Web開發語言選擇策略

📄 **[Web Deployment Guide](./web-deployment-guide.md)** - CSR vs 傳統HTML開發指南 - 客戶端渲染 (CSR) 與傳統HTML比較、React vs Vue vs Svelte 框架分析、現代Web開發技術選擇策略

📄 **[Web Applications Guide](web-applications.md)** - Web應用實作指南 - 圖像處理、數據可視化、企業級應用、SPA/SSR/SSG架構選擇、AI時代的Web應用開發策略

📄 **[JavaScript Animation Libraries Guide](js-animation-libraries.md)** - JavaScript動畫庫完全指南 - GSAP/Anime.js/Three.js/React動畫庫全面對比、通用型vs框架型動畫方案、現代網頁動態表現技術選擇策略

#### 🗄️ 資料庫、RAG

📄 **[Database Choice Guide](database-choice.md)** - 資料庫選擇指南 - MySQL/MongoDB/PostgreSQL/SQLite 深度對比、關聯式資料庫 vs NoSQL vs 向量資料庫、AI輔助開發時代的資料庫技術選型策略

#### 🌐 在實務程式開發的時候AI輔助的問題

解析todo問題的時候LLM不知道怎麼綜合多個todo，可能產生重複的PR
人必須不停地切分。
與Coding的思考方向相反，Coding的時候是從微小開始構築，AI輔助編程的時候需要從整體框架一直切分。

### 📝 知識管理與研究

LLM帶來的最大革新是顛覆人對知識獲取和內化的方式，能夠通過簡易的提問和連續追問快速獲得準確的研究報告和資訊，這是利。但同時也因為“幻覺”讓假資料橫行，如何區分真偽避免被誤導又成為了必須學習的新技能，此為弊。
要如何趨利避害去完成筆記、知識庫的整理、研究和自動搜索但篩選結果？

- **筆記整理與知識庫建構** - 自動化筆記分類、標籤管理、知識圖譜建立
- **文獻研究與資料收集** - 學術論文爬取、引文分析、研究趨勢追蹤
- **網路搜索優化** - 搜索策略自動化、結果篩選、資訊去重

#### 🔍 數據收集與分析

老馬向世界證明了只要你有LLM，百年官府資料也可以瞬間debug和查貓膩。數據整理和挖掘在AI輔助的時代能力是爆炸的。同時，大數據的爬取難度降低、LLM讓語言壁壘降低、內容生成不再辛苦。
怕的只是沒有思路，不怕沒有技術可以達成。

- **網頁爬蟲與數據挖掘** - 電商價格監控、社群媒體分析、新聞資訊收集
- **API 整合與數據處理** - 多平台數據聚合、自動報表生成、數據可視化
- **內容自動化** - 社群媒體發布、郵件營銷、內容管理系統

#### ⚙️ 日常自動化

nocode類workflow自動化工具能夠崛起，證明了人類在電腦前重複操作的作業真的很多。原本辦公室自動化依賴嚴格的流程設定，nocode類接入LLM讓workflow的設定變得可以通過網站上的幾個icon拖來拖去就解決。Vibe Coding工具更進一步，不只是網上的服務可以自動化對接，自己電腦裡的也可以，而且不受限方式，可以依照自己的需求來自定義需要的批量操作、流程化工具。

- **文件處理與轉換** - 批量格式轉換、內容提取、文件合併分割
- **工作流程自動化** - 定時任務、系統監控、自動備份
- **多媒體處理** - 圖片批處理、影音轉碼、縮圖生成

#### 🎮 創意與實驗

還有很多很多可以做，尤其遊戲對接現在怎麼這麼少和AI整合的，一片歲月靜好……XD

- **小型遊戲與互動應用** - 簡單遊戲開發、互動藝術、數據可視化
- **IoT 與硬件控制** - 智能家居、感測器數據處理、自動化控制
- **機器學習實驗** - 小型AI模型、圖像識別、自然語言處理

## 🎯 專案目標

## 🤝 貢獻指南

歡迎提交 Issue 和 Pull Request 來幫助改善這個專案！

## 📝 授權條款

本專案採用 MIT 授權條款 - 詳見 [LICENSE](LICENSE) 檔案
