# AIASE2026-HW1：真空設備 PHM 預測性維護計畫書實作

## 1. 專案簡介
* **內容摘要**：本專案 `content.md` 紀錄了一份針對「智慧製造真空設備」的預測性維護（PHM）計畫書。核心內容包含市場痛點分析、技術規格、邊緣 AI 診斷邏輯、雙案場數據架構及開發進度。
* **選用工具與理由**：選用 **Pandoc** 作為渲染工具。理由是其為業界標準的開源文件轉換器，能精準解析 Markdown 中的表格、數學公式與代碼區塊，並支援透過濾鏡（filter）擴充 Mermaid 流程圖渲染功能。

## 2. 環境需求
* **作業系統**：建議使用 Windows (PowerShell/Anaconda) 或 Linux (Ubuntu)。
* **語言 Runtime**：Python 3.10 或更高版本。
* **系統層套件**：需安裝 `pandoc` 執行檔。

## 3. 安裝步驟
請在您的終端機（Terminal）執行以下指令來配置環境：

```bash
# 1. 安裝系統工具 Pandoc (Windows 建議透過 Conda 安裝)
conda install -c conda-forge pandoc -y

# 2. 安裝 Mermaid 濾鏡以支援流程圖渲染
pip install mermaid-filter

# 3. 安裝專案依賴套件
pip install -r requirements.txt
```
## 4. 執行渲染
請確保位於專案根目錄（包含 `content.md` 的位置），並於終端機執行以下指令。輸出結果將儲存於 `output/` 資料夾：

```bash
# 建立輸出資料夾
mkdir -p output

# 執行轉檔指令 (優先渲染為 HTML 以獲得最佳相容性與圖表呈現)
pandoc content.md -o output/output.html --filter mermaid-filter
```
## 5. 預期輸出
渲染完成後，預期的成果應包含以下內容：
* **最終輸出檔名**：`output/output.html` (或 `output.pdf`)。
* **輸出樣貌說明**：
    * **結構化內容**：呈現專業的技術計畫書格式，包含清晰的 1-5 級標題與技術規格對照表。
    * **程式碼高亮**：包含具備語法高亮的 Python 邊緣運算程式碼區塊。
    * **圖表渲染**：正確呈現以 Mermaid 語法繪製的雙案場數據鏈架構圖。
    * **任務追蹤**：計畫書末端的開發進度將顯示為已勾選的任務清單格式 `[x]`。

## 6. 參考資料
* [Pandoc 官方手冊 (Official User Guide)](https://pandoc.org/MANUAL.html)
* [Mermaid Filter GitHub 儲存庫](https://github.com/jagregory/pandoc-mermaid-filter)
* [Markdown 語法參考指南 (Markdown Guide)](https://www.markdownguide.org/)
