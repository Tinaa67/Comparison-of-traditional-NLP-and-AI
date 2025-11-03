GenAI作業二
從傳統到現代文本處理方法實作與比較
Comparison of Traditional NLP vs. Modern AI

本專案旨在透過實際代碼範例，比較傳統自然語言處理（NLP）方法（TF-IDF、基於規則的分類、統計式摘要）與現代AI方法（基於 Google Gemini 模型）在中文文本分析任務上的效能和特性
專案涵蓋的任務如下
1. 文本相似度： 比較 TF-IDF 餘弦相似度 (A-1) 與 AI 語義相似度(B-1)
2. 文本分類： 比較基於規則的分類器(A-2) 與 AI 分類器（B-2)
3. 自動摘要： 比較統計式關鍵句擷取(A-3) 與 AI 生成式摘要(B-3)

環境準備
1. 依賴安裝
請確保您的 Python 環境安裝了以下套件。如果您在 Colab 環境中，請使用 !pip install -q 命令。
pip install -r requirements.txt
2. API Key 設定
本專案的 AI 相關功能依賴 Google Gemini API。您需要取得 API Key 並設定環境變數或在程式碼中安全載入。
如果您在 Google Colab 上運行：請使用 Colab 左側的 密鑰 (Secrets) 面板，設定密鑰名稱為 GOOGLE_API_KEY，並將您的金鑰貼入。程式碼會自動使用 google.colab.userdata 載入。
如果您在本地環境運行：建議將金鑰設定為環境變數：
export GOOGLE_API_KEY="YOUR_API_KEY_HERE"

檔案說明
1. traditional_methods.py:包含A-1 TF-IDF 餘弦相似度, A-2 比較基於規則的分類器, A-3 比較統計式關鍵句擷取 的範例程式
2. modern_methods.py:包含B-1 AI 語義相似度, B-2 AI 分類器, B-3 AI 生成式摘要 的範例程式
3. comparison.py:包含針對傳統方法(traditional_methods.py)與現代AI (modern_methods.py) 的比較程式
4. results:包含所有範例程式的運行結果輸出截圖
5. report.md:比較分析了兩類方法的優勢、限制、實作心得與應用建議 (含量化與質性分析)
