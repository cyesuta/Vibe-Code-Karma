# LLM 模型選擇指南

## 📖 概述

在 AI 輔助開發的時代，選擇合適的 LLM 模型是成功的關鍵。本指南將幫助你了解不同 LLM 模型的特點、優勢和適用場景，讓你能夠根據具體需求做出最佳選擇。

## 🔗 快速連結

### Google Gemini

- **價格資訊**: [Gemini API 定價](https://ai.google.dev/gemini-api/docs/pricing)
- **方案資訊**: [Gemini 方案詳情](https://aistudio.google.com/plan_information)
- **AI Studio**: [Google AI Studio](https://aistudio.google.com/)
- **API 金鑰管理**: [AI Studio API Key](https://aistudio.google.com/app/apikey)
- **Google Cloud Console**: [APIs Dashboard](https://console.cloud.google.com/apis/dashboard)
- **使用量監控**: [Google Cloud Usage](https://console.cloud.google.com/apis/dashboard)

### Grok (xAI)

- **網頁端介面**: [Grok](http://grok.com/)
- **API 控制台**: [xAI Console](https://console.x.ai/)
- **模型與定價**: [Grok Models & Pricing](https://docs.x.ai/docs/models#models-and-pricing)

### OpenAI

- **網頁端介面**: [ChatGPT](https://chatgpt.com/)
- **組織限制**: [OpenAI Organization Limits](https://platform.openai.com/settings/organization/limits)
- **API 金鑰管理**: [OpenAI API Keys](https://platform.openai.com/settings/api-keys)
- **使用量監控**: [OpenAI Usage](https://platform.openai.com/usage)

### Claude (Anthropic)

- **API 控制台**: [Anthropic Console](https://console.anthropic.com/)

### DeepSeek

- **網頁端介面**: [DeepSeek Chat](http://chat.deepseek.com/)
- **API 金鑰管理**: [DeepSeek API Keys](https://platform.deepseek.com/api_keys)

### Kimi (Moonshot AI)

- **API 金鑰管理**: [Kimi API Keys](https://platform.moonshot.cn/console/api-keys)

### 百煉 (阿里雲)

- **API 金鑰管理**: [阿里雲百煉 API](https://bailian.console.aliyun.com/?tab=model#/api-key)
- **模型列表及價格**: [百煉模型價格表](https://help.aliyun.com/zh/model-studio/models)
- **通義產品頁**: [阿里雲通義](https://cn.aliyun.com/product/tongyi)

## 🔧 LLM 模型集成 API

### SiliconFlow (硅基流動)

- **國際版**: [SiliconFlow Cloud](https://cloud.siliconflow.com/account/ak)
- **中國版**: [硅基流動中國](https://cloud.siliconflow.cn/account/ak)

### 其他集成平台

- **AIHubMix**: [AIHubMix Platform](https://aihubmix.com/)
- **OpenRouter**: [OpenRouter API Keys](https://openrouter.ai/settings/keys)
- **Monica API**: [Monica 綜合 API](http://monica.im/)

## 📊 主要 LLM API 接口對比

### 各 LLM 模型特色及 API 調用價格

| **模型名稱** | **擅長領域** | **價格（每 1M 令牌）** | **調用限制** | **平均價格（美元）** |
| --- | --- | --- | --- | --- |
| **Gemini 1.5 Flash-8B** | 低延遲、多語言、摘要 | **<128K 令牌:** 輸入 $0.0375, 輸出 $0.15<br>**>128K 令牌:** 輸入 $0.075, 輸出 $0.30 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 0.09375 (短令牌) |
| **Gemini 2.0 Flash-Lite** | 長上下文、實時串流、原生工具使用 | 輸入 $0.075, 輸出 $0.30 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 0.1875 |
| **Gemini 1.5 Flash** | 圖像理解、影片理解、音訊理解 | **<128K 令牌:** 輸入 $0.075, 輸出 $0.30<br>**>128K 令牌:** 輸入 $0.15, 輸出 $0.60 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 0.1875 (短令牌) |
| **DeepSeek-V2** | 自然語言處理、代碼生成、問題解答、對話系統 | 輸入 $0.14, 輸出 $0.28 | RPM: 1000, TPM: 1M, 批量 RPM: 1000 | 0.21 |
| **DeepSeek-V2.5** | 增強的自然語言理解、複雜推理、代碼輔助、對話系統 | 輸入 $0.14, 輸出 $0.28 | RPM: 1000, TPM: 1M, 批量 RPM: 1000 | 0.21 |
| **DeepSeek-Coder-V2** | 代碼生成、代碼理解、技術文檔生成 | 輸入 $0.14, 輸出 $0.28 | RPM: 1000, TPM: 1M, 批量 RPM: 1000 | 0.21 |
| **DeepSeek-Coder-V2.5** | 增強的代碼生成、複雜編程任務、技術文檔生成 | 輸入 $0.14, 輸出 $0.28 | RPM: 1000, TPM: 1M, 批量 RPM: 1000 | 0.21 |
| **Gemini 2.0 Flash** | 多模態理解、實時串流、原生工具使用 | 輸入 $0.10, 輸出 $0.40 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 0.25 |
| **Gemini 2.0 Flash Preview** | 多模態理解、多模態生成、原生工具使用 | **文字:** 輸入 $0.10, 輸出 $0.40<br>**圖像:** 輸入 $0.10, 輸出 $0.039 (每圖像) | RPM: 15, TPM: 1M, 批量 RPM: 1 | 0.25 (文字) |
| **Claude 3 Haiku** | 快速回應、聊天機器人、文本生成、摘要 | 輸入 $0.25, 輸出 $1.25 | RPM: 500, TPM: 1M, 批量 RPM: 1000 | 0.75 |
| **OpenAI GPT-4o Mini** | 低延遲、輕量級任務、快速回應 | 輸入 $0.15, 輸出 $0.60 | RPM: 3500, TPM: 350K, 批量 RPM: 10000 | 0.375 |
| **Grok 3 Mini (with Thinking)** | 邏輯任務、無需深度領域知識、快速回應 | 輸入 $0.30, 輸出 $0.50 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 0.40 |
| **Grok 3 Mini Beta** | 與 Grok 3 Mini 相同，但提供更快的回應速度 | 輸入 $0.30, 輸出 $0.50 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 0.40 |
| **Claude 3.5 Haiku** | 快速回應、聊天機器人、文本生成、摘要 | 輸入 $0.80, 輸出 $4.00 | RPM: 1000, TPM: 1M, 批量 RPM: 1000 | 2.40 |
| **OpenAI GPT-3.5 Turbo** | 快速回應、聊天機器人、文本生成、摘要 | 輸入 $0.50, 輸出 $1.50 | RPM: 3500, TPM: 350K, 批量 RPM: 10000 | 1.00 |
| **Gemini 2.5 Flash Preview** | 大規模處理、低延遲、思考任務、代理使用案例 | **思考類:** 輸入 $0.15, 輸出 $3.50<br>**非思考類:** 輸入 $0.15, 輸出 $0.60 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 1.825 (思考類) |
| **Grok 3 Mini Fast Beta** | 與 Grok 3 Mini 相同，但提供更快的回應速度 | 輸入 $0.60, 輸出 $4.00 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 2.30 |
| **Gemini 1.5 Pro** | 長上下文、複雜推理、數學推理 | **<128K 令牌:** 輸入 $1.25, 輸出 $5.00<br>**>128K 令牌:** 輸入 $2.50, 輸出 $10.00 | RPM: 2, TPM: 60K, 批量 RPM: 1 | 3.125 (短令牌) |
| **Gemini 2.5 Pro** | 編碼、推理、多模態理解 | **<200K 令牌:** 輸入 $1.25, 輸出 $10.00<br>**>200K 令牌:** 輸入 $2.50, 輸出 $15.00 | RPM: 2, TPM: 60K, 批量 RPM: 1 | 5.625 (短令牌) |
| **Grok 2 Vision** | 文字和圖像輸入、視覺理解 | **文字輸入:** $2.00, **圖像輸入:** $2.00, **輸出:** $10.00 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 6.00 (文字+輸出) |
| **Grok 3** | 企業用例（資料提取、編碼、文本摘要）、深度領域知識（金融、醫療、法律、科學） | 輸入 $3.00, 輸出 $15.00 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 9.00 |
| **Grok 3 Beta** | 與 Grok 3 相同，但提供更快的回應速度 | 輸入 $3.00, 輸出 $15.00 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 9.00 |
| **Claude 3.5 Sonnet** | 企業用例、複雜推理、編碼、創意寫作 | 輸入 $3.00, 輸出 $15.00 | RPM: 500, TPM: 1M, 批量 RPM: 1000 | 9.00 |
| **OpenAI GPT-4o** | 多模態理解（文字、圖像）、視覺推理、實時互動 | 輸入 $5.00, 輸出 $15.00 | RPM: 300, TPM: 450K, 批量 RPM: 1000 | 10.00 |
| **Grok 3 Fast Beta** | 與 Grok 3 相同，但提供更快的回應速度 | 輸入 $5.00, 輸出 $25.00 | RPM: 15, TPM: 1M, 批量 RPM: 1 | 15.00 |
| **OpenAI GPT-4 Turbo** | 複雜推理、編碼、創意寫作、多語言處理 | 輸入 $10.00, 輸出 $30.00 | RPM: 300, TPM: 450K, 批量 RPM: 1000 | 20.00 |
| **Claude 3 Opus** | 高級推理、深度分析、複雜問題解決 | 輸入 $15.00, 輸出 $75.00 | RPM: 500, TPM: 1M, 批量 RPM: 1000 | 45.00 |
| **OpenAI GPT-4** | 高級推理、複雜問題解決、深度分析 | 輸入 $30.00, 輸出 $60.00 | RPM: 300, TPM: 450K, 批量 RPM: 1000 | 45.00 |
| **Grok 2 Image** | 圖像生成 | 每張生成圖像 $0.07 | RPM: 15, TPM: 1M, 批量 RPM: 1 | - |

## 🎯 主要 LLM 模型對比