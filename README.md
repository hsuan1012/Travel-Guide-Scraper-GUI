# 世界旅遊指南檢索小幫手
[![Python Version](https://img.shields.io/badge/Python-3.12+-blue.svg)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/Framework-Tkinter-orange.svg)](https://docs.python.org/3/library/tkinter.html)
[![Scraper](https://img.shields.io/badge/Scraper-Selenium-green.svg)](https://www.selenium.dev/)

這是一個結合**動態網頁爬蟲（Web Scraping）**與**圖形使用者介面（GUI）**的 Python 整合專案。系統會自動前往「誠品書店」爬取全球各區域最新、最熱門的旅遊書籍資訊，並透過一鍵式圖形介面，讓使用者能流暢地根據「區域」與「地點」連動檢索出推薦書單與作者。

---

## 核心功能與技術亮點

* **防偵測動態爬蟲**：利用 `undetected-chromedriver` 搭配 `Selenium` 模擬真實瀏覽器行為，成功繞過動態網頁與反爬蟲機制，精準翻頁抓取誠品書店的書籍結構。
* **多區域資料範疇**：全面涵蓋「台灣旅遊」、「亞洲旅遊」、「美洲旅遊」、「歐洲旅遊」及「非洲旅遊」五大核心板塊。
* **資料結構化處理**：使用 `Pandas` 進行即時資料清洗與欄位映射，將非結構化的網頁標籤轉化為結構清晰的 `.csv` 資料庫。
* **動態連動 UI 介面**：使用 `Tkinter` 打造現代化的桌面應用程式。內建**下拉選單二級連動邏輯**（選擇區域後，自動更新對應的國家/地點選項），並支援文字模糊搜尋（`str.contains`）與原生滾動條（Scrollbar）展示。

---

## 開發環境與依賴套件

本專案基於 **Python 3.12+** 開發，執行前請確保已安裝以下套件：

```bash
pip install undetected-chromedriver selenium pandas
