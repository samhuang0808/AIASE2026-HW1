# AIASE2026-HW1 創作與渲染實作

## 1. 專案簡介
本專案將「真空設備 PHM 預測性維護計畫書」透過 Pandoc 渲染為專業 PDF 格式。

## 2. 環境需求與渲染指令
* **工具**: Pandoc, Python 3.10+, XeLaTeX
* **執行指令**:
```bash
# 安裝濾鏡
pip install mermaid-filter

# 執行轉檔
mkdir -p output
pandoc content.md -o output/output.pdf --pdf-engine=xelatex --filter mermaid-filter
